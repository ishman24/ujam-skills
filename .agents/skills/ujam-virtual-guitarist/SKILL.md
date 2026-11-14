---
name: ujam-virtual-guitarist
description: Master control guide and composition skill for all UJAM Virtual Guitarists. Covers both heavy/distorted guitars (VG CARBON, IRON) and clean/acoustic nylon/steel guitars (VG SILK 2, AMBER, SPARKLE). Teaches dual-zone keyboard splits (Player vs Instrument mode), MIDI note numbers (C3=60), phrase triggers, articulations, fingerpicking arpeggios, strumming directions, chord voicings, Open Chords, and MorningDAW MCP track writing.
---

# UJAM Virtual Guitarist Master Skill

This skill guides the composition, programming, and real-time control of **all UJAM Virtual Guitarists**:
1. **Heavy / Distorted Electric Guitars**: Specializing in **VG CARBON** (8-string low-tuned djent/metal) and **VG IRON 2**.
2. **Clean / Acoustic & Nylon Guitars**: Specializing in **VG SILK 2** (nylon fingerstyle & concert guitar), **VG AMBER 2** (steel-string acoustic), and **VG SPARKLE 2** (clean pop electric).

UJAM instruments operate with a **two-handed split keyboard architecture**, dedicated articulation/phrase key switches, and guitar physics engines.

---

## 1. Fast Instrument Comparison & Identification

Always identify which UJAM instrument is loaded on the track before generating MIDI:

| Feature / Zone | Heavy / Distorted (VG CARBON / IRON) | Clean / Acoustic (VG SILK 2 / AMBER) |
| :--- | :--- | :--- |
| **Physical Instrument** | 8-string drop-tune electric (F#1 to F#4) | 6-string nylon or steel acoustic (D2 to F4) |
| **Play Range (Musical Notes)** | **F#3 to F#6 (MIDI 66 to 102)** | **C3 to F5 (MIDI 60 to 89)** |
| **Stop Key (Latch Mode)** | **F3 (MIDI 65)** | **B2 (MIDI 59)** |
| **Common Phrases Zone** | **C1 to F2 (MIDI 36 to 53)** | **C0 to B1 (MIDI 24 to 47)** |
| **Style Phrases Zone** | **F#2 to E3 (MIDI 54 to 64)** | **C2 to Bb2 (MIDI 48 to 58)** |
| **Silence Key (Rest without desync)**| **C1 (MIDI 36)** | **C0 (MIDI 24)** |
| **CC#1 (Modulation Wheel)** | **Finisher Amount** | **Damp** (gradual acoustic palm-mute) |
| **Pitchbend Wheel** | Pitch Detune (±1 tone) | **Force** in Player Mode (dynamics), Bend in Instrument |
| **Harmonic Voicing Rule** | Strictly Power Chords & 5ths in low end (*No low 3rds!*) | Full Triads, Maj7, Min7, 9ths, Add9, **Open Chords** |
| **Bass Slash Chords (`Chord/Bass`)**| Not supported | Supported via "Add bass note" (C3 to chord root) |
| **Instrument Mode Mechanics** | Legato on/off, 5 Mute grades, Shreds, Repetitions | **6-String Arpeggio Picking (48–57)**, Up/Downstrokes, Slides |

---

## 2. Detailed Reference Maps

- For complete MIDI key charts of CARBON: see [carbon-midi-map.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-guitarist/references/carbon-midi-map.md).
- For complete MIDI key charts of SILK 2: see [silk2-midi-map.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-guitarist/references/silk2-midi-map.md).
- For heavy drop-tune harmonic physics: see [harmonic-riffing-guide.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-guitarist/references/harmonic-riffing-guide.md).
- For nylon/acoustic fingerpicking & arpeggios: see [acoustic-fingerpicking-guide.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-guitarist/references/acoustic-fingerpicking-guide.md).

---

## 3. Working with Clean & Acoustic Guitars (VG SILK 2)

### A. Harmonic Brilliance & Open Chords
- Clean guitars do not suffer from distortion intermodulation. You can play rich chords across the entire Play Range (60–89).
- **Open Chords**: When activated, adds open strings and 7th, 9th, 11th extensions for expansive, shimmering acoustic accompaniment.
- **Walking Bass & Slash Chords**:
  1. Hold chord notes in Play Range (e.g. `C Major`: 60, 64, 67).
  2. Add a bass note **below** the chord (e.g. `B2` / note 59 or `E3` / note 64).
  3. SILK 2 renders this as a slash chord (e.g. `C / B` or `C / E`).

### B. Custom Fingerpicking Arpeggios (Instrument Mode)
In Instrument Mode, SILK 2 provides dedicated keys for each of the 6 guitar strings:
- **C2 (48)**: String 1 (Lowest Bass String)
- **D2 (50)**: String 2
- **E2 (52)**: String 3
- **F2 (53)**: String 4
- **G2 (55)**: String 5
- **A2 (57)**: String 6 (Highest Treble String)

#### Programming Workflow for Fingerpicking:
1. Turn **Trigger Mode OFF** by triggering `C#1` (37) so the chord fretboard does not sound on touch.
2. Hold the chord voicing in the **Play Range (60–89)**.
3. Rhythmical trigger the picking keys (`C2`, `D2`, `E2`, etc.) to create custom classical or folk arpeggio figures.

### C. Manual Strumming & Stroke Articulations
- **B1 (47)**: Downstroke (full downward strum).
- **A1 (45)**: Upstroke (bright upward brush).
- **Bb1 (46)** / **Ab1 (44)**: Downstroke Stop / Upstroke Stop (palm slap mute).
- **D#2 (51)**: Strum Dead (percussive string strike).
- **Bb2 (58)**: Strum Open (ringing acoustic chord).

---

## 4. Working with Heavy Guitars (VG CARBON)

### The Anti-Mud Harmonic Rule
- In **MIDI notes 66 to 76 (F#3 to E4)**: **Never play full 3rds or 7ths**. High-gain distortion creates clash and mud.
- Stick to: Single Root notes (66), Power Chords (1+5: 66+73), and Octave Power Chords (66+73+78).
- Place 3rds and melodic lines strictly above **MIDI 77 (F4)**.

### Rhythmic Articulation Balancing
- Balance **Full Mutes (`G2` = 55)** on syncopated 16th-note chugs with **Sustains (`C3` = 60)** on accented downbeats.
- Insert **Shred keys (`F#2` = 54 or `C#3` = 61)** on the last beats of measures for explosive fills.

---

## 5. MorningDAW MCP Tool Call Examples

### Example 1: Acoustic Nylon Fingerpicking Arpeggio in VG SILK 2 (Instrument Mode)
- Chord: Am7 (A3=69, C4=72, E4=76, G4=79).
- Fingerpicking: P-I-M-A arpeggio using strings 1, 3, 2, 4 (`C2`, `E2`, `D2`, `F2`).
```json
{
  "ServerName": "morningdaw",
  "ToolName": "add_notes",
  "Arguments": {
    "track": 1,
    "notes": [
      // Trigger Mode OFF (silent fretboard fingering)
      {"start_beat": 0.0, "length_beats": 4.0, "pitch": 37, "velocity": 100},

      // Fretboard chord held silently across the bar
      {"start_beat": 0.0, "length_beats": 4.0, "pitch": 69, "velocity": 100},
      {"start_beat": 0.0, "length_beats": 4.0, "pitch": 72, "velocity": 100},
      {"start_beat": 0.0, "length_beats": 4.0, "pitch": 76, "velocity": 100},
      {"start_beat": 0.0, "length_beats": 4.0, "pitch": 79, "velocity": 100},

      // Fingerpicking pattern (P - I - M - A)
      {"start_beat": 0.0, "length_beats": 0.5, "pitch": 48, "velocity": 105}, // String 1 (Bass)
      {"start_beat": 0.5, "length_beats": 0.5, "pitch": 52, "velocity": 85},  // String 3
      {"start_beat": 1.0, "length_beats": 0.5, "pitch": 50, "velocity": 90},  // String 2
      {"start_beat": 1.5, "length_beats": 0.5, "pitch": 53, "velocity": 95},  // String 4
      {"start_beat": 2.0, "length_beats": 0.5, "pitch": 48, "velocity": 100}, // String 1 (Bass)
      {"start_beat": 2.5, "length_beats": 0.5, "pitch": 52, "velocity": 85},  // String 3
      {"start_beat": 3.0, "length_beats": 0.5, "pitch": 50, "velocity": 90},  // String 2
      {"start_beat": 3.5, "length_beats": 0.5, "pitch": 55, "velocity": 95}   // String 5
    ]
  }
}
```

### Example 2: Pop Acoustic Strumming with Slide Intro in VG SILK 2 (Player Mode)
- Slide Down intro (`Bb1` = 46) into driving Open 1/8s (`D1` = 38).
- Chords: Cmaj9 -> G/B (slash chord) -> Am7.
```json
{
  "ServerName": "morningdaw",
  "ToolName": "add_notes",
  "Arguments": {
    "track": 1,
    "notes": [
      // Intro Slide Down FX on beat 0
      {"start_beat": 0.0, "length_beats": 0.5, "pitch": 46, "velocity": 100},
      {"start_beat": 0.0, "length_beats": 0.5, "pitch": 60, "velocity": 100},

      // Bar 1 (0.5 to 4.0): C Major with Open 1/8s (D1=38)
      {"start_beat": 0.5, "length_beats": 3.5, "pitch": 38, "velocity": 100},
      {"start_beat": 0.5, "length_beats": 3.5, "pitch": 60, "velocity": 105}, // C
      {"start_beat": 0.5, "length_beats": 3.5, "pitch": 64, "velocity": 105}, // E
      {"start_beat": 0.5, "length_beats": 3.5, "pitch": 67, "velocity": 105}, // G
      {"start_beat": 0.5, "length_beats": 3.5, "pitch": 71, "velocity": 105}, // B

      // Bar 2 (4.0 to 8.0): G/B Slash Chord
      {"start_beat": 4.0, "length_beats": 4.0, "pitch": 38, "velocity": 100},
      {"start_beat": 4.0, "length_beats": 4.0, "pitch": 59, "velocity": 100}, // Bass B below chord
      {"start_beat": 4.0, "length_beats": 4.0, "pitch": 67, "velocity": 100}, // G
      {"start_beat": 4.0, "length_beats": 4.0, "pitch": 71, "velocity": 100}, // B
      {"start_beat": 4.0, "length_beats": 4.0, "pitch": 74, "velocity": 100}  // D
    ]
  }
}
```

---

## 6. Golden Rules & Troubleshooting Checklist

1. **"Why is the acoustic guitar playing strange notes instead of chords?"**:
   - Check if you played notes below `C3` (MIDI 60). In SILK 2, notes 24–59 are phrase/picking keys.
2. **"Why is there silence when I hit chords in Player Mode?"**:
   - Check if you are holding a Phrase key (C0–B1 for common phrases, C2–Bb2 for styles).
3. **"How do I create organic acoustic rests without restarting the rhythm loop?"**:
   - Trigger **C0 (MIDI 24, Silence key)** in SILK 2 (or **C1 / 36** in CARBON).
4. **"How do I control acoustic palm-muting?"**:
   - Automate **MIDI CC#1 (Mod Wheel)**. In SILK 2, CC#1 controls **Damp**, smoothly morphing open nylon resonance into tight palm-mutes.
5. **"How do I control player dynamics in SILK 2?"**:
   - Automate the **Pitchbend wheel** in Player Mode. It directly controls **Force** (the energetic intensity of the guitarist).
