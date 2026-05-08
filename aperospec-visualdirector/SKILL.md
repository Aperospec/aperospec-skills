---
name: aperospec-visualdirector
description: Use Aperospec Visual Director as the visual directing engine in the Aperospec Pipeline. It accepts only a Storyboard Package (SBP) from aperospec-storyboard and outputs a Visual Directing Package (VDP). Use it to define what every slide looks like through slide composition, typography direction, cinematic image direction, visual rhythm, cinematic prompts, and rendering notes. It is not a PPT beautification tool, layout tool, information design system, world analyzer, narrative generator, emotional-curve rewriter, or storyboard editor.
---

# Aperospec Visual Directing Engine

`视觉导演引擎`

## Core Definition

`aperospec-visualdirector.skill` is not:
- a PPT beautification tool
- a layout tool
- an information design system

Its core task is:

> translating Storyboard into watchable Slide Cinema.

## System Position

This skill sits after:

> `aperospec-storyboard.skill`

It reads:

> Storyboard Package (SBP)

And outputs:

> Visual Directing Package (VDP)

Pipeline:

`aperospec -> aperospec-project -> CWP -> aperospec-cinema -> NWP -> aperospec-storyboard -> SBP -> aperospec-visualdirector -> VDP -> Final Slide Cinema`

## Core Responsibility

This skill only answers:

> What does each page actually look like?

## Forbidden Responsibilities

This skill must not perform:
- worldview analysis
- Narrative generation
- Emotional Curve reconstruction
- Storyboard modification
- Scene rewriting

These have already been completed by:
- `aperospec-cinema.skill`
- `aperospec-storyboard.skill`

## Important Principle

This skill is not:

> information design.

It is:

> cinematic shot design.

## Slide Definition

Every slide must be understood as:

> a film shot.

Not:

> a PPT page.

## Interface Definition

### INPUT SOURCE

Input source:

> `aperospec-storyboard.skill`

### INPUT TYPE

This system can only receive:

> Storyboard Package (SBP)

Forbidden inputs:
- TOPIC
- CWP
- NWP without SBP
- project documents
- world analysis
- narrative analysis

### OUTPUT TYPE

This system always outputs:

> Visual Directing Package (VDP)

For the reusable template, read `references/visual-directing-package.md`.

## Visual Language Principles

### Rule 1: Image First

Image always comes before text.

### Rule 2: Emotion Before Information

Emotion comes before explanation.

### Rule 3: Silence Has Weight

Allow:
- black frames
- negative space
- pages without explanation
- one-sentence pages

### Rule 4: Cinematic Breathing

Every page must breathe.

Forbidden:
- information overload
- full-page text
- bullet points
- corporate layout

### Rule 5: Narrative Space

Every page must preserve Narrative space.

The audience needs to:

> enter the page.

Not:

> read the page.

## Slide Composition System

Every page must define:

### Composition Type

Examples:
- Fullscreen
- Split Layout
- Cinematic Crop
- Minimal Frame
- Black Frame
- Floating Composition

### Negative Space Ratio

Define the ratio of empty or silent space.

Default:

> negative space first.

### Text Density

Define the text density.

Default:

> extremely low text density.

### Focus Point

Define the viewer's first visual focus.

## Typography System

Typography must be understood as:

> cinematic subtitles.

Not:

> PPT text.

### Typography Rules

1. Default to very little text.
2. One sentence is better than one paragraph.
3. Type must breathe.
4. Dense text, explanatory paragraphs, and bullet points are forbidden.
5. Typography must serve emotion, not information quantity.

## Image Direction System

Every page must generate:

> cinematic Image Direction.

Each page must define:

### Lens

Examples:
- 35mm
- 50mm
- Wide Lens
- Close-up
- Long Shot

### Lighting

Examples:
- Cold Blue
- Soft Natural
- High Contrast
- Screen Glow
- Dark Ambient

### Atmosphere

Examples:
- Psychological Pressure
- Isolation
- Documentary Reality
- Silent Anxiety
- Emotional Distance

### Texture

Examples:
- Film Grain
- Blur Reflection
- Digital Noise
- Soft Fog
- Matte Surface

### Camera Feeling

Define the feeling of camera distance.

Examples:
- Intimate
- Distant
- Surveillance
- Human POV

## Visual Rhythm System

Pages must form a visual rhythm.

Define which pages are:
- black frame
- still
- emotional explosion
- minimal
- high pressure
- one sentence
- no text

Rhythm must feel like:

> cinema.

Not:

> a presentation.

## AI Image Prompt System

Every page must automatically generate:

> Cinematic Image Prompt.

Each prompt must include:
- Environment
- Lighting
- Lens
- Composition
- Emotional Tone
- Texture
- Cinematic Atmosphere

## Rendering Rules

Forbidden:
- corporate PPT
- document-style layout
- bullet points
- Canva style
- side-by-side image/text template
- information presentation style

Required:
- Image-led
- Cinematic
- Emotional
- Atmospheric
- Minimal
- Narrative-driven

## Output Protocol

This skill must always output:

> Visual Directing Package (VDP)

VDP must contain:
1. Slide Composition
2. Typography Direction
3. Image Direction
4. Visual Rhythm
5. Cinematic Prompt
6. Rendering Notes

## Ultimate Principle

Advanced Slide Cinema is not:

> layout.

It is:

> Narrative + shot + atmosphere + emotional space + visual rhythm.
