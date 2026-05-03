# Audio Shear Zone

**Myathe Magick System — Binaural Attunement Engine**

A full acoustic environment builder for consciousness-state attunement, built on the Web Audio API. No dependencies, no install — one standalone HTML file. Drop it in any static host or open it locally in a browser.

The tool has four independent layers that can be used together or separately:

- **Binaural tone generator** — the core entrainment engine
- **Noise color bed** — spectral texture and environmental masking
- **Environmental sounds** — immersive acoustic atmosphere
- **Resonant & harmonic tones** — tuned frequencies and rhythmic structures

All four layers run simultaneously through their own gain controls, so you can build up a full layered session or strip it back to a single element.

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

## Combining layers

Some combinations that work well:

**Deep trance / delta session** — Delta I or II preset + 174 Hz carrier + Ocean or Thunder env + Heartbeat harmonic. The tidal modulation of the ocean and the heartbeat create a layered biological rhythm structure around the entrainment target.

**Theta creative incubation** — Schumann preset + 285 Hz carrier + Wind env + OM Pulse harmonic. The slow wind filter sweep and the breathing OM create a living acoustic container around the earth-resonance frequency.

**Alpha focus session** — Alpha I + 432 Hz carrier + Pink noise + Drone. The drone locks harmonically to the carrier and the pink noise provides neutral masking without fatigue.

**Ceremonial / ritual** — Any theta preset + 528 Hz carrier + Singing Bowl + Wind Wand. The bowl's recurring decay and the wand's spinning pitch modulation create an acoustic environment with strong esoteric character.

**Isochronic + binaural stacking** — Isochronic and binaural beats are different entrainment mechanisms that reinforce each other. Isochronic pulses work through direct rhythmic neural entrainment and do not require headphones; binaural beats work through the frequency-following response and require stereo separation. Running both simultaneously at the same beat frequency produces a layered entrainment signal.

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

---

## Part of the Myathe Magick System

This tool is one node in a suite of interactive research and attunement applications developed alongside the Myathe Magick System — a comprehensive theoretical framework synthesizing torsion field physics, sacred geometry, Kabbalistic cosmology, chaos magick, Mayan cosmology, Jungian psychology, mycorrhizal biology, and archaeoastronomy.

→ [Myathe Magick YouTube channel](https://www.youtube.com/channel/UClWbNxQMrx-XB3h8xXh_oxQ)
