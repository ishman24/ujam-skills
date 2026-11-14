---
name: ujam-virtual-bassist
description: Master control guide and composition skill for all UJAM Virtual Bassists (ROYAL, ROWDY, MELLOW, DANDY, SLAP). Covers dual-zone keyboard architecture (Player Mode with Common/Style phrases vs Instrument Mode note-by-note physical modeling), MIDI note numbers (C3=60), Key & Chord harmonic intelligence (Melodic Mode ON/OFF), articulations (slides, hammer-ons, pull-offs, dead notes, full stops), Drop D tuning, performance wheels (Pitchbend=Force, CC#1=Damp), and MorningDAW MCP bassline writing.
---

# UJAM Virtual Bassist Master Skill

This skill guides the composition, programming, sound design, and real-time control of **all UJAM Virtual Bassist instruments**:
- **ROYAL** (Fingered Electric Bass — Versatile session bass for Pop, Rock, Soul, Indie)
- **ROWDY** (Picked Electric Bass with Overdrive — Hard Rock, Metal, Punk, Alternative)
- **MELLOW** (Acoustic Upright Double Bass — Jazz, Acoustic Pop, Hip-Hop, Folk, Ballads)
- **DANDY** (Flat-Wound Vintage Electric Bass — Motown, Soul, 60s/70s Retro Pop)
- **SLAP** (Active Electric Slap & Pop Bass — Funk, Disco, Modern R&B, Slap Bass Grooves)

---

## 1. Fast Instrument Comparison & Selection

| Bass Title | Playing Technique | Primary Tonal Character | Recommended Musical Genres |
| :--- | :--- | :--- | :--- |
| **VB-ROYAL** | Fingered electric | Round, noble, warm, balanced | Pop, Rock, Soul, Indie, Commercial Songwriting |
| **VB-ROWDY** | Picked electric | Gritty, biting, aggressive pick attack | Hard Rock, Metal, Punk, Alternative Rock |
| **VB-MELLOW**| Acoustic upright | Woody, deep, organic room resonance | Jazz, Acoustic Pop, Hip-Hop, Ballad |
| **VB-DANDY** | Flat-wound strings | Smooth, creamy, subdued top, vintage low-mids | Motown, Soul, Vintage R&B, 70s Disco |
| **VB-SLAP**  | Slap & thumb pop | Punchy thumb strikes, bright pops, percussive | Funk, Disco, Fusion, Modern Pop |

---

## 2. Keyboard Architecture: Player vs. Instrument Mode

Virtual Bassist follows the Yamaha standard (**Middle C = C3 = MIDI note 60**):

### A. PLAYER MODE (Phrase Accompaniment Engine)
Used for automated, groove-locked bass accompaniment:

```
[ C0 (24) ]                 -> Silence Key (Rest without losing phrase sync)
[ C#0 to B1 (25 to 47) ]    -> Common Phrases Zone (Universal grooves & fills)
[ C2 to Bb2 (48 to 58) ]    -> Style Phrases Zone (White = Loops, Black = Intros/Fills)
[ B2 (59) ]                 -> Stop Key (Cease playback in Latch mode)
[ C3 to C6 (60 to 96+) ]    -> Play Range (Chords and Root notes)
```

- **Melodic Mode ON**: Built-in harmonic engine automatically improvises authentic bass runs, walking lines, and passing notes based on the chord and the song's **KEY**.
- **Melodic Mode OFF**: Bassist plays strictly the notes you hold, applying the groove and phrasing of the active Style key.

### B. INSTRUMENT MODE (Note-by-Note Physical Bass Model)
Used for exact, custom basslines, solos, and licks:

```
[ C0 to B0 (24 to 35) ]     -> Key Switches & Articulation Triggers
[ D0 / E0 (26 to 28) ]      -> Lowest open string (28 standard E, 26 with Drop D engaged)
[ C1 to C5 (36 to 84+) ]    -> Playable Bass Range (Automatic 4-string allocation)
```

- **String allocation**: Low E (28–34 or 26–34 in Drop D), A (35–39), D (40–45), G (46–63+).
- **Physical polyphony rule**: Intervals 1–4 semitones are played monophonically on the *same string*; intervals > 4 semitones switch strings (up to 4 voices).
- **Velocity mechanics**:
  - Subsequent note louder within 1–2 semitones = **Slide**.
  - Subsequent note softer 1–2 semitones higher = **Hammer-on**.
  - Subsequent note softer 1–2 semitones lower = **Pull-off**.

---

## 3. Key Switches & Articulations Reference (Instrument Mode)

| MIDI Note | Key Name | Articulation / Action |
| :---: | :---: | :--- |
| **24** | **C0** | **Slide 1 Trigger** (Hold key + play target note to slide up) |
| **25** | **C#0** | **Legato OFF** (forces re-plucking of every note) |
| **26–28**| **D0 to E0** | **Slide Triggers 2, 3, 4** |
| **30** | **F#0** | **Legato ON** (enables hammer-ons, pull-offs, and slides) |
| **31** | **G0** | **"Silent" Dead Note Toggle** (held notes become dead hits) |
| **33** | **A0** | **Dead Note 1** (percussive ghost-note string attack) |
| **34** | **Bb0** | **Full Stop** (hand palm choke across strings) |
| **35** | **B0** | **Dead Note 2** (higher pitched ghost attack) |

---

## 4. Hardware Controllers & Automations

### A. Pitchbend Wheel
- **Player Mode**: Labeled **Force**. Real-time control of plucking energy (soft <-> aggressive accents).
- **Instrument Mode**: Pitch bend (±2 semitones).

### B. Modulation Wheel (CC#1): Damp Control
- Controls **Palm Muting / String Damping** (0 = open sustain, 127 = dry percussive mute).

### C. Sustain Pedal (CC#64)
- Acts as momentary **Latch** in Player Mode.

---

## 5. Tonal Shaping & Effects

- **Pickup**: Continuous blend between Neck (woody, round) and Bridge (bite, nasal punch).
- **Character**: 4-way switch (`Soft`, `Warm`, `Neutral`, `Hard`).
- **Drop D**: Lowers the lowest string from E to D (down to MIDI note 26).
- **Amp**: 4 models (`Rock` 8x10 tube fridge, `Soul` 1x15 vintage, `Pop` 4x10 modern transistor, `Direct` DI).
- **Drive**: Preamp tube saturation.
- **Equalizer**: 4-band macro morphing from *Vintage* (sub-heavy) to *Modern* (punchy slap).
- **Compressor**: One-knob dynamic leveling + transient punch.
- **Octaver**: Synthetic +1 octave layer for high melodic presence.
- **Finisher**: 15 multi-effects (chorus, flanger, overdrive, delay, filter sweeps).

---

## 6. MorningDAW MCP Tool Call Examples

### Example 1: Player Mode Progression with Phrase Fills & Stop
```json
{
  "ServerName": "morningdaw",
  "ToolName": "add_notes",
  "Arguments": {
    "track": 1,
    "clip": 0,
    "notes": [
      { "note": 48, "start_beat": 0.0, "duration": 14.0, "velocity": 100 },
      { "note": 54, "start_beat": 14.0, "duration": 2.0, "velocity": 110 },
      { "note": 50, "start_beat": 16.0, "duration": 16.0, "velocity": 105 },
      { "note": 60, "start_beat": 0.0, "duration": 8.0, "velocity": 100 },
      { "note": 63, "start_beat": 8.0, "duration": 8.0, "velocity": 100 },
      { "note": 65, "start_beat": 16.0, "duration": 8.0, "velocity": 105 },
      { "note": 67, "start_beat": 24.0, "duration": 8.0, "velocity": 110 },
      { "note": 59, "start_beat": 32.0, "duration": 1.0, "velocity": 100 }
    ]
  }
}
```
*Note 48 (Style Phrase 1) runs from beat 0 to 14, followed by Fill 1 (note 54) on beat 14.0. Note 50 (Style Phrase 2) takes over at beat 16.0, and Stop (note 59) terminates playback at beat 32.0!*

### Example 2: Instrument Mode Groovy Bassline with Dead Notes & Choke
```json
{
  "ServerName": "morningdaw",
  "ToolName": "add_notes",
  "Arguments": {
    "track": 1,
    "clip": 0,
    "notes": [
      { "note": 28, "start_beat": 0.0, "duration": 1.5, "velocity": 115 },
      { "note": 33, "start_beat": 1.75, "duration": 0.25, "velocity": 90 },
      { "note": 28, "start_beat": 2.0, "duration": 0.75, "velocity": 110 },
      { "note": 31, "start_beat": 2.75, "duration": 0.25, "velocity": 95 },
      { "note": 33, "start_beat": 3.0, "duration": 0.75, "velocity": 105 },
      { "note": 34, "start_beat": 3.75, "duration": 0.25, "velocity": 100 }
    ]
  }
}
```
*Notice how Dead Note 1 (note 33) provides a rhythmic ghost pickup at beat 1.75, and Full Stop (note 34) executes a crisp fretboard choke on beat 3.75!*

---

## 7. Reference Files

- Complete MIDI mapping chart: [bassist-midi-map.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-bassist/references/bassist-midi-map.md).
- Instrument models, amplifiers, and sonic controls: [bassist-titles-guide.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-bassist/references/bassist-titles-guide.md).
- Bassline composition, chord recognition, and fretboard physics: [bassline-composition-guide.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-virtual-bassist/references/bassline-composition-guide.md).
