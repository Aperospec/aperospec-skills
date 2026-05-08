---
name: aperospec-runtime
description: Use Aperospec Runtime as the orchestration layer for the full Aperospec Pipeline. It does not create cognition, narrative, storyboard, visual design, or rendering. It only runs skills in order, isolates context, passes artifacts, locks responsibility boundaries, and controls pipeline execution from TOPIC to CWP to NWP to SBP to VDP to final slide cinema rendering.
---

# Aperospec Runtime

`流水线总控系统`

## Core Definition

This skill is not a creation layer.

It is a:

> Pipeline orchestration layer.

It does not handle:
- worldview
- Narrative
- storyboard
- visual design
- rendering

It only handles:
- calling skills in sequence
- isolating context
- passing artifacts
- locking responsibility boundaries
- controlling pipeline execution

## Runtime Execution Order

### Step 1

Call:

> `aperospec-project.skill`

Input:

> TOPIC

Output:

> Cognitive World Package (CWP)

### Step 2

Pass only:

> CWP

To:

> `aperospec-cinema.skill`

Output:

> Narrative World Package (NWP)

### Step 3

Pass only:

> NWP

To:

> `aperospec-storyboard.skill`

Output:

> Storyboard Package (SBP)

### Step 4

Pass only:

> SBP

To:

> `aperospec-visualdirector.skill`

Output:

> Visual Directing Package (VDP)

### Step 5

Rendering Agent reads:

> VDP

Output:

> Final Slide Cinema

## Pipeline Rules

### Rule 1

Each skill may only do its own job.

No responsibility pollution.

### Rule 2

Never let one agent simultaneously handle:
- Narrative
- Storyboard
- Visual
- Rendering

Otherwise:

> Context Explosion.

### Rule 3

Visual Director can only see:

> Storyboard.

It must not reread:
- project documents
- world cognition
- Narrative analysis

### Rule 4

Final slides must be:

> Image-led.

Not:

> Text-led.

### Rule 5

The goal is not:

> making PPT.

It is:

> making watchable Slide Cinema.

## Runtime Output

When asked to run the full pipeline, return the artifacts in order:
- CWP
- NWP
- SBP
- VDP
- Final rendering instructions or final slide artifact when requested

For the reusable runtime prompt, read `references/runtime-protocol.md`.

## Final Definition

Aperospec Pipeline is not:

> AI makes PPT.

It is:

> AI cinematic cognition production system.
