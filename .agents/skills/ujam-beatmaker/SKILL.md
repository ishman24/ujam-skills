---
name: ujam-beatmaker
description: Master control guide and drum programming skill for all UJAM Beatmaker plugins (DOPE, EDEN, HUSTLE, VOID, VICE, HYPE, KANDY, NEMESIS, GLORY, IDOL, RICO, BERSERK, CIRCUITS, COZY). Teaches dual-zone keyboard mapping (Instrument manual hits 36–51 vs Style groove phrases 60–83), white-key looping vs black-key fills/intros/breakdowns/endings, hardwired Pitchbend (Kick/Snare balance) and CC#1 (Beat Intensity), genre-specific Special Sliders, and MorningDAW MCP clip programming.
---

# UJAM Beatmaker Master Skill

This skill guides the composition, drum programming, dynamic arrangement, and real-time control of **all UJAM Beatmaker series virtual instruments**:
- **DOPE** (Boom Bap, 90s Hip-Hop)
- **EDEN** (EDM, Festival, Dance)
- **HUSTLE** & **GLORY** (Trap, Grime, 808 Drill, Modern Urban)
- **VOID** (Drum & Bass, Jungle, Breakbeat)
- **VICE** (80s Synthwave, Retrowave)
- **HYPE** (Progressive House, Big Room EDM)
- **KANDY** (Modern Billboard Pop)
- **NEMESIS** (Cyberpunk, Darksynth, Aggressive Industrial)
- **IDOL** (K-Pop)
- **RICO** (Reggaeton, Dembow, Latin Urban)
- **BERSERK** (Dubstep, Glitch, Heavy Beats)
- **CIRCUITS** (Vintage Analog Drum Machines)
- **COZY** (Lo-Fi Hip-Hop, Chillhop)

Every UJAM Beatmaker shares the exact same core architecture, differing primarily in their genre-specific sample kits, groove styles, and signature **Special Sliders**.

---

## 1. Fast Architecture & Keyboard Zones

UJAM Beatmaker follows the Yamaha standard (**Middle C = C3 = MIDI note 60**):

```
Zone 0: MIDI 14 to 26 (D-1 to D0)  -> 808 Bass Tune (HUSTLE & GLORY only, 1 chromatic octave)
Zone 1: MIDI 36 to 51 (C1 to D#2)  -> INSTRUMENT SECTION (Manual drum one-shots & kit hits)
Zone 2: MIDI 52 to 59 (E2 to B2)   -> Empty / Unassigned
Zone 3: MIDI 60 to 83 (C3 to B4)   -> STYLE SECTION (Groove phrases, fills, breakdowns, stop)
```

---

## 2. Style Section: Grooves & Song Arrangement (MIDI 60 to 83)

The Style section contains 23 groove parts and 1 Stop key:

### White Keys: Continuous Looping Song Parts
In **Latch mode**, pressing a white key initiates a continuous groove loop that stays in sync with the DAW transport. Higher keys increase arrangement density and energy:
- **C3 (60)**: Verse 1 (Minimal / Sparse groove)
- **D3 (62)**: Verse 2 (Standard verse with clap/snare)
- **E3 (64)**: Verse 3 (Rhythmic variation)
- **F3 (65)**: Verse 4 (Driving verse with hats)
- **G3 (67)**: Verse 5 (Pre-chorus / build-up groove)
- **A3 (69)**: Chorus 1 (Main beat drop / full power)
- **B3 (71)**: Chorus 2 (Chorus with open hats)
- **C4 (72)**: Chorus 3 (Driving syncopation)
- **D4 (74)**: Chorus 4 (Heavy layered percussion)
- **E4 (76)**: Chorus 5 (Climax / maximum intensity)
- **F4 (77)**, **G4 (79)**, **A4 (81)**: Special 1, 2, 3 (Alternative rhythm, half-time, or bridge)

### Black Keys: Transitional, Fills & Breakdown Parts
- **Intros (`C#3` = 61, `D#3` = 63)**: 1 to 2 bar intros. Play once, then automatically drop into the previous Verse/Chorus.
- **Fills (`F#3` = 66, `G#3` = 68, `A#3` = 70)**: 1-bar or 1/2-bar transition fills. Play once and return immediately to the current loop.
- **Breakdowns (`F#4` = 78, `G#4` = 80, `A#4` = 82)**: **Held keys**. Stripped-down breakdown groove plays *only while held*; releasing returns to the previous loop.
- **Endings (`C#4` = 73, `D#4` = 75)**: Final cadence hit and cymbal tail. Automatically stops the sequencer.
- **Stop (`B4` = 83)**: Stops playback immediately.

---

## 3. Instrument Section: Individual Drum Hits (MIDI 36 to 51)

> ⚠️ **Non-GM Drum Mapping**: UJAM Beatmaker uses an electronic-optimized layout, NOT standard General MIDI!

| MIDI Note | Pad Name | Drum Element |
| :---: | :---: | :--- |
| **36 (C1)** | BD 1 | Main Punch Kick |
| **37 (C#1)** | BD 2 | Alternative / Sub / Dirty Kick |
| **38 (D1)** | SN 1 | Main Snare Drum |
| **39 (D#1)** | Clap | Handclap / Finger Snap |
| **40 (E1)** | SN 2 | Alternative Snare / Rimshot / Side Stick |
| **41 (F1)** | Tom 1 | Floor Tom (Low) |
| **42 (F#1)** | HH 1 | Closed Hi-Hat |
| **43 (G1)** | Tom 2 | Mid Tom |
| **44 (G#1)** | HH 2 | Half-Open Hi-Hat |
| **45 (A1)** | Tom 3 | High Tom |
| **46 (A#1)** | HH 3 | Open Hi-Hat |
| **47 (B1)** | FX 1 | Percussion 1 / Impact / Sub Bass |
| **48 (C2)** | FX 2 | Percussion 2 / Sweep / Glitch / Cowbell |
| **49 (C#2)** | Cymbal 1 | Crash Cymbal |
| **50 (D2)** | Cymbal 2 | Ride Cymbal |
| **51 (D#2)** | HH 4 | Shaker / Accent Hat / Percussion 3 |

*You can layer manual hits (36–51) directly over active style phrases (60–83) for customized accents, fills, and crash cymbal crashes!*

---

## 4. Performance Controllers (Hardware & Automation)

UJAM Beatmakers feature two hardwired performance controllers that breathe life into static arrangements:

### A. Pitchbend Wheel: Kick/Snare Balance Slider
- **Pitch Bend > 0 (Up)**: Gradually mutes and eliminates the **Kick Drum**. Ideal for pre-drop tension, snare rolls, and ambient verses.
- **Pitch Bend < 0 (Down)**: Gradually mutes and eliminates the **Snare Drum**. Ideal for four-on-the-floor kick intros and breakdown beats.
- **Pitch Bend = 0 (Center)**: Both Kick and Snare operate at nominal balance.

### B. Modulation Wheel (CC#1): Beat Intensity Slider
- Controls dynamic velocity and energy of the drummer in real time without altering channel fader volume.

---

## 5. Genre-Specific Special Sliders Quick Reference

| Plugin | Special Slider Name | Core Function & Sonic Effect |
| :--- | :--- | :--- |
| **DOPE** | **Vinyl Drive** | Turntable crackle, vinyl noise, vintage tape compression |
| **EDEN** | **Kick Pump** | Sidechain pumping compressor driven by the kick drum |
| **HUSTLE** | **Bass Tune** | 808 sub kick chromatic pitch tuning (also MIDI 14–26) |
| **VOID** | **Vortex** | LFO notch sweep + compression for risers and swirling drops |
| **VICE** | **Time Machine** | 1980s thin retro tape vs 2080s heavy futuristic punch |
| **HYPE** | **Riser** | Combined HPF filter + spacious reverb + sync delay |
| **KANDY** | **Sweetness** | Multiband compression + transient designer for modern pop punch |
| **NEMESIS** | **Pressurize / Hypercharge** | Down = Multiband compression; Up = Multiband distortion |
| **GLORY** | **Bass Tune** | 808 sub kick chromatic pitch tuning (also MIDI 14–26) |
| **IDOL** | **Juice** | Multiband EQ + stereo widener + punch compression |
| **RICO** | **Me Gusta** | Stereo widener + sub boost (up) vs mid punch (down) |
| **BERSERK**| **Squish / Devastate** | Down = Slam compression; Up = Aggressive wave distortion |
| **CIRCUITS**| **Boost + / Boost -** | Up = Low/high boost + comp; Down = Mid punch + transient sharpener |
| **COZY** | **Nostalgia** | Vinyl crackle + tube mic convolution + lo-fi saturation |

---

## 6. MorningDAW MCP Tool Call Examples

### Example 1: 16-Bar Dynamic Song Progression (Verse -> Pre-Chorus -> Fill -> Chorus)
```json
{
  "ServerName": "morningdaw",
  "ToolName": "add_notes",
  "Arguments": {
    "track": 0,
    "clip": 0,
    "notes": [
      { "note": 60, "start_beat": 0.0, "duration": 16.0, "velocity": 100 },
      { "note": 64, "start_beat": 16.0, "duration": 16.0, "velocity": 105 },
      { "note": 67, "start_beat": 32.0, "duration": 12.0, "velocity": 110 },
      { "note": 70, "start_beat": 44.0, "duration": 4.0, "velocity": 115 },
      { "note": 69, "start_beat": 48.0, "duration": 16.0, "velocity": 120 },
      { "note": 49, "start_beat": 48.0, "duration": 2.0, "velocity": 127 }
    ]
  }
}
```
*Notice how at beat 44.0, Fill 3 (note 70) takes over seamlessly for 1 bar before dropping into Chorus 1 (note 69) with a layered Crash cymbal hit (note 49) on beat 48.0!*

### Example 2: Ending a Song Cleanly
```json
{
  "ServerName": "morningdaw",
  "ToolName": "add_notes",
  "Arguments": {
    "track": 0,
    "clip": 0,
    "notes": [
      { "note": 73, "start_beat": 64.0, "duration": 4.0, "velocity": 115 }
    ]
  }
}
```
*Note 73 (Ending 1) triggers the final hit and cymbal decay, automatically stopping the Beatmaker engine without leaving dangling sounds.*

---

## 7. Reference Files

- Full MIDI key and pad breakdown: [beatmaker-midi-map.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-beatmaker/references/beatmaker-midi-map.md).
- Detailed guide of each Beatmaker title & Special slider: [beatmaker-titles-guide.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-beatmaker/references/beatmaker-titles-guide.md).
- Song arrangement patterns and controller workflows: [drum-programming-patterns.md](file:///d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/ujam-beatmaker/references/drum-programming-patterns.md).
