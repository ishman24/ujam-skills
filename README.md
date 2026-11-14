# MorningDAW MCP & UJAM Instrument Skills Ecosystem

Este repositorio contiene la configuración, plugins y el conjunto de **habilidades maestras (Skills)** para permitir que **Antigravity** (asistente de IA agentic de Google DeepMind) componga, programe, diseñe sonido y controle en tiempo real instrumentos virtuales avanzados en **MorningDAW** a través del protocolo **Model Context Protocol (MCP)**.

---

## 1. Visión General del Proyecto

Los instrumentos virtuales de la familia **UJAM** destacan por su enorme calidad sonora y su motor físico/estilístico, pero presentan una arquitectura de control muy particular (teclados divididos en dos zonas, interruptores de articulación por debajo del Do central, ruedas de modulación/pitchbend con funciones propietarias no estándar y motores de inteligencia armónica).

Para que un agente de IA pueda componer música profesional y coherente sin caer en disonancias, "barro" frecuencial o desincronizaciones rítmicas, hemos desarrollado una tríada de skills especializadas que cubren las tres familias principales de instrumentos UJAM: **Virtual Guitarist**, **Beatmaker** y **Virtual Bassist**.

---

## 2. Catálogo de Skills Desarrolladas

### 🎸 `ujam-virtual-guitarist`
Skill unificada para la composición y control de guitarras pesadas/distorsionadas y guitarras limpias/acústicas.

- **Instrumentos Soportados**:
  - *Distorsionadas / Heavy*: **VG CARBON** (8 cuerdas drop-tuning para djent/metal moderno) y **VG IRON 2** (rock/metal).
  - *Limpias / Acústicas*: **VG SILK 2** (nylon fingerpicking y clásica), **VG AMBER 2** (acústica de acero) y **VG SPARKLE 2** (eléctrica pop limpia).
- **Mapeo y Convención**: Estándar Yamaha (**C3 = MIDI 60**).
- **Mecánicas Clave**:
  - **Regla Anti-Barro (VG CARBON)**: Prohibición de terceras o triadas completas en el registro bajo (MIDI 66–76) para evitar la distorsión por intermodulación; uso exclusivo de fundamentales, quintas y octavas en graves.
  - **Arpegios Personalizados P-I-M-A (VG SILK 2)**: Modo *Trigger OFF* (`C#1` = 37) con pulsación individual de las 6 cuerdas (`C2, D2, E2, F2, G2, A2` = MIDI 48–57).
  - **Strums & Articulaciones**: Rasgueo abajo (`B1`), rasgueo arriba (`A1`), slap/stop (`Bb1`, `Ab1`), dead note (`D#2`) y acorde abierto resonante (`Bb2`).
  - **Controladores**: Rueda Mod (CC#1) asignada a *Finisher* en guitarras eléctricas y a *Damp* (palm mute acústico) en acústicas; Pitchbend asignado a *Force* (dinámica de rasgueo).
- **Archivos de Referencia**:
  - [`SKILL.md`](.agents/skills/ujam-virtual-guitarist/SKILL.md)
  - [`carbon-midi-map.md`](.agents/skills/ujam-virtual-guitarist/references/carbon-midi-map.md)
  - [`silk2-midi-map.md`](.agents/skills/ujam-virtual-guitarist/references/silk2-midi-map.md)
  - [`harmonic-riffing-guide.md`](.agents/skills/ujam-virtual-guitarist/references/harmonic-riffing-guide.md)
  - [`acoustic-fingerpicking-guide.md`](.agents/skills/ujam-virtual-guitarist/references/acoustic-fingerpicking-guide.md)

---

### 🥁 `ujam-beatmaker`
Skill maestra para la programación rítmica, arreglos y producción de baterías electrónicas y urbanas.

- **Instrumentos Soportados (14 Títulos)**:
  - **DOPE** (Boom Bap, 90s Hip-Hop)
  - **EDEN** (EDM, Festival, Dance)
  - **HUSTLE** & **GLORY** (Trap, 808 Drill, Urban)
  - **VOID** (Drum & Bass, Jungle, Breakbeat)
  - **VICE** (80s Synthwave, Retrowave)
  - **HYPE** (Progressive House, Big Room EDM)
  - **KANDY** (Pop Moderno, Billboard)
  - **NEMESIS** (Cyberpunk, Darksynth, Electro Agresivo)
  - **IDOL** (K-Pop)
  - **RICO** (Reggaeton, Dembow, Latin Urban)
  - **BERSERK** (Dubstep, Glitch, Electro Pesado)
  - **CIRCUITS** (Cajas de Ritmo Vintage Analógicas)
  - **COZY** (Lo-Fi Hip-Hop, Chillhop)
- **Mapeo No-GM Optimizado**:
  - **Instrument Section (MIDI 36–51 / C1–D#2)**: Doble bombo (36/37), caja principal (38), claps (39), caja secundaria (40), toms (41, 43, 45), 4 estados de hi-hat (cerrado 42, semi-abierto 44, abierto 46, shaker/acento 51) y platos (49 crash, 50 ride).
  - **Style Section (MIDI 60–83 / C3–B4)**:
    - *Teclas Blancas (Looping)*: Versos 1–5 (60, 62, 64, 65, 67), Coros 1–5 (69, 71, 72, 74, 76) y Especiales 1–3 (77, 79, 81).
    - *Teclas Negras (One-shot / Transición)*: Intros 1–2 (61, 63), Fills 1–3 (66, 68, 70), Endings 1–2 (73, 75) y Breakdowns (78, 80, 82, activos sólo mientras se mantienen pulsados).
    - *Stop Key*: `B4` (MIDI 83).
- **Controladores y Sliders Especiales**:
  - **Pitchbend**: Rueda hard-wired al balance **Kick/Snare** (arriba atenúa bombo para subidones; abajo atenúa caja para 4-on-the-floor).
  - **Mod Wheel (CC#1)**: **Beat Intensity** (escala de energía dinámica en tiempo real).
  - **Afinación de 808 (HUSTLE/GLORY)**: Control cromático de notas MIDI 14 a 26 (D-1 a D0).
  - **Catálogo de Sliders Especiales**: *Vinyl Drive*, *Kick Pump*, *Vortex*, *Time Machine*, *Riser*, *Sweetness*, *Pressurize/Hypercharge*, *Juice*, *Me Gusta*, *Squish/Devastate*, *Boost +/-* y *Nostalgia*.
- **Archivos de Referencia**:
  - [`SKILL.md`](.agents/skills/ujam-beatmaker/SKILL.md)
  - [`beatmaker-midi-map.md`](.agents/skills/ujam-beatmaker/references/beatmaker-midi-map.md)
  - [`beatmaker-titles-guide.md`](.agents/skills/ujam-beatmaker/references/beatmaker-titles-guide.md)
  - [`drum-programming-patterns.md`](.agents/skills/ujam-beatmaker/references/drum-programming-patterns.md)

---

### 🎸 `ujam-virtual-bassist`
Skill de composición, diseño tímbrico y modelado de bajo de sesión.

- **Instrumentos Soportados**:
  - **VB-ROYAL** (Bajo eléctrico pulsado con dedos — Pop, Rock, Soul, Indie).
  - **VB-ROWDY** (Bajo con púa y saturación — Rock duro, Metal, Punk).
  - **VB-MELLOW** (Contrabajo acústico vertical — Jazz, Acústico, Hip-Hop).
  - **VB-DANDY** (Bajo vintage con cuerdas planas — Motown, 60s/70s Soul).
  - **VB-SLAP** (Bajo activo slap/pop — Funk, Disco, Modern Pop).
- **Arquitectura de Doble Modo**:
  - **PLAYER MODE (Motor de Acompañamiento)**:
    - `C0` (24): Tecla *Silence* (silencia la frase sin reiniciar el compás).
    - `C#0 a B1` (25 a 47): *Common Phrases* universales (redondas, negras, semicorcheas, fills de 1 compás, ritmos latinos y disco).
    - `C2 a Bb2` (48 a 58): *Style Phrases* cíclicas con intros y fills dedicados.
    - `B2` (59): Tecla *Stop* en modo Latch.
    - `C3 a C6` (60 a 96+): Rango de acordes y notas fundamentales.
    - **Inteligencia Armónica (Melodic Mode ON/OFF)**: Detección de 14 tipos de acordes y enlace con el parámetro **KEY** para que las notas de paso armonicen sin disonancia con la escala del tema.
  - **INSTRUMENT MODE (Modelo Físico de 4 Cuerdas)**:
    - *Key Switches (MIDI 24–35)*: Triggers de slides (24–28), Legato ON/OFF (30/25), Dead Notes percusivas (33, 35) y Full Stop (34).
    - *Rango de Notas Reales (28–84+ o 26 en Drop D)*: Asignación física a cuerdas (E 28–34, A 35–39, D 40–45, G 46–63+). Intervalos $\le$ 4 semitonos se tocan en la misma cuerda; saltos mayores cambian de cuerda (hasta 4 voces). Disparo automático de slides (+velocidad) y hammer-ons/pull-offs (-velocidad).
- **Modelado Sonoro**:
  - Mezcla continua de pastillas (*Neck/Bridge*).
  - Selector *Character* de 4 posiciones (*Soft*, *Warm*, *Neutral*, *Hard*).
  - Afinador *Drop D* a Re grave (36.7 Hz / MIDI 26).
  - 4 amplificadores (*Rock* 8x10 a válvulas, *Soul* 1x15, *Pop* 4x10 transistores y *Direct* DI).
  - Canal de efectos: *Drive*, *Compressor* (con transient shaper), *Equalizer* (morphing Vintage/Modern), *Octaver* y multiefectos *Finisher* (15 modos).
- **Archivos de Referencia**:
  - [`SKILL.md`](.agents/skills/ujam-virtual-bassist/SKILL.md)
  - [`bassist-midi-map.md`](.agents/skills/ujam-virtual-bassist/references/bassist-midi-map.md)
  - [`bassist-titles-guide.md`](.agents/skills/ujam-virtual-bassist/references/bassist-titles-guide.md)
  - [`bassline-composition-guide.md`](.agents/skills/ujam-virtual-bassist/references/bassline-composition-guide.md)

---

## 3. Demostración Práctica en MorningDAW: Suite Multi-Pista

Para verificar la cohesión armónica y rítmica de las skills, se programó una suite completa de **32 compases (128 pulsos / ~1:04 min) a 120 BPM en tonalidad de Do Menor (C Minor)** distribuida en 4 pistas simultáneas dentro de MorningDAW:

```
Pistas del Proyecto en MorningDAW:
┌───────┬─────────────────┬───────────┬────────────┬──────────────────────────────────────┐
│ Pista │ Nombre          │ Plugin    │ Nivel (dB) │ Rol Musical                          │
├───────┼─────────────────┼───────────┼────────────┼──────────────────────────────────────┤
│ Trk 0 │ Instrument 1    │ BM-NEMESIS│  -7.0 dB   │ Batería electrónica pesada y fills   │
│ Trk 1 │ VG-CARBON       │ VG-CARBON │  -8.0 dB   │ Riffs djent distorsionados y power ch│
│ Trk 2 │ VG-SILK2        │ VG-SILK2  │   0.0 dB   │ Arpegios acústicos fingerpicking PIMA│
│ Trk 3 │ VB-ROYAL        │ VB-ROYAL  │  -4.5 dB   │ Bajo de sesión, base y licks         │
└───────┴─────────────────┴───────────┴────────────┴──────────────────────────────────────┘
```

### Secciones Musicales Sincronizadas (Marcadores):
1. **Intro (Player Mode) [pulsos 0–16]**: Arpegio fingerpicking suave en nylon (SILK2), bajo sutil en notas redondas (ROYAL) y parada de expectación (*Silence* en pulso 14).
2. **Verse (Djent Groove) [pulsos 16–48]**: Riff djent pesado con palm-mutes sincopados (CARBON), bajo clavando el bombo en semicorcheas y adornos agudos acústicos. Fills de transición en compases 8 y 12.
3. **Pre-Chorus (Build) [pulsos 48–64]**: Escalada armónica ascendente ($Ab \rightarrow Bb \rightarrow Cm \rightarrow D^\circ \rightarrow Eb$) con rasgueo acústico abierto, bajo en corcheas conductoras y fill de redoble.
4. **Chorus (Wall of Sound) [pulsos 64–96]**: Muralla de guitarras en quintas y octavas, acompañamiento rítmico acústico brillante y bajo en compás completo con máxima presencia.
5. **Breakdown (Low F# Djent) [pulsos 96–112]**: Sincopación poli-rítmica grave alternando Sol y Fa sostenido al unísono entre bajo y guitarra pesada con percusión cortante.
6. **Outro (Ending Ring) [pulsos 112–128]**: Pedal largo en Do menor, acento cadencial final y tecla *Stop* en pulso 127 para corte limpio de motores.

---

## 4. Estructura de Directorios

```
MCP-CONFIG/
├── .agents/
│   ├── plugins/
│   │   └── morningdaw/
│   │       ├── plugin.json
│   │       └── mcp_config.json        # Excluido de Git (credenciales/token)
│   ├── skills/
│   │   ├── ujam-virtual-guitarist/
│   │   │   ├── SKILL.md
│   │   │   └── references/
│   │   ├── ujam-beatmaker/
│   │   │   ├── SKILL.md
│   │   │   └── references/
│   │   └── ujam-virtual-bassist/
│   │       ├── SKILL.md
│   │       └── references/
│   └── mcp_config.json                # Excluido de Git (credenciales/token)
├── UJAM-documents/                    # Excluido de Git (manuales en PDF)
├── .gitignore                         # Configurado para ignorar PDFs y tokens
└── README.md                          # Este documento
```

---

## 5. Despliegue e Instalación

Las skills están desplegadas de forma idéntica en dos ubicaciones para máxima disponibilidad:
1. **Workspace Local**: `d:/Sonido/MorningDAW/MCP-CONFIG/.agents/skills/`
2. **Configuración Global de Antigravity**: `C:/Users/34658/.gemini/config/skills/`

Cualquier sesión de Antigravity que opere sobre MorningDAW detecta automáticamente estas skills y sus mapas de referencia al interactuar con pistas e instrumentos UJAM.
