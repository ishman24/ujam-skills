# UJAM Virtual Guitarist SILK 2 - Complete MIDI & Parameter Map

> Reference Standard: **C3 = MIDI note 60** (Yamaha standard, as specified in UJAM documentation).
> Note: In all MorningDAW MCP tool calls, use the exact **MIDI Note Number (0–127)**.

---

## 1. Global Note Range Overview

| Keyboard Zone | Key Name Range (C3=60) | MIDI Note Range | Role in PLAYER Mode | Role in INSTRUMENT Mode |
| :--- | :--- | :--- | :--- | :--- |
| **Common Phrases** | C0 – B1 | 24 – 47 | Hardwired Common Phrases & Special FX | Slides, Trigger Mode On/Off, Up/Downstrokes |
| **Style Phrases / Picking** | C2 – Bb2 | 48 – 58 | Style Phrases (11 phrases per style) | **Individual String Picking (Arpeggios) & Strum Types** |
| **Stop Key** | **B2** | **59** | **Stops playback (in Latch mode)** | Strum – Auto |
| **Bass Note Inversion Zone** | C3 – [Lowest Chord Note] | 60 – Chord Root | Add explicit Bass Note for slash chords (`F/D`) | Add explicit Bass Note for slash chords (`F/D`) |
| **PLAY RANGE (Fretboard)** | **C3 – F5** | **60 – 89** | **Chord / Note Input** (Sounds D2–F4) | **Chord / Fretboard Voicings** (Sounds D2–F4) |

> **IMPORTANT COMPARISON**:
> - In **VG CARBON**, Play Range is **F#3 to F#6 (66 to 102)** with Stop at **F3 (65)**.
> - In **VG SILK 2**, Play Range is **C3 to F5 (60 to 89)** with Stop at **B2 (59)**!

---

## 2. PLAYER Mode MIDI Reference

In Player mode, SILK 2 provides realistic acoustic nylon-string guitar accompaniment (strumming and fingerpicking patterns).

### Common Phrases (C0 – B1, MIDI 24 – 47)
| Key Name | MIDI # | Category | Description |
| :--- | :--- | :--- | :--- |
| **C0** | **24** | **Silence** | Silences all phrases while keeping phrase engine looping in sync (essential for pauses/rests) |
| **C#0 / Db0** | 25 | Sustain | Long Chord With Fill |
| **D0** | 26 | Sustain | Open 1/1 (Whole note ringout) |
| **D#0 / Eb0** | 27 | Sustain | Generic Rhythm Sustain |
| **E0** | 28 | Rhythm | Long Chord on 2 & 4 |
| **F0** | 29 | Rhythm | Off-Beat 2 & 4 |
| **F#0 / Gb0** | 30 | Rhythm | Single Note Rhythm |
| **G0** | 31 | Rhythm | Open Stops 1/4 |
| **G#0 / Ab0** | 32 | Rhythm | Generic Chord Rhythm |
| **A0** | 33 | Rhythm | Open 1/4 |
| **A#0 / Bb0** | 34 | Rhythm | Chord Rhythm 1/16 |
| **B0** | 35 | Rhythm | Half-Mute 1/4 |
| **C1** | 36 | Rhythm | Muted 1/4 |
| **C#1 / Db1** | 37 | Rhythm | Muted 1/8 Open |
| **D1** | 38 | Rhythm | Open 1/8 |
| **D#1 / Eb1** | 39 | Rhythm | Build-Up Open 1/8 |
| **E1** | 40 | Rhythm | Half-Muted 1/8 |
| **F1** | 41 | Rhythm | Muted 1/8 |
| **F#1 / Gb1** | 42 | Rhythm | Muted 1/16 Riding |
| **G1** | 43 | Rhythm | Muted 1/16 |
| **G#1 / Ab1** | 44 | Rhythm | Build-Up Muted 1/8 |
| **A1** | 45 | Rhythm | Off-Beat 1/8 |
| **A#1 / Bb1** | **46** | **Special FX** | **Slide Down** (natural finger sliding down string, ideal song/verse starter) |
| **B1** | **47** | **Special FX** | **Pick Slide** (expressive pick scraping noise) |

### Style Phrases & Stop (C2 – B2, MIDI 48 – 59)
| Key Name | MIDI # | Role | Description |
| :--- | :--- | :--- | :--- |
| **C2 – Bb2** | **48 – 58** | Style Phrases | 11 phrases per style. Ordered by intensity from low (C2) to high (Bb2). Black keys offer syncopations and fills. |
| **B2** | **59** | **STOP** | Stops playback immediately when Latch is active. |

### Play Range & Chord Intelligence (C3 – F5, MIDI 60 – 89)
- **Single Note**: Plays complete power chord or root-fifth-octave voicing.
- **Two Notes**: Interprets interval (+min2 up to +maj14).
- **Three Notes**: Interprets complete guitar triads (Major, Minor, Diminished, Augmented, Sus2, Sus4).
- **Four Notes**: Interprets 4-note guitar tetrads (Maj7, Min7, 7th, Dim7, 6th, etc.).
- **Play Mode: Chord**: Interprets standard keyboard chords into acoustic guitar voicings.
- **Play Mode: Note**: Plays your exact custom voicings while maintaining the rhythmic strum/pick pattern.
- **Open Chords Button**: Adds natural acoustic ringing open strings (adding 7th, 9th, 11th, 13th extensions).

### Bass Notes Feature (Slash Chords)
- Hold chord in Play Range (e.g., F Major: F3 [65] + A3 [69] + C4 [72]).
- Add a bass note **below the chord's lowest note** (e.g., D3 [62]).
- SILK 2 immediately voices this as a slash chord: **`F / D` (F Major over D bass)**!

---

## 3. INSTRUMENT Mode MIDI Reference (Fingerpicking & Strumming)

In Instrument mode, SILK 2 allows **note-by-note fingerpicking arpeggios, manual up/downstrokes, and string mutes**.

### Strumming, Picking & Key Switches (C1 – B2, MIDI 36 – 59)
| Key Name | MIDI # | Function / Articulation |
| :--- | :--- | :--- |
| **C#1 / Db1** | **37** | **Trigger Mode: OFF** (silent fretboard fingering, strum via key switches) |
| **D1** | 38 | Slide – Up |
| **D#1 / Eb1** | **39** | **Trigger Mode: ON** (keys in Play Range trigger notes directly) |
| **E1** | 40 | Slide – Down |
| **F1** | 41 | Slide – Up & Down |
| **F#1 / Gb1** | 42 | Disable Articulation Strumming |
| **G1** | 43 | Pick Slide |
| **G#1 / Ab1** | 44 | Stop – Upstroke |
| **A1** | **45** | **Upstroke** (manual upward strum of held chord) |
| **A#1 / Bb1** | 46 | Stop – Downstroke |
| **B1** | **47** | **Downstroke** (manual downward strum of held chord) |
| **C2** | **48** | **Picking: String 1 (Bass Note)** — First note of custom arpeggio |
| **C#2 / Db2** | 49 | Release |
| **D2** | **50** | **Picking: String 2** — Second note of custom arpeggio |
| **D#2 / Eb2** | 51 | Strum – Dead Note (percussive string slap) |
| **E2** | **52** | **Picking: String 3** — Third note of custom arpeggio |
| **F2** | **53** | **Picking: String 4** — Fourth note of custom arpeggio |
| **F#2 / Gb2** | 54 | Strum – Mute (tight damped strum) |
| **G2** | **55** | **Picking: String 5** — Fifth note of custom arpeggio |
| **G#2 / Ab2** | 56 | Strum – Half Mute |
| **A2** | **57** | **Picking: String 6 (Highest String)** — Sixth note of custom arpeggio |
| **A#2 / Bb2** | 58 | Strum – Open (ringing open chord) |
| **B2** | 59 | Strum – Auto (engine picks alternating up/down strum) |

---

## 4. Real-time Continuous Controllers & Automation

| Controller | Control Name | Function & Tips |
| :--- | :--- | :--- |
| **Pitchbend** | **Force** *(Player Mode)* | Real-time dynamic control of player energy (pianissimo to fortissimo). |
| **Pitchbend** | **Bend** *(Instrument Mode)* | Pitch bend ±2 semitones. |
| **CC#1 (Mod Wheel)** | **Damp** | **Gradual palm-muting!** Morph smoothly from open ringing strings (0) to tight palm-mutes (127). |
| **Automation** | **Blend** | Blends between Microphone setup (left: warm, body, room) and Piezo pickup (right: direct, punchy, crisp). |
| **Automation** | **Character** | `Soft` (warm/intimate), `Tame` (mellow background), `Real` (dynamic natural touch), `Hard` (energetic/bright strumming). |
| **Automation** | **Open Chords** | Toggle open string acoustic voicings (adds 7, 9, 11 extensions). |
| **Automation** | **Air** | Stereo signal level of additional room microphones for spatial width. |
| **Automation** | **Width** | Acoustic double-tracking engine with unmasking EQ. |
| **Automation** | **Variance** | Adds physical strumming delay between strings and natural fretboard noise. |
| **Automation** | **Stomp Box Amount** | Controls intensity of the 30 included guitar stomp pedals. |
| **Automation** | **Finisher Amount** | Controls intensity of the 60+ Finisher multi-FX presets. |
