# Audio Shear Zone — Sequence Scripting Guide

Sequences are JSON files that script a timed session — fading sounds in and out, engaging binaural tones, triggering spoken guidance, and moving through a designed arc of experience. No coding required. If you can edit a text file, you can write a sequence.

---

## File structure

Every sequence lives in the `sequences/` folder and must be listed in `sequences/manifest.json` to appear in the tool.

### manifest.json

```json
{
  "programs": [
    {
      "file": "onboarding.json",
      "title": "Introduction to the Audio Shear Zone (5 min)"
    },
    {
      "file": "my_sequence.json",
      "title": "My Custom Session (20 min)"
    }
  ]
}
```

Add one entry per sequence. The `file` value is the filename inside the `sequences/` folder. The `title` is what appears in the Programs dropdown.

### sequence file

```json
{
  "id": "my_sequence",
  "title": "My Custom Session",
  "duration": 1200,
  "steps": [
    ...
  ]
}
```

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Internal identifier, no spaces |
| `title` | string | Display name |
| `duration` | number | Total session length in **seconds** |
| `steps` | array | Ordered list of timed events |

The `duration` field controls the progress bar. The session doesn't stop automatically when duration is reached — include explicit fade-out steps near the end.

---

## Steps

Each step is an object with at minimum a `t` (time in seconds from start) and an `action`. Steps fire in parallel if their `t` values overlap — you can fade in ocean at t:0 and start a noise fade at t:5 without either blocking the other.

```json
{"t": 0, "action": "env", "target": "ocean", "vol": 0, "fadeTo": 0.5, "fadeTime": 8}
```

### Common fields

| Field | Type | Description |
|-------|------|-------------|
| `t` | number | Time in seconds from session start when this step fires |
| `action` | string | What to do — see action types below |
| `label` | string | Optional — status bar message shown when step fires |

---

## Action types

### `env` — environmental sound

Starts an environmental sound and/or fades its volume.

```json
{"t": 0, "action": "env", "target": "ocean", "vol": 0, "fadeTo": 0.5, "fadeTime": 8, "label": "Ocean fading in..."}
```

| Field | Description |
|-------|-------------|
| `target` | One of: `ocean` `rain` `wind` `fire` `thunder` `cave` |
| `vol` | Starting volume (0–1). Omit to use current volume. |
| `fadeTo` | Target volume (0–1) |
| `fadeTime` | Fade duration in seconds |

Only one environmental sound can be active at a time. Starting a new one stops the previous.

**To fade out and stop:**

```json
{"t": 280, "action": "stop_env", "fadeTime": 18, "label": "Ocean fading out..."}
```

---

### `noise` — noise color

Starts a noise color and/or fades its volume.

```json
{"t": 30, "action": "noise", "target": "pink", "vol": 0, "fadeTo": 0.2, "fadeTime": 10}
```

| Field | Description |
|-------|-------------|
| `target` | One of: `white` `pink` `brown` `blue` `violet` `grey` |
| `vol` | Starting volume (0–1) |
| `fadeTo` | Target volume (0–1) |
| `fadeTime` | Fade duration in seconds |

To fade out noise, set `fadeTo: 0`. Only one noise color can be active at a time.

---

### `harm` — harmonic / resonant tone

Starts a harmonic layer and/or fades the harmonic bus volume.

```json
{"t": 60, "action": "harm", "target": "om", "vol": 0, "fadeTo": 0.45, "fadeTime": 8}
```

| Field | Description |
|-------|-------------|
| `target` | One of: `drone` `bowl` `om` `iso` `heart` `wand` |
| `vol` | Starting volume (0–1) |
| `fadeTo` | Target volume (0–1) |
| `fadeTime` | Fade duration in seconds |

Note: all active harmonics share a single gain bus. Fading the harmonic volume affects all active harmonic layers simultaneously. Multiple harmonics can run at the same time.

**To stop a specific harmonic:**

```json
{"t": 240, "action": "stop_harm", "target": "om", "fadeTime": 8}
```

---

### `binaural` — binaural tone

Sets beat and carrier frequencies and fades the binaural tone in or out. Automatically starts the tone if it isn't running.

```json
{"t": 90, "action": "binaural", "beat": 10, "carrier": 396, "fadeTo": 0.15, "fadeTime": 15, "label": "Binaural engaging at Alpha I"}
```

| Field | Description |
|-------|-------------|
| `beat` | Beat (difference) frequency in Hz. Recommended range: 0.5–28 Hz |
| `carrier` | Carrier (base) frequency in Hz. Recommended range: 174–963 Hz |
| `fadeTo` | Target master volume (0–1). Keep low (0.1–0.2) when voice is present |
| `fadeTime` | Fade duration in seconds — use long fades (10–20s) for smooth onset |

To fade out the binaural tone:

```json
{"t": 220, "action": "binaural", "fadeTo": 0, "fadeTime": 20, "label": "Binaural fading out..."}
```

**Binaural beat frequency reference:**

| Range | Hz | State |
|-------|----|-------|
| Delta | 0.5–4 Hz | Deep sleep, restoration |
| Theta | 4–8 Hz | Trance, imagery, dream |
| Schumann | 7.83 Hz | Earth resonance |
| Alpha | 8–12 Hz | Relaxed alertness |
| Beta | 12–28 Hz | Focus, active cognition |

**Carrier frequency reference** (Solfeggio):

| Hz | Association |
|----|-------------|
| 174 | Grounding |
| 285 | Field / tissue |
| 396 | Release |
| 417 | Change |
| 432 | Natural tuning |
| 528 | Transformation |
| 639 | Connection |
| 741 | Expression |
| 852 | Intuition |
| 963 | Unity / Crown |

---

### `speak` — spoken guidance (Web Speech API)

Speaks a line of text using the browser's built-in speech synthesis. No audio files needed — works immediately in any modern browser.

```json
{"t": 10, "action": "speak", "text": "Welcome. Find a comfortable position and breathe slowly.", "rate": 0.78, "pitch": 0.85}
```

| Field | Default | Description |
|-------|---------|-------------|
| `text` | required | The words to speak |
| `rate` | 0.82 | Speech rate. 0.7–0.85 recommended for meditation guidance |
| `pitch` | 0.88 | Voice pitch. Lower values feel more grounded |
| `volume` | 0.9 | Speech volume (0–1) |

**Tips for spoken guidance:**
- Keep individual spoken segments under 30 seconds where possible
- Leave at least 20–30 seconds between speak steps so the voice isn't interrupted
- Schedule voice steps 5–10 seconds *after* a sound change so the listener has settled before being spoken to
- Lower `rate` (0.72–0.78) and `pitch` (0.82–0.88) makes the voice feel slower and more grounded — appropriate for deep states
- The voice quality varies by operating system and browser. For production quality, pre-render with ElevenLabs and use the `audio` action instead (see below)

---

### `audio` — pre-rendered audio file *(for ElevenLabs / production voice)*

Plays an MP3 or WAV file from the `sequences/audio/` folder. Use this for production-quality guidance voice rendered with ElevenLabs or any other TTS tool.

```json
{"t": 10, "action": "audio", "src": "sequences/audio/intro.mp3", "volume": 0.9}
```

| Field | Description |
|-------|-------------|
| `src` | Path to audio file relative to the tool root |
| `volume` | Playback volume (0–1) |

Place audio files in `sequences/audio/` and reference them by path. The `speak` action is for drafting; `audio` is for publishing.

---

## Volume guidelines

All volume values are on a 0–1 scale. These ranges work well in practice:

| Layer | Suggested range | Notes |
|-------|----------------|-------|
| Environmental | 0.3–0.6 | Foundation layer, can be relatively present |
| Noise | 0.1–0.25 | Should sit behind everything else |
| Harmonic | 0.3–0.5 | Singing bowl, OM, etc. — can be present but not dominant |
| Binaural | 0.1–0.2 | Keep low when voice is present — 0.15 is usually right |
| Voice (speak) | 0.85–1.0 | Should always be the clearest element |

---

## Timing patterns

### Layered entry (recommended opening)
```
t:0   env fades in over 8s
t:12  noise fades in over 10s
t:25  speak — welcome / orientation
t:50  harm fades in over 8s
t:65  speak — explain what they're hearing
t:90  binaural fades in over 15s
t:110 speak — explain the entrainment
```

### Clean exit (recommended closing)
```
t: duration - 60   binaural fades out over 20s
t: duration - 45   speak — closing words
t: duration - 30   noise fades to 0 over 20s
t: duration - 25   harm fades to 0 over 15s
t: duration - 20   stop_env over 20s
```

### State transition (mid-session)
```
t: 600   binaural — change beat from 10 to 6, fade carrier, label: "Descending to Theta..."
t: 605   speak — "Allow the rhythm to slow..."
t: 615   env — transition from ocean to wind over 20s
```

---

## Complete minimal example

A 10-minute ambient session with no binaural beats — just layered sound and occasional spoken guidance:

```json
{
  "id": "ambient_forest",
  "title": "Forest Ambient (10 min)",
  "duration": 600,
  "steps": [
    {"t": 0,   "action": "env",  "target": "rain",  "vol": 0, "fadeTo": 0.5, "fadeTime": 10, "label": "Rain fading in..."},
    {"t": 15,  "action": "noise","target": "pink",  "vol": 0, "fadeTo": 0.15,"fadeTime": 12},
    {"t": 30,  "action": "harm", "target": "bowl",  "vol": 0, "fadeTo": 0.4, "fadeTime": 8},
    {"t": 42,  "action": "speak","text": "Settle into the sound of rain. You have nowhere to be.",  "rate": 0.78, "pitch": 0.85},
    {"t": 180, "action": "speak","text": "Simply breathe. The bowl will mark the passage of time.", "rate": 0.76, "pitch": 0.85},
    {"t": 360, "action": "speak","text": "You are halfway through. Rest here as long as you need.", "rate": 0.76, "pitch": 0.85},
    {"t": 530, "action": "stop_harm", "target": "bowl", "fadeTime": 10},
    {"t": 545, "action": "speak","text": "The session is coming to a close. Take your time returning.", "rate": 0.74, "pitch": 0.83},
    {"t": 565, "action": "noise","target": "pink",  "fadeTo": 0, "fadeTime": 20},
    {"t": 575, "action": "stop_env", "fadeTime": 25}
  ]
}
```

---

## Tips and notes

**Steps are not blocking.** Multiple steps at the same `t` value all fire simultaneously. A `speak` step does not pause the timeline — the next step fires at its scheduled time regardless of whether the voice has finished speaking.

**Overlapping voices.** If a `speak` step fires while the previous utterance is still playing, the previous utterance is cancelled. Space your speak steps far enough apart to avoid this.

**The sequencer does not stop sounds automatically.** Always include explicit fade-out steps for everything you start. A clean exit is as important as a clean entry.

**Draft with Web Speech, publish with audio files.** The `speak` action is fast to iterate with and works immediately. When a sequence is ready to publish, render the voice lines with ElevenLabs, save them to `sequences/audio/`, and replace `speak` steps with `audio` steps.

**JSON must be valid.** A single missing comma or bracket will prevent the sequence from loading. Use a JSON validator (jsonlint.com or any code editor) before pushing to GitHub.

**The stop button always works.** The ◼ End Session button in the transport row cancels all running sequences and stops all sound immediately, regardless of where in the timeline the session is.

---

## Part of the Myathe Magick System

→ [Audio Shear Zone on GitHub](https://github.com/myathemagick-netizen/audio-shear-zone)
→ [Myathe Magick YouTube channel](https://youtube.com/@MyatheMagick)
