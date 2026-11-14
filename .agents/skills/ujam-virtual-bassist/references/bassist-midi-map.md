# UJAM Virtual Bassist - MIDI Key Map & Controller Reference

This document provides the complete MIDI mapping for all instruments in the **UJAM Virtual Bassist 2 / 2.1 series** (ROYAL, ROWDY, MELLOW, DANDY, SLAP).

> Standard: Middle C = **C3 = MIDI note 60** (Yamaha standard used by UJAM).

---

## 1. Dual Mode Overview

Virtual Bassist operates in two fundamentally different modes, toggled by the **Player / Instrument** switch at the top center of the plugin UI:

```
┌────────────────────────────────────────────────────────────────────────┐
│ PLAYER MODE: Phrase-based accompaniment engine (Common + Style phrases)│
│ [ C0 (24) ]                -> Silence Key (Rest without losing sync)   │
│ [ C#0 to B1 (25 to 47) ]   -> Common Phrases Zone (Universal patterns) │
│ [ C2 to Bb2 (48 to 58) ]   -> Style Phrases Zone (Genre-specific)     │
│ [ B2 (59) ]                -> Stop Key (Cease playback)                │
│ [ C3 to C6 (60 to 96+) ]   -> Play Range / Chord & Root Input         │
└────────────────────────────────────────────────────────────────────────┘

┌────────────────────────────────────────────────────────────────────────┐
│ INSTRUMENT MODE: Note-by-note physical bass modeling with articulations│
│ [ C0 to B0 (24 to 35) ]    -> Articulation & Key Switch Zone           │
│ [ Drop D (26 to 27) ]      -> Extended low register (when active)      │
│ [ C1 to C5 (36 to 84+) ]   -> Playable Pitch Range (4-string physical) │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 2. PLAYER MODE: Keyboard Map (MIDI 24 to 96+)

### A. Control & Phrase Switching Keys (MIDI 24 to 59)

| MIDI Note | Note Name | Function | Behavior |
| :---: | :---: | :--- | :--- |
| **24** | **C0** | **Silence Key** | Mutes bass audio without resetting phrase sequencer. Great for rhythmic pauses. |
| **25–35** | **C#0 to B0** | **Common Phrases (Part 1)** | Universal basic rhythms (1/2, 1/4, 1/8 notes, syncopated pulses). |
| **36–47** | **C1 to B1** | **Common Phrases (Part 2)** | 1/16th patterns, Latin/Disco grooves, and transitional fills. |
| **48–58** | **C2 to Bb2** | **Style Phrases Zone** | Selected Style phrases (white = loop, black = intro/fill). |
| **59** | **B2** | **Stop Key** | Stops phrase playback immediately in Latch mode. |

#### Complete Common Phrases Breakdown (MIDI 25 to 47):
| MIDI Note | Key Name | Name / Style | Pattern Length |
| :---: | :---: | :--- | :---: |
| **25** | C#0 | Long 1/2 Notes | 2 Bars |
| **26** | D0 | Long 1/4 Notes | 2 Bars |
| **27** | D#0 | Short 1/4 Notes | 2 Bars |
| **28** | E0 | Long 1/8 Notes | 2 Bars |
| **29** | F0 | Short 1/8 Notes | 2 Bars |
| **30** | F#0 | Short 1/8 + 1/16 Notes | 2 Bars |
| **31** | G0 | Basic 1/8 Note 1 | 2 Bars |
| **32** | G#0 | Basic 1/8 Note 2 | 2 Bars |
| **33** | A0 | Basic Syncopated 1 | 2 Bars |
| **34** | A#0 | Basic Syncopated 2 | 2 Bars |
| **35** | B0 | Basic 1/16 Note 1 | 2 Bars |
| **36** | C1 | Basic 1/16 Note 2 | 2 Bars |
| **37** | **C#1** | **Fill 1/8 Note** | **1 Bar (Plays once, reverts)** |
| **38** | D1 | Basic 1/16 Note Short | 2 Bars |
| **39** | **D#1** | **Fill 1/16 Note 1** | **1 Bar (Plays once, reverts)** |
| **40** | E1 | Samba | 2 Bars |
| **41** | F1 | Samba 1+5 (Root + Fifth) | 2 Bars |
| **42** | **F#1** | **Fill 1/16 Note 2** | **1 Bar (Plays once, reverts)** |
| **43** | G1 | Disco 1/8 Notes (Octaves) | 2 Bars |
| **44** | **G#1** | **Fill 1/16 Note 3** | **1 Bar (Plays once, reverts)** |
| **45** | A1 | Disco Samba | 2 Bars |
| **46** | **A#1** | **Fill 1/16 Note 4** | **1 Bar (Plays once, reverts)** |
| **47** | B1 | Salsa | 2 Bars |

#### Style Phrases Breakdown (MIDI 48 to 58):
- **White Keys (48, 50, 52, 53, 55, 57)**: Cyclic looping phrases increasing in complexity and density from C2 up to A2.
- **Black Keys**:
  - **49 (C#2)** & **51 (D#2)**: Intro phrases (1–2 bars, play once, auto-revert to current loop).
  - **54 (F#2)**, **56 (G#2)**, **58 (A#2)**: Fill phrases (play once, auto-revert to current loop).

### B. Play Range: Musical Notes & Chords (MIDI 60 to 96+)
- **Notes C3 to C6 (60–96+)**: Holds the pitch or chord.
- **Melodic Mode ON**: Bassist plays walking basslines, pentatonic fills, and scale figures matching the chord and selected **KEY**.
- **Melodic Mode OFF**: Bassist plays strictly the notes you hold, but follows the rhythm and articulation of the selected phrase.

---

## 3. INSTRUMENT MODE: Keyboard Map (MIDI 24 to 84+)

Instrument mode provides note-by-note performance with automatic string selection and physical playing mechanics.

### A. Key Switches & Articulation Triggers (MIDI 24 to 35)

| MIDI Note | Key Name | Articulation / Action |
| :---: | :---: | :--- |
| **24** | **C0** | **Slide 1 Trigger** (Hold key + play note in note range to slide up) |
| **25** | **C#0** | **Legato OFF** (forces re-plucked notes) / **Slide 2** |
| **26** | **D0** | **Slide 3 Trigger** |
| **27** | **D#0** | **Slide 4 Trigger** |
| **28** | **E0** | **Slide 5 Trigger** |
| **30** | **F#0** | **Legato ON** (activates smooth hammer-ons and slides) |
| **31** | **G0** | **"Silent" Dead Note Toggle** (keys in play range sound as dead attacks) |
| **33** | **A0** | **Dead Note 1** (percussive string ghost-note hit) |
| **34** | **Bb0** | **Full Stop** (fretboard string mute / stop slap) |
| **35** | **B0** | **Dead Note 2** (higher pitched ghost attack) |

### B. Playable Pitch Range & 4-String Allocation (MIDI 28 to 84+)

Virtual Bassist automatically selects the appropriate physical string based on interval distance:

| String | Standard MIDI Range | Drop D MIDI Range | Open String Pitch |
| :---: | :---: | :---: | :---: |
| **E-String (Lowest)** | **28 to 34** (E0 to A#0) | **26 to 34** (D0 to A#0) | E0 = 28 (or D0 = 26) |
| **A-String** | **35 to 39** (B0 to D#1) | **35 to 39** | A0 = 33 (played on A-string at 35) |
| **D-String** | **40 to 45** (E1 to A1) | **40 to 45** | D1 = 38 (fretted at 40) |
| **G-String (Highest)**| **46 to 63+** (A#1 to Eb3+) | **46 to 63+** | G1 = 43 (fretted at 46) |

#### Automatic Fretboard Physics Rules:
1. **Intervals 1 to 4 semitones**: Played monophonically on the *same string* as a fret shift.
2. **Intervals > 4 semitones**: Switches to a neighboring string, allowing up to 4-voice polyphony.
3. **Subsequent note louder (+velocity) within 1–2 semitones**: Produces an authentic **Slide**.
4. **Subsequent note softer (-velocity) 1–2 semitones higher**: Produces a **Hammer-On**.
5. **Subsequent note softer (-velocity) 1–2 semitones lower**: Produces a **Pull-Off**.

---

## 4. Hardware Controllers & Wheels

### A. Pitchbend Wheel
- **In Player Mode**: Labeled **Force**. Adjusts the player's physical plucking energy (soft <-> aggressive accents) in real time.
- **In Instrument Mode**: Standard pitch bend (±2 semitones).

### B. Modulation Wheel (CC#1): Damp Control
- Controls **Palm Muting / String Damping** across both Player and Instrument modes.
- Value 0 = Full ringing open sustain; Value 127 = Dry, percussive, woody palm-muted staccato.

### C. Sustain Pedal (CC#64)
- Acts as a momentary **Latch** control in Player Mode (phrases keep playing while held).
