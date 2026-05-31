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
For the management-layer PM rules, read `references/runtime-management-rules.md`.
For team productivity standards, read `/TEAM_PRODUCTIVITY_PROTOCOL.md` and `/PIPELINE_ACCEPTANCE_CHECKLIST.md`.

## Runtime Authority

`aperospec-runtime` is the only orchestration role allowed to:

- receive the full project request
- decide which stage starts first
- route work across the Pipeline
- freeze or preserve artifacts
- decide whether the issue is a stage failure or a rendering failure

It must not:

- replace the user's creative judgment
- silently rewrite locked content
- let downstream skills directly negotiate scope with the user

## User Approval Rule

Runtime may silently continue only when:

- the project direction is unchanged
- no locked asset is being modified
- no existing formal name is being replaced
- the next stage is a normal downstream translation

Runtime must return to the user for confirmation when:

- the project direction changes
- a new existing asset is inserted mid-pipeline
- a locked name, chapter, exhibit item, or structure conflicts with downstream generation
- the pipeline must roll back to an earlier stage
- the final deck is ready for acceptance

## Injection Re-entry Rule

If the user adds new existing content after the pipeline has already started, Runtime must first decide whether that content changes the resolved layer map.

If it does, Runtime must send the material back through `aperospec-injection` before continuing.

Runtime must not manually improvise a new layer decision when a new asset changes lock, skip, or assisted-generation logic.

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

Exception:
- Style DNA Map from a Runtime Injection Map may be included only when `aperospec-injection` classified user reference images as Style Reference Only.

Forbidden Context:
- original project documents
- CWP
- NWP
- raw reference images as semantic content
- Style Reference Only images before they have been converted into Style DNA Map

Output:

> Visual Directing Package (VDP)

Runtime Rule:

Visual Director is only responsible for:

> page visuals.

Forbidden:
- rethinking worldview
- rethinking Narrative
- rethinking Emotional Curve
- copying subjects, objects, characters, logos, scenes, layouts, poses, or narrative events from Style Reference Only images

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

## Rework Rule

Runtime must not restart the whole pipeline by default.

When a failure appears, Runtime must first identify the failing boundary:

- `CWP` failure: wrong root cause, wrong driving force, wrong future projection, or wrong cognitive trigger logic
- `NWP` failure: wrong narrative world, emotional environment, or core conflict translation despite a valid `CWP`
- `CDP` failure: wrong concept sequencing, rhythm, page cognition, or emotional advancement despite a valid `NWP`
- `VDP` failure: wrong visual hierarchy, poster logic, or content-fidelity execution despite a valid `CDP`
- Rendering failure: the `VDP` is valid, but image generation, slide assembly, or final deck execution drifts

Rework must restart from the first failed artifact and preserve every validated upstream artifact.

## Interruption Rule

If the user interrupts the pipeline with a new request, Runtime must classify the interruption as one of the following:

- Direction Change
- Existing Asset Injection
- Locked Asset Conflict
- Final Rendering Fix
- Surface Rendering Fix

Runtime behavior:

- Direction Change: return to the user, confirm the new direction, then restart from the earliest affected stage
- Existing Asset Injection: rerun `aperospec-injection` first
- Locked Asset Conflict: pause and ask the user to decide which asset has authority
- Final Rendering Fix: keep `VDP` frozen and retry Stage 5 only
- Surface Rendering Fix: keep upstream artifacts frozen and retry only the rendering or slide-assembly layer

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

## Final Acceptance Rule

Runtime must not treat Stage 5 as complete only because a `.pptx` file exists.

The final deck is complete only when:

- every intended page is rendered
- every page has its corresponding Hero Image or an explicitly approved fallback
- the deck follows `VDP` without narrative redesign
- no locked names are altered
- the deck avoids obvious corporate PPT degradation
- the output is ready for user review

If any of these conditions fail, Stage 5 remains incomplete.

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
