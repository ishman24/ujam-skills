# UJAM Virtual Guitarist CARBON - Complete MIDI & Parameter Map

> Reference Standard: **C3 = MIDI note 60** (Yamaha standard, as specified in UJAM documentation).
> Note: Some DAWs (e.g., FL Studio or standard Roland notation) refer to MIDI 60 as C4. In all MorningDAW MCP tool calls, use the exact **MIDI Note Number (0–127)**.

---

## 1. Global Note Range Overview

| Keyboard Zone | Key Name Range (C3=60) | MIDI Note Range | Role in PLAYER Mode | Role in INSTRUMENT Mode |
| :--- | :--- | :--- | :--- | :--- |
| **Marker / Meta** | C-2 | 0 | Internal dropped phrase marker | Internal dropped phrase marker |
| **Common Phrases / Articulations** | C1 – F2 | 36 – 53 | Hardwired Common Phrases & Shreds | Note Articulations & Legato Controls |
| **Style Phrases / Repetitions** | F#2 – E3 | 54 – 64 | Style-specific Phrases (11 phrases) | Shreds & 2-bar Repetition engines |
| **Stop Key** | F3 | 65 | Stops playback (in Latch mode) | Repetitions (16ths, 2 bars) |
| **PLAY RANGE (Pitches)** | **F#3 – F#6** | **66 – 102** | **Musical Notes** (Sounds F#1–F#4) | **Musical Notes** (Sounds F#1–F#4) |

> **CRITICAL**: The Play Range is placed high on the MIDI keyboard (**F#3 to F#6, notes 66–102**) to make room for articulations/phrases below, but Virtual Guitarist CARBON sounds **almost an octave lower than a standard guitar** (tuned to low F# on an 8-string). Notes played at MIDI 66 sound at F#1 (~46.25 Hz)!

---

## 2. PLAYER Mode MIDI Reference

In Player mode, Virtual Guitarist CARBON handles rhythm, picking technique, and strumming patterns. Your MIDI track must send:
1. **Left-Hand Control Keys (36–64)**: Select phrase/groove.
2. **Right-Hand Note Keys (66–102)**: Set harmonic pitches (up to 4-voice polyphony).

### Common Phrases (Hard-wired across ALL styles)
| Note Name | MIDI # | Category | Description & Behavior |
| :--- | :--- | :--- | :--- |
| **C1** | **36** | **Silence** | Keeps rhythm engine running synchronously in total silence (ideal for breaks/rests) |
| **C#1** | **37** | **Ending** | Plays an open 1/1 whole-note sustain ring-out and stops the player |
| **D1** | **38** | Rhythmic | Open 1/4 notes |
| **D#1** | **39** | **Ending** | Plays a muted 1/1 whole-note stop and stops the player |
| **E1** | **40** | Rhythmic | Muted 1/4 notes |
| **F1** | **41** | Rhythmic | Open 1/8 notes |
| **F#1** | **42** | **Shred** | Open 1/32 notes (temporary burst, held for desired duration) |
| **G1** | **43** | Rhythmic | Muted 1/8 notes |
| **G#1** | **44** | **Shred** | Half Muted 1/32 notes |
| **A1** | **45** | Rhythmic | Open 1/16 notes |
| **A#1** | **46** | **Shred** | Full Muted 1/32 notes |
| **B1** | **47** | Rhythmic | Muted 1/16 notes |
| **C2** | **48** | Chug | Wuggeda 1 (classic driving heavy chug pattern) |
| **C#2** | **49** | **Shred** | Moderate Muted 1/16 Triads (Triplets) |
| **D2** | **50** | Chug | Wuggeda 2 |
| **D#2** | **51** | **Shred** | Full Muted 1/16 Triads (Triplets) |
| **E2** | **52** | Chug | Wuggeda 3 |
| **F2** | **53** | Chug | Wuggeda 4 |

### Style Phrases (Dependent on loaded Style)
| Note Name | MIDI # | Role | Typical Behavior |
| :--- | :--- | :--- | :--- |
| **F#2 – E3** | **54 – 64** | Style Phrases | 11 phrases per style. White keys scale in rhythmic density and intensity from low to high. Black keys provide style-specific syncopations, fills, and riffs. |
| **F3** | **65** | **STOP** | Halts playback immediately when in Latch mode. |

### Pitch Input / Play Range (Player Mode)
| Note Name | MIDI # | Mode Selector | Description |
| :--- | :--- | :--- | :--- |
| **F#3 – F#6** | **66 – 102** | **Single Mode** | Monophonic melodic riffs; legato enabled; automatic slides up to 1 whole tone; hammer-ons/pull-offs via velocity. |
| **F#3 – F#6** | **66 – 102** | **Chords Mode** | Polyphonic (up to 4 voices). Ideal for power chords, octaves, and dyads. Legato disabled. |

---

## 3. INSTRUMENT Mode MIDI Reference

In Instrument mode, you control every single note attack and articulation individually, turning CARBON into a direct virtual guitar instrument.

### Articulation Control Keys
| Note Name | MIDI # | Type | Action / Articulation |
| :--- | :--- | :--- | :--- |
| **C#2** | **49** | Switch | **Legato OFF** (clean chord/interval triggers down to semitones) |
| **D#2** | **51** | Switch | **Legato ON** (expressive slides up to whole tone, hammer-ons/pull-offs) |
| **F2** | **53** | Note Type | **Dead Notes** (unpitched, percussive string chugs & rhythmic mutes) |
| **F#2** | **54** | Shred | 32th Moderate Mutes (super-fast picked stream while held) |
| **G2** | **55** | Note Type | **Full Mutes** (tight, short palm mutes - quintessential djent/metal chug) |
| **G#2** | **56** | Shred | 32th Half Mutes |
| **A2** | **57** | Note Type | **Half Mutes** (medium damped, chunky & punchy) |
| **A#2** | **58** | Shred | 32th Full Mutes |
| **B2** | **59** | Note Type | **Long Mutes** (lightly damped, sustained body) |
| **C3** | **60** | Note Type | **Sustains** (fully open, ringing power chords and lead notes) |
| **C#3** | **61** | Shred | 16T Half Mutes (1/16 note triplet shred) |
| **D3** | **62** | Repetition | **4ths Repetitions** (auto-plays 2 bars of quarter notes legato) |
| **D#3** | **63** | Shred | 16T Full Mutes (1/16 note triplet shred) |
| **E3** | **64** | Repetition | **8ths Repetitions** (auto-plays 2 bars of eighth notes legato) |
| **F3** | **65** | Repetition | **16ths Repetitions** (auto-plays 2 bars of sixteenth notes legato) |

### Play Range (Instrument Mode)
| Note Name | MIDI # | Voices | Behavior |
| :--- | :--- | :--- | :--- |
| **F#3 – F#6** | **66 – 102** | Up to 4 | Direct pitch execution, velocity-sensitive. When Legato is ON, overlapping notes create guitar slides and transitions. |

### Guitar-Style Playing Mode (Easter Egg)
1. Turn **Latch ON** in Instrument Mode.
2. Hold pitch chord/note in the **Play Range (66–102)** with your right hand (fretting).
3. Tap the **Articulation Keys (53–60)** with your left hand to rhythmically strum/pick the strings!

---

## 4. Real-time Continuous Controllers & Automation

| Controller | Control Name | Function & Tips |
| :--- | :--- | :--- |
| **Pitchbend** | Pitch Bend Wheel | Bends pitch ±1 whole tone (±2 semitones). Perfect for subtle vibrato, dive-bombs, or heavy bends. |
| **CC#1** | **Modulation Wheel** | **Hardwired to the FINISHER Knob**. Directly morphs the 20-effect Finisher rack from subtle to maximum sonic distortion/delay/filtering. |
| **CC#64** | Sustain Pedal | Temporary Latch. Releasing pedal releases notes that are not physically held. |
| **Automation** | **Severity** | Amp distortion gain (ranges 0 to 666). Past 2 o'clock enters high-saturation "insane" territory. |
| **Automation** | **Condition** | Amp model selector: `Paranoid` (warm/fuzz) -> `Disturbed` (punchy rock) -> `Insane` (modern hi-gain) -> `Rabid` (cutting metal) -> `Lobotomized` (crushing destruction). |
| **Automation** | **Focus** | 4-position morphing EQ: 7 o'clock = Bass Boost, 9 = Low Mid Boost, 12 = Neutral, 3 = Hi Mid Boost ("twang"), 5 = Hi Range Boost. |
| **Automation** | **Filter** | 24dB Bi-directional Synthesizer Filter. Turn left for Resonant Lowpass, turn right for Resonant Highpass. Essential for intros/risers. |
| **Automation** | **Layerer** | Multi-tracking configuration: `Single` (1 guitar center), `Double` (L/R hard pan), `Triple` (Center + L/R), `Quadro` (4 guitars across stereo stage). Parameters: `Spread` (stereo width), `Distance` (depth/room reverb), `Separation` (spectral un-masking EQ). |
