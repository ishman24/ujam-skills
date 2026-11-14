# UJAM Virtual Bassist - Bassline Composition & Programming Guide

This guide details best practices for programming musical, pocket-tight, and expressive basslines using **UJAM Virtual Bassist** in MorningDAW.

---

## 1. Harmonic Intelligence: Melodic Mode vs. Melodic Mode OFF

Virtual Bassist features a dedicated harmonic intelligence engine designed to play realistic walking lines, pentatonic riffs, and scale runs.

### A. Melodic Mode ON (The Session Bassist Approach)
- **When to use**: When you want the virtual player to embellish the chord progression with authentic bass riffs, passing tones, and dynamic fills.
- **How it works**:
  1. Hold a chord or root note in the **Play Range (C3 to C6 / MIDI 60–96)**.
  2. Set the **KEY** parameter in the plugin UI to match your song's key signature (e.g. C Minor, F Major).
  3. The engine uses both the **current chord** AND the **overall song KEY** to choose passage notes that harmonize perfectly without chromatic dissonance.
- **Automation Tip**: If your song modulates to a new key in the bridge, automate the **KEY** parameter in your DAW!

### B. Melodic Mode OFF (The Precise Rhythmic Arranger)
- **When to use**: When you have composed exact bass notes or root movements and only want Virtual Bassist to provide the rhythmic groove, velocity feel, and physical damping.
- **How it works**:
  - The player will play *strictly* the pitch you hold in the Play Range, applying the rhythmic timing and articulations of the active Style phrase.

---

## 2. Supported Chord Types (Play Range C3+)

When Melodic Mode is ON, Virtual Bassist detects 14 chord structures from single notes to multi-note voicings:

| Chord Type | Example in C | Notes to Send (Play Range) |
| :--- | :--- | :--- |
| **Power 5th** | `C (5th)` | `C3 (60), G3 (67)` |
| **Major** | `Cmaj` | `C3 (60), E3 (64), G3 (67)` |
| **Minor** | `Cmin` | `C3 (60), Eb3 (63), G3 (67)` |
| **Dominant 7th** | `C7th` | `C3 (60), E3 (64), G3 (67), Bb3 (70)` |
| **Major 7th** | `Cmaj7`| `C3 (60), E3 (64), G3 (67), B3 (71)` |
| **Minor 7th** | `Cmin7`| `C3 (60), Eb3 (63), G3 (67), Bb3 (70)` |
| **Diminished** | `Cdim` | `C3 (60), Eb3 (63), F#3 (66)` |
| **Half-Diminished**| `Cm7b5`| `C3 (60), Eb3 (63), F#3 (66), Bb3 (70)` |
| **Augmented** | `Caug` | `C3 (60), E3 (64), G#3 (68)` |
| **Sus 2** | `Csus2`| `C3 (60), D3 (62), G3 (67)` |
| **Sus 4** | `Csus4`| `C3 (60), F3 (65), G3 (67)` |
| **Sixth** | `C6th` | `C3 (60), E3 (64), G3 (67), A3 (69)` |
| **Minor 6th** | `Cmin6`| `C3 (60), Eb3 (63), G3 (67), A3 (69)` |
| **Minor Major 7** | `CmMaj7`| `C3 (60), Eb3 (63), G3 (67), B3 (71)` |

---

## 3. Instrument Mode Programming Rules (Physical Bass Modeling)

When writing note-by-note basslines in **Instrument Mode**, leverage the physical engine rules:

### A. The 4-Semitone Polyphony Rule
- Intervals **between 1 and 4 semitones** are treated as fret movements on the *same string* (monophonic).
- Intervals **greater than 4 semitones** trigger a new note on a *different string*, allowing polyphonic double-stops and chords (up to 4 voices).

### B. Dynamic Articulations via Velocity & Pitch
- **Slide**: Trigger a note 1–2 semitones away with **higher velocity** than the preceding note.
- **Hammer-On**: Trigger a note 1–2 semitones higher with **lower velocity**.
- **Pull-Off**: Trigger a note 1–2 semitones lower with **lower velocity**.
- **Forced Slides (Intro Slides)**: Hold one of the slide keys in **C0 to E0 (MIDI 24–28)**, then play the target note in the Play Range.

### C. Ghost Notes & Slaps (Dead Notes)
- To create a tight, percussive pocket:
  - Place a **Dead Note (`A0` = 33 or `B0` = 35)** on the 16th-note immediately before a primary downbeat (e.g. at beat 1.75 before beat 2.0).
  - Use **Full Stop (`Bb0` = 34)** on the "and" of beat 4 to create a crisp acoustic string choke before a breakdown.

---

## 4. Micro Timing & Groove Pocket

Inside the **Micro Timing** menu:
- **Speed**: `0.5x` (Half-Time), `1.0x` (Normal), `2.0x` (Double-Time).
- **Feel (Push / Pull)**:
  - Left of center: plays off-beats slightly *ahead* of the beat (driving, energetic, rushing).
  - Right of center: plays off-beats slightly *behind* the beat (laid-back, lazy, neo-soul pocket).
- **Swing / Shuffle**: Delays off-beats to match triplet swing grids.
- **Timing (Tight / Loose)**:
  - Left: 100% quantized to the grid (great for electronic dance/synth tracks).
  - Center: Natural human feel.
  - Right: Loose human timing variations.

---

## 5. Performance Controllers & Automations

1. **Force (Pitchbend in Player Mode)**:
   - Automate Pitchbend up (+2000 to +8191) on accented downbeats or chorus peaks to increase plucking attack.
   - Lower Pitchbend during quiet verses for a gentle, rounded touch.
2. **Damp (CC#1 Modulation Wheel)**:
   - Automate CC#1 upwards (e.g. value 70–100) to transform sustained bass notes into tight palm-muted staccatos.
3. **Silence Key (`C0` = 24)**:
   - Insert a note on `C0` during drum breaks to mute the bass line cleanly without resetting the phrase cycle.
