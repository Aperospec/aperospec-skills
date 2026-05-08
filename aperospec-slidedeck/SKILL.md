---
name: aperospec-slidedeck
description: Use Aperospec Slidedeck as a downstream Narrative Rendering System that accepts only a Narrative World Package (NWP) from aperospec-cinema and outputs a fixed Slide Cinema Package (SCP). Use for standardized NWP-to-slide mapping: world to opening sequence, emotional environment to atmosphere layer, Something Is Coming to narrative tension sequence, core conflict to conflict sequence, emotional curve to slide rhythm system, immersive experience to spatial experience, visual world to art direction, and scene potentials to cinematic scenes. This skill does not analyze the world, regenerate narrative, accept raw topics/PPT requests, or create bullet-point corporate presentations.
---

# Aperospec Slidedeck Narrative Rendering System

`下游 Skill | Slide Cinema 渲染引擎`

## Core Definition

This skill is not:

> making PPT.

It is:

> rendering a Narrative World Package into a Slide Cinema Package.

It is no longer a thinking system or a narrative generation system.

It is a downstream:

> Narrative Rendering System.

Its only responsibility is:

> like a director, shoot the Narrative into a film made of slides.

## Pipeline Position

Pipeline:

`aperospec -> aperospec-project -> CWP -> aperospec-cinema -> NWP -> aperospec-slidedeck -> SCP -> Final Slide Movie`

| Skill | Position | Output |
| --- | --- | --- |
| aperospec | original cognitive personality layer | divergent thinking |
| aperospec-project | standardized cognitive engine | Cognitive World Package (CWP) |
| aperospec-cinema | narrative translation engine | Narrative World Package (NWP) |
| aperospec-slidedeck | Slide Cinema rendering engine | Slide Cinema Package (SCP) |

## Interface Definition

### INPUT SOURCE

Input source:

> `aperospec-cinema.skill`

### INPUT TYPE

This system can only receive:

> Narrative World Package (NWP)

The NWP must contain:
- WORLD
- EMOTIONAL ENVIRONMENT
- SOMETHING IS COMING
- CORE CONFLICT
- EMOTIONAL CURVE
- IMMERSIVE EXPERIENCE
- VISUAL WORLD
- SCENE POTENTIALS

Forbidden direct inputs:
- theme
- phenomenon
- world analysis
- Cognitive results
- PPT requirements
- raw bullet points
- business structure

If the input is not an NWP, do not produce slides. Ask for a valid NWP from `aperospec-cinema`.

### OUTPUT TYPE

This system always outputs:

> Slide Cinema Package (SCP)

## System Responsibility

Old responsibility was vague:
- cinematic
- worldview
- narrative
- slide

New responsibility is precise:

`Narrative World Package (NWP) -> Slide Cinema Package (SCP)`

This skill only performs:

> Narrative Rendering.

It does not create the Narrative.

It renders the Narrative into cinematic slides.

## Narrative To Slide Mapping System

This is the core mapping protocol.

### NWP: WORLD -> Opening Sequence

Generate:
- opening shots
- Establishing Shots
- world-entry slides

### NWP: EMOTIONAL ENVIRONMENT -> Atmosphere Layer

Generate:
- black frames
- negative space
- lighting rhythm
- spatial pressure

### NWP: SOMETHING IS COMING -> Narrative Tension Sequence

Generate:
- omen slides
- Transition slides
- Silent Slides

### NWP: CORE CONFLICT -> Conflict Sequence

Generate:
- emotional scenes
- human tension
- behavioral conflict

### NWP: EMOTIONAL CURVE -> Slide Rhythm System

Generate:
- rhythm
- peaks
- pauses
- breathing

### NWP: IMMERSIVE EXPERIENCE -> Spatial Experience

Generate:
- spatial feeling
- immersion
- narrative movement

### NWP: VISUAL WORLD -> Art Direction

Generate:
- color
- typography
- lighting
- atmosphere

### NWP: SCENE POTENTIALS -> Cinematic Scenes

Generate:
- storyboards
- shots
- Close-ups
- Inserts
- Silent moments

## Slide Cinema Package Output Protocol

Always output the fixed SCP structure below.

For the reusable template, read `references/slide-cinema-package.md`.

### 1. SCREENPLAY

Slide movie screenplay.

Define:
- Opening
- Conflict
- Transition
- Escalation
- Ending

### 2. VISUAL SCRIPT

Define:
- shots
- camera movement
- light and shadow
- rhythm
- typography density

### 3. STORYBOARD

Define each page:
- shot type
- page temperament
- emotional target
- information density

### 4. SLIDE STRUCTURE

Define:
- page order
- rhythm
- transition
- black frames
- information insert points

### 5. ART DIRECTION

Define:
- color
- typography
- lighting
- atmosphere

## Strict Rules

### RULE 1

Forbidden:

> re-analyzing the world.

### RULE 2

Forbidden:

> regenerating the Narrative.

Use the NWP as the source of truth.

### RULE 3

Forbidden:
- bullet-point PPT
- dense reporting pages
- equal-weight information blocks

### RULE 4

Forbidden:
- corporate reporting style
- enterprise pitch style
- "solution" language
- "empower" language

### RULE 5

Must follow:

> Scene Before Explanation.

### RULE 6

Must follow:

> Emotion Before Information.

### RULE 7

Must include:

> Silent Slides.

## Final Principle

This system does not:

> think.

It does not:

> generate Narrative.

It only:

> renders Narrative into a cinematic Slide Movie.
