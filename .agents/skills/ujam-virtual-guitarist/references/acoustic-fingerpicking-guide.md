# Acoustic Harmony and Fingerpicking Guide for UJAM Clean Guitars (SILK 2, AMBER, SPARKLE)

Unlike heavy, high-gain guitars (such as VG CARBON), clean nylon-string and steel-string acoustic guitars thrive on **rich, harmonic complexity, extended chords, open ringing intervals, and delicate fingerpicking arpeggios**.

---

## 1. Clean Guitar Harmony & Voicing Principles

### A. Triads, 7ths, and 9ths
Clean guitars do not suffer from severe intermodulation distortion in the low-mid register. You can freely use:
- **Major and Minor Triads**: Clean, transparent separation between the root, 3rd, and 5th.
- **7th and 9th Chords**: Major 7th (`Maj7`), Minor 7th (`m7`), Dominant 7th (`7`), and Add9 chords create lush, emotional singer-songwriter and pop textures.
- **Suspensions (sus2, sus4)**: Excellent for intros, acoustic interludes, and resolutions.

### B. The "Open Chords" Feature
- In SILK 2, activating **Open Chords** automatically adds open strings to chord voicings.
- The engine intelligently introduces upper tensions (7, 9, 11, 13) depending on the chord, giving the acoustic guitar an expansive, wide, and spherical character.
- **Best for**: Arpeggios, fingerpicking styles (e.g., *Porcelain*, *Youngsters*, *Singing Souls*), and ballads.
- *Note*: Deactivate Open Chords when you want tight, dry, percussive funk or strict triad backing.

### C. Bass Inversions & Slash Chords (`Chord / Bass`)
SILK 2 includes a specialized **Bass Note zone** between `C3` and the lowest note of the played chord:
1. Play a chord in the Play Range (e.g., `G Major`: G3 [67] + B3 [71] + D4 [74]).
2. Add a bass note **below** the chord (e.g., `B2` or `E3` [64]).
3. The chord reader interprets it as a **slash chord** (e.g., `G / B` or `G / E` [Em7 inversion]).
4. **Usage in Ballads & Fingerpicking**: Creates walking basslines (e.g., `C -> C/B -> Am7 -> C/G -> F`) essential for acoustic storytelling.

---

## 2. Fingerpicking Arpeggios in Instrument Mode

Virtual Guitarist SILK 2 features dedicated **Individual String Picking Key Switches** (MIDI notes 48 to 57):

| String | Key Switch | MIDI Note | Typical String Assigned |
| :---: | :---: | :---: | :--- |
| **String 1** | **C2** | **48** | Lowest Bass String (E / A / D string depending on chord root) |
| **String 2** | **D2** | **50** | Second lowest string |
| **String 3** | **E2** | **52** | Third string |
| **String 4** | **F2** | **53** | Fourth string |
| **String 5** | **G2** | **55** | Fifth string |
| **String 6** | **A2** | **57** | Highest treble string (high E) |

### How to Program Custom Fingerpicking Patterns:
1. In the track, hold the target chord in the **Play Range (C3 to F5)** (e.g., C Major: 60, 64, 67, 72).
2. Set **Trigger Mode: OFF (C#1 = 37)** so that chord changes are silent on the fretboard.
3. Rhythmically trigger the picking keys with desired velocities:

#### Classic 4/4 Folk/Pop Fingerpicking Pattern (1 Bar):
```
Beat:    1.0      1.5      2.0      2.5      3.0      3.5      4.0      4.5
String:  String 1 String 3 String 2 String 4 String 1 String 3 String 2 String 5
MIDI:    C2 (48)  E2 (52)  D2 (50)  F2 (53)  C2 (48)  E2 (52)  D2 (50)  G2 (55)
```

#### Gentle 6/8 or 3/4 Ballad Arpeggio (1 Bar):
```
Beat:    1.0      1.33     1.66     2.0      2.33     2.66
String:  String 1 String 2 String 3 String 4 String 5 String 6
MIDI:    C2 (48)  D2 (50)  E2 (52)  F2 (53)  G2 (55)  A2 (57)
```

#### Alternating Strum + Bass Picking:
- Beat 1.0: Bass pick -> `C2` (48)
- Beat 1.5: Upstroke strum -> `A1` (45)
- Beat 2.0: Dead-strum slap -> `D#2` (51)
- Beat 2.5: High string pick -> `G2` (55)

---

## 3. Dynamic Strumming & Flamenco / Latin Techniques

### Upstroke vs. Downstroke Control
- **Downstroke (`B1` = 47)**: Emphasizes the lower strings first, producing a full, grounded sound.
- **Upstroke (`A1` = 45)**: Sweeps upwards from the higher strings, creating a brighter, lighter accent.
- **Stop Downstroke (`Bb1` = 46)** and **Stop Upstroke (`Ab1` = 44)**: Immediate hand-chokes simulating a guitarist cutting string resonance with the heel of the palm.

### Organic Humanization
- **Variance Knob**: Increase to introduce subtle strum delays between strings and organic fret squeaks.
- **Damp (CC#1 - Modulation Wheel)**: Automate CC#1 upwards on verse rhythm sections to tighten the sound into acoustic palm-mutes, then drop CC#1 to 0 on the chorus for maximum open string resonance.
- **Force (Pitchbend Wheel in Player Mode)**: Automate smooth dynamic swells (whisper-soft fingerstyle to powerful energetic strumming).

---

## 4. Song Arrangement Architecture for Clean Guitars

| Song Section | Style / Mode | Left-Hand Trigger | Voice & Harmonic Complexity | Tone & Mic Settings |
| :--- | :--- | :--- | :--- | :--- |
| **Intro** | Player or Fingerpicking | Slide Down `Bb1` (46) -> Single Note Rhythm `F#0` (30) or custom picks | Open Chords ON, add9 or sus2 intervals | Blend 100% Mic (warm body), Air at 40%, Character: Soft |
| **Verse 1** | Instrument Mode (Arpeggios) | P-I-M-A picking using `C2, D2, E2, F2` | Triads with walking bassline inversions (`C -> C/B -> Am7`) | CC#1 (Damp) at 20-30% for delicate intimacy |
| **Pre-Chorus** | Player Mode | Muted 1/8s `F1` (41) building to Open 1/8s `D1` (38) | Minor 7th chords with ascending root motion | Force (Pitchbend) rising from 50% to 85% |
| **Chorus** | Player Mode | Style Phrase high intensity (e.g. `A2` or `Bb2`) | Full 4-note voicings with Open Chords ON | Character: Hard, Width: ON, Stomp Box: Chorus, Finisher: Shimmer |
| **Bridge** | Instrument Mode | Alternating manual Downstroke (`B1`) and Upstroke (`A1`) | Suspended chords (sus4 -> maj) | Blend adjusted towards Piezo for cutting presence |
| **Outro** | Player Mode | Open 1/1 Sustain `D0` (26) | Final major or add9 chord ringing freely | Let chord decay; automate Finisher reverb tails |
