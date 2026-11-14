# UJAM Beatmaker - MIDI Key Map & Controller Reference

This document provides the definitive MIDI mapping for all plugins in the **UJAM Beatmaker 2 / 2.1 series** (DOPE, EDEN, HUSTLE, VOID, VICE, HYPE, KANDY, NEMESIS, GLORY, IDOL, RICO, BERSERK, CIRCUITS, COZY).

> Standard: Middle C = **C3 = MIDI note 60** (Yamaha standard used by UJAM).

---

## 1. Keyboard Layout Overview

```
[ D-1 to D0 (14-26) ] -> HUSTLE & GLORY only: 808 Bass Pitch Tuning (1 Octave)
[ C1  to D#2 (36-51) ] -> INSTRUMENT SECTION (Manual Drum Hits & One-Shots)
[ E2  to B2  (52-59) ] -> Unassigned / Reserved
[ C3  to B4  (60-83) ] -> STYLE SECTION (Song Part Groove Phrases & Fills)
```

---

## 2. Style Section: Groove Phrases & Song Parts (MIDI 60 to 83)

The Style section allows triggering full genre-specific drum arrangements that automatically sync with DAW tempo and bar lines.

### A. Looping Song Parts (White Keys)
In **Latch mode**, white keys loop continuously until another phrase or the Stop key is pressed.
Phrases increase in energy and density as you move up the keyboard:

| MIDI Note | Note Name | Song Part | Musical Role & Energy |
| :---: | :---: | :--- | :--- |
| **60** | **C3** | **Verse 1** | Sparse / minimal groove (kick + hi-hat or rimshot) |
| **62** | **D3** | **Verse 2** | Verse with light snare/clap addition |
| **64** | **E3** | **Verse 3** | Mid-tempo verse variation with extra percussion |
| **65** | **F3** | **Verse 4** | Driving verse with busier hi-hat patterns |
| **67** | **G3** | **Verse 5** | Pre-chorus tension / driving verse |
| **69** | **A3** | **Chorus 1** | Full beat drop with solid kick & snare presence |
| **71** | **B3** | **Chorus 2** | Chorus variation with open hats / cymbals |
| **73** | *C#4* | *(Black key - see below)* | |
| **72** | **C4** | **Chorus 3** | Driving chorus with syncopated ghost notes |
| **74** | **D4** | **Chorus 4** | High-energy chorus with layered percussion |
| **76** | **E4** | **Chorus 5** | Peak festival / anthem climax intensity |
| **77** | **F4** | **Special 1** | Half-time, triplet, or genre-specific syncopation |
| **79** | **G4** | **Special 2** | Rhythmic bridge / alternative groove |
| **81** | **A4** | **Special 3** | Extra polyrhythmic or stripped-down groove |

### B. Transitional & One-Shot Parts (Black Keys)
Black keys do not loop infinitely (except Breakdowns while held):

| MIDI Note | Note Name | Song Part | Behavior & Description |
| :---: | :---: | :--- | :--- |
| **61** | **C#3** | **Intro 1** | 1 to 2 bar intro pattern. Plays once, then automatically reverts to the previous Verse/Chorus. |
| **63** | **D#3** | **Intro 2** | Alternative intro pattern (often with risers/snare rolls). |
| **66** | **F#3** | **Fill 1** | 1-bar or half-bar transition fill. Plays once, then reverts. |
| **68** | **G#3** | **Fill 2** | More intense syncopated fill with cymbals/rolls. |
| **70** | **A#3** | **Fill 3** | Maximum complexity turnaround fill into chorus/drop. |
| **73** | **C#4** | **Ending 1** | Final cadence and hit. Ends performance cleanly and stops. |
| **75** | **D#4** | **Ending 2** | Alternative ring-out or tail ending. |
| **78** | **F#4** | **Breakdown 1**| **Held Key**: Plays stripped-down breakdown beat only while held! Releasing reverts to previous loop. |
| **80** | **G#4** | **Breakdown 2**| Alternative breakdown (kick-less or snare-less). |
| **82** | **A#4** | **Breakdown 3**| Filtered or atmospheric breakdown variation. |

### C. Stop Key
| MIDI Note | Note Name | Function | Description |
| :---: | :---: | :--- | :--- |
| **83** | **B4** | **Off / Stop** | Stops phrase playback immediately without killing reverb tails. |

---

## 3. Instrument Section: Individual Drum Hits (MIDI 36 to 51)

> ⚠️ **Important**: Beatmaker mapping differs from General MIDI (GM) standard!
> It is optimized for electronic drum production (dual kicks, claps, multiple hi-hat openness states, sound effects).

| MIDI Note | Note Name | Instrument Pad | Description / Usage |
| :---: | :---: | :--- | :--- |
| **36** | **C1** | **BD 1** | Main Punch Kick / Low fundamental bass drum |
| **37** | **C#1** | **BD 2** | Alternative Kick (Sub, clicky transient, or distorted) |
| **38** | **D1** | **Snare 1** | Main Snare Drum (Fat, central crack) |
| **39** | **D#1** | **Clap** | Handclap / Finger Snap / Layer Clap |
| **40** | **E1** | **Snare 2** | Alternative Snare (Rimshot, side stick, or tight snare) |
| **41** | **F1** | **Tom 1 (Tom L)** | Low Floor Tom |
| **42** | **F#1** | **HH 1 (Closed)** | Tight Closed Hi-Hat |
| **43** | **G1** | **Tom 2 (Tom M)** | Mid Rack Tom |
| **44** | **G#1** | **HH 2 (Half)** | Half-Open Hi-Hat / Loose Hat |
| **45** | **A1** | **Tom 3 (Tom H)** | High Rack Tom |
| **46** | **A#1** | **HH 3 (Open)** | Fully Open Sizzle Hi-Hat |
| **47** | **B1** | **FX 1 / Perc 1** | Impact FX, Shaker, or Sub Bass (HUSTLE/GLORY) |
| **48** | **C2** | **FX 2 / Perc 2** | Sweep, Glitch hit, Vocal shout, or Cowbell |
| **49** | **C#2** | **Cymbals 1** | Crash Cymbal (accent hit with splash) |
| **50** | **D2** | **Cymbals 2** | Ride Cymbal (cup/bow articulation) |
| **51** | **D#2** | **HH 4 / Accent** | Pedal Hat, Shaker, or High Accent Percussion |

---

## 4. Special Pitch Tuning Zone (HUSTLE & GLORY Only)

For 808-focused Beatmakers (**HUSTLE** and **GLORY**), you can write tuned 808 basslines directly via MIDI notes:

| MIDI Range | Note Names | Function |
| :---: | :---: | :--- |
| **14 to 26** | **D-1 to D0** | Chromatic tuning of the 808 Sub Kick across 1 full octave. |

---

## 5. Performance Hardware Controllers & Automations

### A. Pitchbend Wheel: Kick/Snare Balance Slider
- **Hard-wired function**: Dynamically balances the presence of Kick vs Snare!
- **Pitch Wheel > Center (> 0)**: Progressively fades out the **Kick drum**. Great for building up snare rolls and hi-hat excitement before a drop.
- **Pitch Wheel < Center (< 0)**: Progressively fades out the **Snare drum**. Great for four-on-the-floor kick grooves, intros, and minimal verses.
- **Pitch Wheel = Center (0)**: Both Kick and Snare operate at full nominal volume.

### B. Modulation Wheel (CC#1): Beat Intensity Slider
- **Hard-wired function**: Controls the dynamic energy / intensity of the playing groove.
- Acts as a macro velocity scaling factor: pulling it down simplifies and calms the groove without affecting the master fader volume.

### C. Sustain Pedal (CC#64)
- When **Latch** is turned off in the plugin UI, pressing CC#64 acts as a momentary latch: phrases continue playing as long as the sustain pedal is held.

---

## 6. Micro Timing & Feel

Inside the **Micro Timing** menu of the plugin interface:
- **Speed**: `0.5x` (Half-Time), `1.0x` (Normal), `2.0x` (Double-Time).
- **Player Sync**: `Note On`, `1/16`, `1/8`, `1/4`, or `Song Position` (ensures phrases trigger in lockstep with the DAW grid).
- **Groove Feel Sliders**:
  - **Swing / Shuffle**: CIRCUITS, EDEN, HYPE, KANDY.
  - **Quantize**: DOPE, HUSTLE, VOID.
  - **Slack**: BERSERK, VICE, NEMESIS, GLORY (slight delay between kick and snare/hat for authentic unquantized human / MPC feel).
  - **Humanize**: RICO, COZY (drifts hits slightly off the grid for relaxed lo-fi swing).
