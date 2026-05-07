# Audio Shear Zone

**Myathe Magick System — Binaural Attunement Engine**

A full acoustic environment builder for consciousness-state attunement, built on the Web Audio API. No dependencies, no install — one standalone HTML file. Drop it in any static host or open it locally in a browser.

The tool has five independent sound layers plus two higher-level control systems:

- **Binaural tone generator** — the core entrainment engine
- **Noise color bed** — spectral texture and environmental masking
- **Environmental sounds** — immersive acoustic atmosphere
- **Resonant & harmonic tones** — tuned frequencies and rhythmic structures
- **Live Earth Sync** — real-time Schumann resonance and space weather attunement
- **Session presets** — 25 one-click configurations across five categories
- **Scripted programs** — timed sequences that automate layering, fading, and guided voice

All sound layers run simultaneously through their own gain controls. Session presets load a complete configuration in one click. Scripted programs run automated sessions — fading sounds in and out, delivering spoken guidance, and moving through a designed arc of experience.

→ [Live tool](https://myathemagick-netizen.github.io/audio-shear-zone/)

---

## Headphones

Headphones are required for the binaural beat engine. The illusory beat tone only arises when each ear receives its frequency in isolation — speakers deliver both tones to both ears and the effect collapses. The noise, environmental, and harmonic layers work fine on speakers.

---

## I. Binaural tone generator

### How it works

Two pure sine tones are delivered separately — one to each ear. The brain perceives the difference between them as a third, illusory tone. This is the binaural beat. It originates subcortically in the medial nucleus of the superior olivary complex, the first structure in the auditory pathway to receive input from both ears simultaneously, and propagates through the auditory cortex into broader neural networks. Through a mechanism called the frequency-following response, cortical oscillations tend to synchronize toward the difference frequency.

For example: left ear 200 Hz + right ear 210 Hz = a perceived beat of **10 Hz**.

Perceptual thresholds worth knowing:

- Below ~3 Hz: the beat is heard as a tone rotating from ear to ear
- 3–20 Hz: fluctuating loudness — the primary working range
- Above 20 Hz: begins to sound rough; above 30 Hz the two tones are perceived as separate

### Brainwave band map

| Band | Range | Associated states |
|------|-------|-------------------|
| **Delta** | 0.5–4 Hz | Deep dreamless sleep, physical restoration, deep repair |
| **Theta** | 4–8 Hz | Hypnagogic imagery, dream-logic, trance, creative incubation |
| **Alpha** | 8–12 Hz | Relaxed alertness, meditative onset, creative receptivity |
| **Beta** | 12–30 Hz | Focused cognition, working memory, active problem solving |
| **Gamma** | 30+ Hz | Neural binding, insight states, heightened awareness |

The band map at the bottom of the controls updates in real time as you move the beat frequency slider. The **Schumann Resonance** preset (7.83 Hz) sits at the theta-alpha boundary and corresponds to the Earth's own electromagnetic resonance frequency.

### Carrier frequency and the Solfeggio presets

The carrier (base tone) shapes the timbre and comfort of the session. It also affects how clearly the brain perceives the beat — Gerald Oster's research (1973, *Scientific American*) produced the **Oster Curve**, showing which carrier frequencies produce the most perceptible binaural beats at a given target frequency:

- Theta targets (4–8 Hz): carrier 160–210 Hz range is optimal
- Alpha targets (~10 Hz): carrier 230–240 Hz range is optimal
- General comfortable range for long sessions: 200–500 Hz

Lower carriers feel warmer and more grounding; higher carriers are brighter and more activating.

The sidebar includes ten Solfeggio carrier presets. Selecting one sets the base tone while leaving the beat frequency unchanged, so you can combine any brainwave target with any sacred carrier:

| Frequency | Traditional association |
|-----------|------------------------|
| 174 Hz | Grounding, foundation |
| 285 Hz | Tissue and field influence |
| 396 Hz | Release of guilt / fear → joy |
| 417 Hz | Change, undoing stagnation |
| 432 Hz | Natural tuning, earth alignment |
| 528 Hz | Transformation, the "miracle tone" |
| 639 Hz | Connection, relational healing |
| 741 Hz | Expression, problem solving |
| 852 Hz | Intuition, return to order |
| 963 Hz | Crown, unity states |

### Schumann sweep

The sweep button snaps the beat frequency to 4 Hz and begins oscillating it slowly between 4–12 Hz, cycling through the theta-alpha boundary. This is the classic threshold zone for trance, creative incubation, and hypnagogic entry. When you stop the sweep it returns to whatever beat frequency you had set before engaging it.

---

## II. Noise colors

All six noise types are algorithmically generated from the Web Audio API — no audio files. They can run independently of the binaural tones. Only one noise color can be active at a time. Volume is controlled separately.

| Color | Character | Good for |
|-------|-----------|----------|
| **White** | All frequencies at equal amplitude — bright, present, full | Short masking sessions, focus |
| **Pink** | Equal energy per octave — softer than white, more natural | Long sessions, general use, layering |
| **Brown** | Energy concentrated in low frequencies — deep, warm, cave-like | Delta/theta work, sleep, grounding |
| **Blue** | Emphasis on high frequencies — airy, bright, crystalline | Clarity, Beta/Gamma states |
| **Violet** | Extreme high-frequency emphasis — near-white hiss | Tinnitus masking, very short use |
| **Grey** | Psychoacoustically "flat" — tuned to the equal-loudness contour of human hearing | Neutral background, fatigue reduction |

**Pink noise** is the most widely used for binaural beat sessions — its octave-balanced spectrum sits naturally behind the tones without competing with them. **Brown noise** pairs well with deep delta/theta work and adds a grounding texture. **Grey noise** is the most perceptually neutral choice for extended listening.

---

## III. Environmental sounds

Algorithmic sound environments built from filtered noise and oscillators. All are generated in real time — no samples. Only one environmental sound can be active at a time. Volume is controlled separately from noise and harmonics.

| Sound | How it's built | Character |
|-------|---------------|-----------|
| **Rain** | Bandpass-filtered white noise | Steady, consistent; good general masking |
| **Ocean** | Brown noise with 0.12 Hz tidal amplitude modulation | Slow breath rhythm; good for theta/delta |
| **Wind** | Lowpass noise with a slow LFO sweeping the filter cutoff | Drifting, shifting; good for trance work |
| **Fire** | Brown noise with randomized crackle transients | Warm, irregular; grounding and present |
| **Thunder** | Very deep brown noise with 0.04 Hz slow tremolo | Subsonic rumble; pairs with delta states |
| **Cave** | Sustained 55 Hz + 110 Hz tones with ultra-slow wobble | Deep resonant hum; strong grounding effect |

Environmental sounds work well on speakers and can be used as standalone ambience without the binaural layer engaged.

---

## IV. Resonant & harmonic tones

Unlike noise and environmental sounds, multiple harmonic tones can be active simultaneously — stack them freely. Volume is controlled by a single shared slider.

| Sound | How it works | Notes |
|-------|-------------|-------|
| **Drone** | Filtered sawtooth wave locked to the current carrier frequency | Updates if you change the carrier; harmonically tied to the binaural tones |
| **Singing Bowl** | Sine wave with sharp attack and 4.5-second exponential decay, auto-striking every 5.5 seconds | Mimics a bowed or struck singing bowl; re-excites itself continuously |
| **OM Pulse** | 136.1 Hz sine tone (the traditional OM fundamental) with slow breathing amplitude envelope | Can run alone as a room tone independent of the binaural carrier |
| **Isochronic** | Rhythmic on/off gating of a sine tone at the current beat frequency | A different entrainment mechanism from binaural beats — works without headphones; updates automatically if you change the beat frequency |
| **Heartbeat** | Dual low-frequency thumps (~70 bpm) mimicking the lub-dub of a heartbeat | Particularly effective for deep delta sessions; grounding and primal |
| **Wind Wand** | Fundamental (220 Hz) plus 3rd, 5th, and 7th harmonics, with pitch modulated by a sinusoidal spin-speed envelope | See below |

### Wind wand

The wind wand (also called a singing rod or bullroarer in various traditions) produces sound through rotation — the pitch rises as it speeds up and falls as it slows. The algorithmic version models this with:

- A pure odd-harmonic series (fundamental + 3rd + 5th + 7th) as the tonal source
- A sinusoidal spin-speed envelope that slowly accelerates and decelerates
- Doppler-like frequency modulation that rises and falls with the spin cycle
- Subtle amplitude shimmer at a slightly different rate from the pitch modulation

The **Wand speed** slider controls the rate of the spin cycle — slow values produce long lazy sweeps, high values produce rapid spinning. A small waveform display appears showing the current pitch modulation state.

The wind wand can run independently of the binaural layer, or alongside it — the odd-harmonic spectrum sits in a frequency range that generally does not interfere with the binaural carrier tones.

---

## V. Live Earth Sync — Schumann Resonance

The Live Earth Sync panel connects the tool to real-time planetary electromagnetic data, allowing you to tune the binaural beat frequency to the live state of the Earth-ionosphere cavity rather than a fixed preset value.

### What the Schumann resonance is

The Schumann resonances are standing electromagnetic waves in the cavity between the Earth's surface and the ionosphere, sustained continuously by global lightning activity — roughly 40–50 lightning strikes per second worldwide. The fundamental mode sits at approximately 7.83 Hz, with harmonics at 14.3, 20.8, 27.3, and 33.8 Hz. These are not fixed values — they drift with solar activity, geomagnetic conditions, and the daily rotation of the three major lightning centers (Africa, South America, Southeast Asia). The frequency typically varies within ±0.5 Hz of the baseline fundamental; the amplitude can spike dramatically during geomagnetic storms.

This is not a static number to meditate to. It is a living signal reflecting the electromagnetic state of the planet in real time.

### How the panel works

**Stable baseline tiles (SR1–SR5)** — the five Schumann harmonic modes displayed as fixed reference values. SR1 (7.83 Hz) and SR2 (14.3 Hz) fall within binaural beat perception range and lock the beat frequency when clicked. SR3, SR4, and SR5 (20.8, 27.3, 33.8 Hz) fall above the binaural threshold — clicking them sets the *carrier* frequency instead, which is a musically and physically meaningful use of those harmonics even though they cannot drive the beat engine directly.

**Live SR1 value** — fetched from NOAA's space weather service and estimated from current geomagnetic conditions. After fetching, this shows a value like `7.71 Hz (est from Kp 2.3)` — the small drift from 7.83 is derived from the live Kp index and a time-of-day modulation based on the known daily cycle of the resonance. Click **Lock live SR1 to beat** to engage this value as the binaural beat frequency. If auto-refresh is enabled, the beat will drift slowly as the live value updates every five minutes.

**Manual entry** — if live fetch is unavailable or you want to use a value you've read directly from a monitoring source, enter it in the manual field and click Set & lock. This engages the same live-lock mechanism as the fetched value.

**Auto-refresh** — when enabled, the tool polls NOAA every five minutes and updates the live SR1 estimate and space weather display automatically. If the live lock is engaged, the binaural beat frequency will drift gently with the planet.

### Space weather data displayed

| Field | Source | Notes |
|-------|--------|-------|
| **Kp Index (3hr)** | NOAA SWPC | Global geomagnetic activity index, 0–9 scale. Updated every 3 hours — may show `3hr delay` between updates. |
| **Solar Wind km/s** | NOAA ACE/DSCOVR satellite | Updates every ~minute. Speed spikes indicate increased ionospheric pressure. |
| **IMF Bt (nT)** | NOAA ACE/DSCOVR satellite | Interplanetary magnetic field strength in nanoTeslas. |
| **Field State** | Derived from Kp | Quiet / Unsettled / Active / Storm. Defaults to `Quiet*` if Kp is between update cycles. |

**Kp and what it means for your session:** a Kp of 0–2 is quiet, baseline conditions — the resonance is stable and amplitude bars show typical values. Kp 3–4 is unsettled — some elevation across harmonics, the higher modes become more active. Kp 5+ is geomagnetic storm territory — significant ionospheric disturbance, SR amplitude can spike substantially, and the resonance becomes more variable. These are also the moments considered most significant for planetary-scale attunement work.

### For precise live amplitude data

NOAA's public API provides frequency drift estimates but not live SR amplitude. For real-time amplitude monitoring, cross-reference:

- [HeartMath Global Coherence Initiative](https://www.heartmath.org/gci/gcms/live-data/) — global magnetometer network, live SR amplitude charts
- [schumannresonance.today](https://schumannresonance.today) — aggregated live SR data with frequency and amplitude display
- [Tomsk State University spectrogram](http://sosrff.tsu.ru/) — raw spectrogram from Siberian monitoring station

Read the current SR1 value from any of these and enter it manually for maximum precision.

---

## Combining layers

Some combinations that work well:

**Deep trance / delta session** — Delta I or II preset + 174 Hz carrier + Ocean or Thunder env + Heartbeat harmonic. The tidal modulation of the ocean and the heartbeat create a layered biological rhythm structure around the entrainment target.

**Theta creative incubation** — Schumann preset + 285 Hz carrier + Wind env + OM Pulse harmonic. The slow wind filter sweep and the breathing OM create a living acoustic container around the earth-resonance frequency.

**Alpha focus session** — Alpha I + 432 Hz carrier + Pink noise + Drone. The drone locks harmonically to the carrier and the pink noise provides neutral masking without fatigue.

**Ceremonial / ritual** — Any theta preset + 528 Hz carrier + Singing Bowl + Wind Wand. The bowl's recurring decay and the wand's spinning pitch modulation create an acoustic environment with strong esoteric character.

**Isochronic + binaural stacking** — Isochronic and binaural beats are different entrainment mechanisms that reinforce each other. Isochronic pulses work through direct rhythmic neural entrainment and do not require headphones; binaural beats work through the frequency-following response and require stereo separation. Running both simultaneously at the same beat frequency produces a layered entrainment signal.

**Live planetary session** — Fetch live space weather, lock live SR1 to beat, enable auto-refresh, set carrier to 285 Hz or 396 Hz, add Pink noise and Cave or Ocean environment. The beat frequency will drift slowly with the planet's actual electromagnetic state over the course of the session. During high-Kp events the amplitude bars will show elevated harmonic activity across SR3–SR5 — consider clicking SR3 to also shift the carrier toward 20.8 Hz, placing the entire session within the live harmonic structure of the resonance.

---


## Session presets

The **Session Preset** dropdown at the top of the tool loads a complete configuration — beat frequency, carrier, noise color, environmental sound, and harmonic layers — in one click. The tone starts automatically. A description of each preset appears below the dropdown when selected.

Presets are organized into five categories:

**Crystal Path / Chakra** — seven presets ascending the vertical axis from Logos/Shadow/Root at delta through Chaos/Spirit/Crown at high beta. Beat frequency climbs steadily from 0.5 Hz at the base to 28 Hz at the crown; carrier follows the Solfeggio sequence from 396 Hz to 963 Hz. Each preset has its own noise color, environmental sound, and harmonic character matched to the principle it represents.

**Gateway Tapes** — four presets mapped to Monroe Institute Focus Levels 10, 12, 15, and 21. Each follows the acoustic structure documented in the declassified CIA analysis: OM Pulse as the resonant tuning layer, pink noise bed, binaural tone at the appropriate frequency for that Focus Level. See the Gateway Tapes section below for full details.

**Combining Layers** — the five session recipes from the Combining Layers section below, available as one-click presets: Deep Trance, Theta Incubation, Alpha Focus, Ceremonial/Ritual, and Isochronic Stack.

**General** — six broadly useful configurations: Deep Sleep, Lucid Dream Entry, Creative Flow, Sharp Focus, Grounding, and Stress Release.

**Live Earth** — two presets designed around the Live Earth Sync panel: Schumann Baseline (SR1 locked, cave environment, OM pulse) and Planetary Storm Mode (for high-Kp geomagnetic events — fetch live data and lock SR1 first for full effect).

The **◼ End Session** button in the transport row stops all sound immediately regardless of what is active — useful if a session becomes overwhelming or you simply want silence.

---
## Gateway Tapes configurations

The Monroe Institute's Gateway Experience (1970s–present) is the most thoroughly documented audio-based consciousness research program, including a declassified 1983 CIA analysis. Monroe's Hemi-Sync technology is structurally identical to binaural beats — two tones, one per ear, difference frequency as the entrainment target — layered with pink and white noise and guided voice. The Focus Level system maps directly onto the brainwave bands used in this tool.

### Monroe's Focus Level system

| Focus Level | Description | Brainwave equivalent |
|-------------|-------------|----------------------|
| **Focus 10** | Mind Awake / Body Asleep — foundational altered state | Alpha (8–12 Hz) |
| **Focus 12** | Expanded Awareness — deep meditation, internal imagery | Theta (4–8 Hz) |
| **Focus 15** | No Time — dissolution of linear time sense | Deep Theta (4–6 Hz) |
| **Focus 21** | The Bridge — edge of time-space perception | Theta/Delta boundary |
| **Focus 27+** | Non-physical realities, expanded contact states | Delta + harmonics |

Monroe's documented carrier frequency was approximately 400 Hz for Alpha-level work, making 396 Hz or 417 Hz from the Solfeggio grid the closest available presets.

The acoustic structure of the original tapes, as described in the declassified CIA document, followed a specific sequence: first a **resonant tuning** step where the listener hums a sustained tone alongside a recorded chorus to bring mind and body into pre-entrainment resonance, then Hemi-Sync binaural tones introduced gradually, then pink and white noise added as a bed beneath the tones. This exact structure is reproducible in this tool — run OM Pulse first, then engage the binaural tone, then add Pink noise.

### Recommended configurations by Focus Level

**Focus 10 — Mind Awake / Body Asleep**
- Beat: Alpha I (10 Hz)
- Carrier: 396 Hz or 417 Hz (closest to Monroe's ~400 Hz)
- Harmonic: OM Pulse first (resonant tuning step), then leave running
- Noise: Pink at low volume
- Environmental: Cave (isolation tank acoustic context) or none

**Focus 12 — Expanded Awareness**
- Beat: Theta II (6 Hz) or Schumann Sweep (cycles through the exact theta-alpha boundary the tapes are designed to cross)
- Carrier: 285 Hz or 396 Hz
- Harmonic: OM Pulse + Singing Bowl (the bowl's cycling decay mimics the recurring tonal structures of the tapes)
- Noise: Pink at low-to-medium volume
- Environmental: none, or Cave very quietly

**Focus 15 — No Time**
- Beat: Theta I (4 Hz)
- Carrier: 285 Hz
- Harmonic: OM Pulse + Drone
- Noise: Pink fading into Brown
- Environmental: Ocean (the slow tidal breath rhythm reinforces the dissolution of linear time sense)

**Focus 21 and beyond — The Bridge**
- Beat: Delta II (2 Hz) or Delta I (0.5 Hz)
- Carrier: 174 Hz (lowest grounding carrier)
- Harmonic: Drone + Heartbeat (the heartbeat provides a biological anchor at the deepest states; Monroe explicitly used pulse-like rhythms at the lower Focus Levels)
- Noise: Brown
- Environmental: Thunder very quietly (subsonic rumble consistent with isolation room conditions)

### Notes on the Monroe approach

The Gateway tapes are not just a sound file — they are a complete system with visualization techniques, breathing practices, and structured intention-setting before audio begins. The "Energy Conversion Box" is Monroe's method for mentally setting aside external concerns before a session; the resonant humming step is a physiological preparation, not decoration. Replicating the acoustic structure without the preparatory framework will produce a different (not necessarily lesser) experience.

Monroe's later research expanded beyond standard binaural beats into amplitude modulation, phase modulation, and spatial audio techniques. The modern Hemi-Sync product line is considerably more sophisticated than the original tapes and incorporates over 50 variations of audio entrainment technology.

The CIA's 1983 analysis ("Analysis and Assessment of the Gateway Process," Lt. Col. Wayne McDonnell) is publicly available via the National Archives and worth reading as a primary source — it is a serious attempt to understand the neurophysiological and quantum-mechanical basis of the technique, written by someone who had not previously encountered it and was trying to assess its intelligence applications.

---

## VI. Scripted programs

The **⟐ Program** dropdown (visible when a `sequences/` folder is present in the repository) runs timed sessions that automate everything — fading layers in and out, adjusting volumes, triggering spoken guidance, and moving through a designed arc of experience over a set duration.

### How programs work

A program is a JSON file in the `sequences/` folder. It contains a list of steps, each with a timestamp (in seconds from session start) and an action. When you press Run, the sequencer fires each step at its scheduled time. A progress bar tracks the session. The ◼ End Session button cancels the program and stops all sound at any point.

Programs can control any layer the tool supports:

- **env** — start an environmental sound, fade its volume in or out
- **noise** — start a noise color, fade its volume
- **harm** — start a harmonic layer, fade the harmonic bus
- **binaural** — set beat and carrier frequencies, fade the tone in or out
- **speak** — deliver spoken guidance via the browser's built-in speech synthesis
- **audio** — play a pre-rendered audio file (for ElevenLabs voice or field recordings)
- **stop_env / stop_harm** — gracefully fade out and stop a layer

Steps are not blocking — multiple steps at the same timestamp fire simultaneously, and a speak step does not pause the timeline. The sequencer is designed so that binaural tones, environmental sounds, and spoken guidance can all be layered with precise timing.

### Guided voice

The `speak` action uses the Web Speech API built into every modern browser — no external service, no audio files, works immediately. Rate and pitch are controllable; slowing the rate to 0.75–0.82 and lowering pitch to 0.85–0.88 produces a more grounded, meditative delivery.

For production quality, render voice lines with ElevenLabs or any text-to-speech tool, save them to `sequences/audio/`, and reference them with the `audio` action instead. The JSON structure is otherwise identical — swap `speak` for `audio` when moving from draft to published.

### Available programs

Programs appear in the dropdown automatically when listed in `sequences/manifest.json`. The included program is:

**Introduction to the Audio Shear Zone (5 min)** — an onboarding sequence for first-time users. Ocean environment fades in, followed by pink noise, OM pulse, and a binaural tone at Alpha I. Spoken guidance explains each layer as it arrives. Everything fades out cleanly at the end. Designed to orient a new listener to what each element of the tool is and does, before they begin exploring on their own.

### Writing your own programs

See **`sequences/SCRIPTING.md`** for the complete sequence authoring guide — full reference for all action types, volume guidelines, timing patterns, and a complete minimal example. Writing a sequence requires only a text editor and basic familiarity with JSON.

---
## Best practices

**Start with pink or brown noise at low volume** before bringing in the binaural tones. It gives your auditory system something to settle into before the entrainment begins.

**Match the carrier to the target.** For deep delta/theta work, lower carriers (174–285 Hz) feel more congruent. For alpha/beta states, mid carriers (396–528 Hz) work well.

**Set an intention before engaging.** The tool is a carrier of attention, not a replacement for it.

**Session length.** Twenty minutes is a reasonable minimum for reaching a stable entrained state. Theta work often takes 10–15 minutes to onset. Delta targets should generally be used for sleep or deep rest rather than timed sessions.

**Do not use while driving or operating machinery. Not a medical device.**

---

## Notes on the science

EEG studies confirm that the brain produces a frequency-following response to binaural difference tones. Whether this reliably shifts associated cognitive or consciousness states — and to what degree — varies by individual, session length, and context. The effect is real at the neurological level; the downstream subjective outcomes are not guaranteed.

The Solfeggio carrier frequencies are drawn from esoteric tradition. Their specific healing properties are not established in peer-reviewed literature. They are included here as tools for intentional attunement within the Myathe Magick System framework, not as medical claims.

The Schumann resonance data is real geophysical data from NOAA's Space Weather Prediction Center. The live SR1 frequency estimate is derived from the Kp index and known daily variation patterns — it is an approximation, not a direct SR measurement. For precise amplitude data, use the HeartMath GCI or Tomsk monitoring links provided in the tool.

---

## Repository structure

```
audio-shear-zone/
├── index.html              ← the entire tool — one standalone file
└── sequences/
    ├── manifest.json       ← lists available programs
    ├── SCRIPTING.md        ← sequence authoring guide
    ├── onboarding.json     ← included onboarding program
    └── audio/              ← place pre-rendered voice MP3s here
```

The tool works as a single `index.html` file without the `sequences/` folder. The Programs dropdown only appears when `sequences/manifest.json` is found. No build step, no dependencies, no server required beyond basic static file hosting.

---
## Part of the Myathe Magick System

This tool is one node in a suite of interactive research and attunement applications developed alongside the Myathe Magick System — a comprehensive theoretical framework synthesizing torsion field physics, sacred geometry, Kabbalistic cosmology, chaos magick, Mayan cosmology, Jungian psychology, mycorrhizal biology, and archaeoastronomy.

→ [Myathe Magick YouTube channel](https://youtube.com/@MyatheMagick)
