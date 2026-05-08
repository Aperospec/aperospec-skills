---
name: aperospec-storyboard
description: Use Aperospec Storyboard as the storyboard engine in the Aperospec Pipeline. It accepts only a Narrative World Package (NWP) from aperospec-cinema and outputs a Storyboard Package (SBP): slide sequence, silent slides, emotional peaks, transition slides, narrative rhythm, and scene progression. It answers how the film advances scene by scene. It does not perform visual design, layout, typography, image direction, rendering, world analysis, or narrative generation.
---

# Aperospec Storyboard Engine

`下游 Skill | 分镜引擎`

## Core Definition

This skill is not the final slide design engine.

It is the storyboard engine.

Its task is:

> translating a Narrative World Package into a sequence of cinematic beats.

It answers:

> How does this film advance scene by scene?

## Pipeline Position

`aperospec -> aperospec-project -> CWP -> aperospec-cinema -> NWP -> aperospec-storyboard -> SBP -> aperospec-visualdirector -> VDP -> Final Slide Cinema`

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
- TOPIC
- CWP
- PPT requirements
- visual design requirements
- image prompts
- typography requests
- layout requests

### OUTPUT TYPE

This system always outputs:

> Storyboard Package (SBP)

### OUTPUT TARGET

Output target:

> `aperospec-visualdirector.skill`

## Responsibility Boundary

This skill is responsible for:
- Slide Sequence
- Silent Slides
- Emotional Peaks
- Transition Slides
- Narrative Rhythm
- Scene Progression

This skill is not responsible for:
- visual design
- layout
- image generation
- image prompts
- typography
- composition
- final rendering

## Narrative To Storyboard Mapping

Map NWP fields into SBP:

| NWP field | SBP output |
| --- | --- |
| WORLD | opening sequence and world entry |
| EMOTIONAL ENVIRONMENT | atmosphere beats and silent pressure |
| SOMETHING IS COMING | omen beats and transitions |
| CORE CONFLICT | conflict scenes and emotional tension |
| EMOTIONAL CURVE | rhythm, peaks, pauses, and release |
| IMMERSIVE EXPERIENCE | audience movement through the film |
| VISUAL WORLD | only high-level scene temperament, not design |
| SCENE POTENTIALS | storyboard beats and scene progression |

## Output Protocol

Always output a:

> Storyboard Package (SBP)

For the reusable template, read `references/storyboard-package.md`.

SBP must contain:
- Slide Sequence
- Silent Slides
- Emotional Peaks
- Transition Slides
- Narrative Rhythm
- Scene Progression

## Strict Rules

### RULE 1

Do not re-analyze the world.

### RULE 2

Do not regenerate the Narrative.

Use the NWP as the source of truth.

### RULE 3

Do not design visuals.

Forbidden:
- layout
- typography
- image prompts
- color palette
- composition
- rendering rules

### RULE 4

The output is not a final deck.

It is:

> the cinematic skeleton of the Slide Cinema.

## Final Principle

This skill does not decide what the world means.

It decides:

> how the film moves.
