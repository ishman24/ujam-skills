# Harmonic and Melodic Riffing Guide for UJAM Virtual Guitarist CARBON

Virtual Guitarist CARBON is an **8-string custom low-tuned guitar** spanning down to low F# (actual frequency ~46.25 Hz). Due to the acoustic laws of low-frequency physics and high-gain amp saturation (intermodulation distortion), writing music for CARBON requires strict harmonic discipline to avoid acoustic "mud" while maximizing punch, clarity, and aggression.

---

## 1. Low Register Physics & The Harmonic Mud Trap

### The Intermodulation Distortion Problem
When two frequencies enter a high-gain distortion stage, the nonlinear clipping generates sum and difference frequencies (\(f_1 \pm f_2\)).
- In higher registers, these difference frequencies add pleasant overtones.
- In low registers (F#1 to E2, triggered by MIDI notes 66 to 76 in CARBON), minor and major 3rds produce difference frequencies in the deep sub-bass range (20–40 Hz) that are completely out of tune with the root note, creating violent rumble, loss of punch, and a blurred mix.

### Golden Voicing Rules by Register

#### A. Low Register (F#3 to E4 / MIDI 66 to 76 — Actual Pitch: F#1 to E2)
- **Rule 1: Never play full 3-note triads (major or minor) in this register.**
- **Rule 2: Stick to single notes, octaves, and Perfect 5th Power Chords.**
  * *Single Root Note*: e.g., Low F# (MIDI 66) for tight syncopated djent chugs.
  * *Power Chord (Dyad - 1 & 5)*:
    - Root + 5th (e.g., F#3 [66] + C#4 [73]).
  * *Full Power Chord (Root + 5th + Octave)*:
    - F#3 (66) + C#4 (73) + F#4 (78).
  * *Tension Exception - Tritone (Diminished 5th)*:
    - Root + Flat 5th (e.g., F#3 [66] + C4 [72]) for evil, aggressive metal tension. Use as a passing chord or accent stab, not a resting harmony.

#### B. Mid Register (F4 to C5 / MIDI 77 to 84 — Actual Pitch: F2 to C3)
- In this octave, power chords sound crisp and clear.
- Open inverted power chords (Drop-D style 4ths or 5ths) work well.
- Suspended chords (**sus2** and **sus4**) can be introduced cleanly:
  * e.g., F#3 (66) + C#4 (73) + G#4 (80) [F# sus2 power chord].
  * Adds modern progressive/cinematic tension without muddiness.

#### C. Upper Register (C#5 to F#6 / MIDI 85 to 102 — Actual Pitch: C#3 to F#4)
- Full harmonic expression, melody lines, lead riffs, and complex extensions belong here:
  * **Minor 3rds & Major 3rds**: Place the 3rd here while the root stays low.
    * Example: Low F# (66) + C#4 (73) + A4 (81) or A5 (93) for a pristine minor chord.
  * **Melodic Hooks & Solos**: Use Single Mode or Legato Instrument Mode.
  * **Add9 / Minor 7th / Octave slides**: Beautiful, wide cinematic voicings.

---

## 2. Rhythmic Groove & Articulation Matrix

Heavy guitar realism is 70% articulation and 30% pitch. In CARBON, you must balance palm-mutes, open sustains, and fast bursts.

### The Dynamic Riffing Formula
```
[Heavy Downbeat / Accent] -> [Syncopated Chugs] -> [Color / Tension Chord] -> [Turnaround / Shred Fill]
Artic: Sustain (C3/60)   -> Full Mute (G2/55)   -> Half Mute (A2/57)       -> Shred (F#2/54 or C#3/61)
```

1. **Pedal-Tone Chugging**:
   - Keep the lowest root note (e.g., F#3 = 66, or A3 = 69) as a rhythmic anchor.
   - Use **Full Mutes (G2 = 55)** on 16th-note off-beats.
   - On the snare hits (beats 2 & 4) or anticipated 16th syncopations, pop into **Half Mutes (A2 = 57)** or open **Sustains (C3 = 60)** with higher velocity (>110).

2. **The "Dead Note" Rhythmic Slap (F2 = 53)**:
   - Use Dead Notes as ghost notes immediately preceding a heavy downbeat, or as a percussive stop on beat 4 of a measure.

3. **Shred Fills at Section Transitions**:
   - At bar 4 or bar 8, hold **C#2/49** (Player mode) or **C#3/61** (Instrument mode) for exactly two beats to unleash a machine-gun 16th-note triplet burst leading into the next phrase.

---

## 3. Legato, Slides, and Expressive Nuance

In **Single Mode** (Player) or with **Legato ON (D#2 / 51)** (Instrument):
- **Slide**: Trigger Note B, then before Note B ends, trigger Note C (within 1–2 semitones) at an equal or higher velocity. CARBON automatically slides between the frets instead of picking again.
- **Hammer-On / Pull-Off**: Trigger the second note with **significantly lower velocity** than the held note.
  * Pitch higher + lower velocity = Hammer-On.
  * Pitch lower + lower velocity = Pull-Off.

---

## 4. Structuring a Dynamic Song with CARBON

| Song Section | Recommended Mode | Voicing Style | Articulation Strategy | Sound / Amp Settings |
| :--- | :--- | :--- | :--- | :--- |
| **Intro / Buildup** | Player Mode | Sparse power chords or single low notes | Open 1/4 (D1/38) or Wuggeda 1 (C2/48) | Single Guitarist. Filter knob turned left (lowpass sweep). Severity moderate. Finisher CC#1 at 20-40%. |
| **Verse** | Instrument Mode | Low single-note groove (djent rhythm) | Tight Full Mutes (G2/55) with dead-note ghosting (F2/53) | Double Layerer. Condition: Insane or Rabid. Focus at 9 o'clock (low-mid punch). |
| **Pre-Chorus** | Player or Instrument | Ascending power chords with sus2/sus4 tension | Half Mutes building into Open 1/8 notes (F1/41) | Double to Triple. Mod Wheel (CC#1) rising to build tension. |
| **Chorus / Drop** | Player Mode (Chords) or Instrument | Wide Power Chords + Octaves (Root + 5th + 8ve) | Full Sustains (C3/60) + Common Phrases (F1/41 or Style white keys) | Quadro Layerer! Spread at 100%. Severity boosted. Finisher preset: "Double Track" or "Clouds". |
| **Breakdown** | Instrument Mode | Drop F# pedal bursts, polyrhythmic pauses | Alternating Full Mutes (G2/55) with Silence (C1/36) and Dead Notes (F2/53) | Condition: Lobotomized. Distance knob dialed back for massive spatial impact. |
| **Outro / Final Ring** | Player Mode | Final root power chord | Ending Key: C#1 (37) for ringing sustain or D#1 (39) for abrupt stop | Let notes ring naturally; automate reverb/delay decay. |
