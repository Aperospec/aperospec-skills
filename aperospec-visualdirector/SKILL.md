---
name: aperospec-visualdirector
description: Use Aperospec Visual Director as the visual directing engine in the Aperospec Pipeline. It accepts only a Storyboard Package (SBP) from aperospec-storyboard and outputs a Visual Directing Package (VDP): slide composition, typography system, image direction, visual rhythm, AI image prompts, and rendering rules. It answers what each page should look like. It does not analyze the world, generate CWP/NWP/SBP, or alter storyboard structure.
---

# Aperospec Visual Director Engine

`视觉导演引擎`

## Core Definition

This skill turns:

> Storyboard

Into:

> watchable Slide Cinema.

It answers:

> What does each page actually look like?

## Pipeline Position

`aperospec -> aperospec-project -> CWP -> aperospec-cinema -> NWP -> aperospec-storyboard -> SBP -> aperospec-visualdirector -> VDP -> Final Slide Cinema`

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

## Context Isolation Rule

Visual Director can only see:

> Storyboard Package (SBP)

It must not reread:
- project documents
- world cognition
- Narrative analysis
- upstream source material

Otherwise, it will start thinking again.

## VDP Output Protocol

For the reusable template, read `references/visual-directing-package.md`.

VDP must contain:
- Slide Composition
- Typography System
- Image Direction
- Visual Rhythm
- AI Image Prompt
- Rendering Rules

## Slide Composition

Define:
- full-screen / split layout
- composition
- negative space
- black frame ratio
- visual hierarchy

## Typography System

Define:
- font size
- density
- alignment
- breathing
- minimalism

## Image Direction

Define:
- camera distance
- lighting
- atmosphere
- grain
- blur
- texture
- photographic language

## Visual Rhythm

Define:
- which page is still
- which page is black frame
- which page has only one sentence
- which page is emotional impact

## AI Image Prompt

Every page must generate a cinematic image prompt.

Each prompt must include:
- atmosphere
- lighting
- framing
- lens
- emotional tone
- environment
- cinematic texture

## Rendering Rules

Must enforce:

> Image-led Slides.

Forbidden:
- document layout
- bullet points
- corporate PPT
- long text blocks

## Strict Rules

### RULE 1

Do not change storyboard order.

### RULE 2

Do not reinterpret Narrative.

### RULE 3

Do not analyze the original topic.

### RULE 4

All final pages must be Image-led.

## Final Principle

This skill does not think through the world.

It directs:

> how the film should be seen.
