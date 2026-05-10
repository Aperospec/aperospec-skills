---
name: aperospec-runtime
description: Use Aperospec Runtime as the non-creative orchestration layer for the full Aperospec Pipeline. It controls the pipeline like an industrial production line: runs skills in order, isolates context, passes only the required artifact to each stage, freezes CWP/NWP/CDP/VDP artifacts, preserves internal build artifacts for debugging, and prevents context pollution. It does not create worldview, narrative, concept deck, visual design, or rendering.
---

# Aperospec Runtime Orchestrator

`流水线总控系统`

## Core Definition

`aperospec-runtime.skill` is not a creative skill.

It does not handle:
- worldview
- Narrative
- concept deck
- visual design

Its only responsibility is:

> controlling the entire Pipeline so it runs correctly.

## System Position

This skill sits above all other skills.

It is responsible for:
- calling skills in sequence
- isolating context
- passing artifacts
- locking responsibility boundaries
- controlling runtime

## Runtime Principle

Pipeline must run:

> like an industrial production line.

## Most Important Rule

Each skill may only see:

> the content it is supposed to see.

Forbidden:

> Context Pollution.

## Runtime Structure

For the detailed execution template, read `references/runtime-protocol.md`.

### Optional Stage 0: Injection Handoff

If the upstream input is a Runtime Injection Map (RIM) from `aperospec-injection.skill`, Runtime must:
- respect the detected layer
- respect Lock / Skip / Assisted Generation decisions
- preserve locked content before any downstream generation
- start the pipeline from the first unresolved stage

If no RIM is provided, Runtime starts from Stage 1.

### Stage 1: Cognitive Engine

Call:

> `aperospec-project.skill`

Input:
- project topic
- original materials
- Existing Scene Library

Output:

> Cognitive World Package (CWP)

Runtime Rule:

After CWP is generated, immediately freeze it.

Later skills must not modify it.

### Stage 2: Narrative Universe

Call:

> `aperospec-cinema.skill`

Allowed Context:

> CWP only.

Forbidden Context:
- original project documents
- extra user explanation
- later-stage content

Output:

> Narrative World Package (NWP)

Runtime Rule:

Cinema is only responsible for:

> Narrative Universe.

Forbidden:
- concept deck
- visual design

### Stage 3: Concept Deck

Call:

> `aperospec-conceptdeck.skill`

Allowed Context:

> NWP only.

Forbidden Context:
- original project documents
- CWP
- Visual Direction

Output:

> Concept Deck Package (CDP)

Runtime Rule:

Concept Deck is only responsible for:

> Concept Narrative.

Forbidden:
- visual design
- rendering

### Stage 4: Visual Director

Call:

> `aperospec-visualdirector.skill`

Allowed Context:

> CDP only.

Forbidden Context:
- original project documents
- CWP
- NWP

Output:

> Visual Directing Package (VDP)

Runtime Rule:

Visual Director is only responsible for:

> page visuals.

Forbidden:
- rethinking worldview
- rethinking Narrative
- rethinking Emotional Curve

### Stage 5: Rendering Agent

Call:

> Rendering Agent

Allowed Context:

> VDP only.

Output:

> Final Slide Cinema as a deliverable `.pptx` file.

Runtime Rule:

Stage 5 must execute final rendering.

It must:
- read VDP as the only creative source
- call GPT Image 2 to generate each page's Hero Image
- insert each Hero Image into its corresponding slide as the primary visual body
- render all pages into a deliverable `.pptx` file

Forbidden:

- automatically redesigning Narrative
- outputting only text
- outputting only VDP
- outputting only image prompts
- outputting only a concept plan

## Artifact System

Pipeline must automatically preserve:
- CWP
- NWP
- CDP
- VDP
- Final Deck

## Artifact Rule

These are:

> Internal Build Artifacts.

By default, the user does not need to review them.

## User Interaction Rule

By default, the user only sees:

> Final Slide Cinema.

Intermediate artifacts are used internally unless the user asks to inspect or debug the pipeline.

## Runtime Failure Rule

If the Final Deck shows:
- Narrative drift
- corporate PPT degradation
- emotional fracture
- missing shot feeling
- collapsed slide rhythm

Then preserve:
- CWP
- NWP
- CDP
- VDP
- Final Deck

Use them for:

> Pipeline Debug.

## Most Important Principle

The core of a truly advanced Pipeline is not:

> Prompt.

It is:

> Context Isolation.

## Ultimate Goal

This system is not:

> automatically generating PPT.

It is:

> automatically producing Slide Cinema like a film-industry pipeline.
