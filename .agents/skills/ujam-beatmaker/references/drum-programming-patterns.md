# UJAM Beatmaker - Song Arrangement & Drum Programming Guide

This guide explains how to arrange coherent, dynamic, and professional drum tracks using UJAM Beatmaker in combination with MorningDAW MCP tools.

---

## 1. Core Song Arrangement Principles

A realistic and engaging drum track builds energy dynamically across sections. In UJAM Beatmaker, this is achieved by progressing through phrases, firing fills at transitional boundaries, and automating performance sliders.

### Structure of an 8 to 32 Bar Section Flow

```
[ Intro ]       -> Intro 1 (61) or Verse 1 (60) with Kick muted via Pitchbend > 0
[ Verse A ]     -> Verse 1 (60) or Verse 2 (62) - Simple kick, snare/clap, closed hats
[ Verse B ]     -> Verse 3 (64) or Verse 4 (65) - Added percussion, driving hats
[ Pre-Chorus ]  -> Verse 5 (67) or Breakdown (78/80) - Rising tension + Fill 1 (66) on bar 8
[ Chorus A ]    -> Chorus 1 (69) or Chorus 2 (71) - Full kick & snare power, open hats
[ Chorus B ]    -> Chorus 4 (74) or Chorus 5 (76) - Maximum energy, ride cymbal + Fill 3 (70)
[ Bridge ]      -> Special 1 (77) or Special 2 (79) - Half-time or syncopated breakdown
[ Outro ]       -> Ending 1 (73) or Ending 2 (75) - Cadence hit with natural cymbal ring-out
```

---

## 2. Using Fills, Intros & Breakdowns

### Automatic Return Behavior
- **Intros (`C#3` = 61, `D#3` = 63)** and **Fills (`F#3` = 66, `G#3` = 68, `A#3` = 70)** are designed to play once and automatically revert to the previous playing Verse or Chorus without requiring another note-on event!
- When programming in a MIDI clip:
  1. Trigger your looping verse (e.g. note 60 at beat 0.0 with length 16.0).
  2. At beat 15.0 (the 4th beat of measure 4), trigger Fill 1 (note 66 with length 1.0).
  3. The Beatmaker will interrupt the verse, execute the fill seamlessly, and continue.

### Hold-to-Play Breakdowns
- **Breakdown keys (`F#4` = 78, `G#4` = 80, `A#4` = 82)** only play while the key is held down!
- If you release the note, Beatmaker returns to the previously active groove.
- Keep the note active for the full duration of your desired breakdown section (e.g., 2 full bars = 8 beats).

---

## 3. The Power of Real-Time Pitchbend (Kick/Snare Automation)

The Pitchbend wheel is hard-wired to the **Kick/Snare Balance** slider on the plugin GUI:

| Pitchbend State | Value Range | Musical Effect | Best Production Usage |
| :--- | :---: | :--- | :--- |
| **Pitch Bend Up** | `> 0` to `+8191` | Gradually removes **Kick Drum** | Buildups, Snare rolls, Ambient intros, breakdowns |
| **Center** | `0` | Both Kick and Snare active | Standard groove sections |
| **Pitch Bend Down**| `< 0` to `-8192` | Gradually removes **Snare Drum** | 4-on-the-floor club intros, minimal verses, acoustic transitions |

### Automating via MorningDAW:
When creating build-ups into a chorus, automate Pitch Bend upwards over 2 bars to filter out the heavy kick, letting hi-hats and snares build momentum. At the downbeat of the drop (beat 1 of the chorus), snap Pitch Bend back to 0.

---

## 4. Layering Manual Drum Hits (Instrument Section) Over Grooves

You can combine the **Style section (60–83)** with the **Instrument section (36–51)** in the exact same MIDI clip:

- Let **Verse 2 (`D3` = 62)** provide the steady drum foundation.
- Add extra **Clap hits (`D#1` = 39)** on beat 4 of every other bar.
- Add an explosive **Crash cymbal (`C#2` = 49)** on bar 1 beat 1 of each section.
- Add custom **Tom fills (`F1`, `G1`, `A1` = 41, 43, 45)** right before a chorus transition.
- For 808 Trap plugins (HUSTLE / GLORY), trigger **tuned sub-bass slides** in the range 14–26 (D-1 to D0) on key downbeats.

---

## 5. Tempo & Speed Synchronization

- UJAM Beatmakers automatically sync to the host DAW tempo via VST/CLAP sync.
- If producing half-time hip hop at 140 BPM or double-time drum & bass, use the **Micro Timing Speed** parameter:
  - `Half-time`: Slows the internal groove engine by 50%.
  - `Double-time`: Speeds the internal groove engine by 200%.
- For swung genres (Lo-Fi, Boom Bap, UK Garage), adjust the **Swing / Slack / Humanize** parameter to infuse natural groove pocket and avoid robotic rigidity.
