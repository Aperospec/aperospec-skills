# Aperospec Runtime Protocol

Use this protocol when the user asks to run the full pipeline.

## Input

Runtime may receive:
- Runtime Injection Map (RIM)
- project topic
- original materials
- Existing Scene Library

If a valid RIM is provided from `aperospec-injection`, apply it first.
Locked content must remain locked.
Skip / Assisted Generation / Continue Generation rules must be respected before entering Stage 1.

Normalize unresolved upstream material into the Stage 1 input only.

Do not pass raw input to later stages.

## Optional Stage 0: aperospec-injection

If present, read:

> Runtime Injection Map (RIM)

Use it to determine:
- which layer is already fixed
- which stage should be skipped
- which stage should run in Assisted Generation mode
- which content is locked and cannot be rewritten

## Stage 1: aperospec-project

Call:

> `aperospec-project.skill`

Allowed Context:
- project topic
- original materials
- Existing Scene Library

Output:

> Cognitive World Package (CWP)

Freeze:

> CWP is frozen immediately after generation.

## Stage 2: aperospec-cinema

Call:

> `aperospec-cinema.skill`

Allowed Context:

> CWP only.

Forbidden:
- original project documents
- user extra explanation
- CDP
- VDP
- Final Deck

Output:

> Narrative World Package (NWP)

Freeze:

> NWP is frozen immediately after generation.

## Stage 3: aperospec-conceptdeck

Call:

> `aperospec-conceptdeck.skill`

Allowed Context:

> NWP only.

Forbidden:
- original project documents
- CWP
- VDP
- rendering instructions

Output:

> Concept Deck Package (CDP)

Freeze:

> CDP is frozen immediately after generation.

## Stage 4: aperospec-visualdirector

Call:

> `aperospec-visualdirector.skill`

Allowed Context:

> CDP only.

Forbidden:
- original project documents
- CWP
- NWP
- upstream analysis

Output:

> Visual Directing Package (VDP)

Freeze:

> VDP is frozen immediately after generation.

## Stage 5: Rendering Agent

Call:

> Rendering Agent

Allowed Context:

> VDP only.

Forbidden:
- CWP
- NWP
- CDP
- original project documents

Output:

> Final Slide Cinema as a deliverable `.pptx` file.

Rendering Rule:

Stage 5 must execute final rendering.

Rendering must:
- read VDP as the only creative source
- call GPT Image 2 to generate each page's Hero Image
- insert each Hero Image into its corresponding slide as the primary visual body
- render all pages into a deliverable `.pptx` file
- strictly follow VDP and not redesign Narrative

Forbidden:
- outputting only text
- outputting only VDP
- outputting only image prompts
- outputting only a concept plan

## Artifact Chain

Preserve internally:

`CWP -> NWP -> CDP -> VDP -> Final Deck`

## User Visibility

Default user-facing output:

> Final Slide Cinema.

Intermediate artifacts are internal build artifacts unless the user asks to inspect them.

## Pipeline Debug

If the final deck fails because of Narrative drift, corporate PPT style, emotional fracture, missing shot feeling, or broken rhythm, inspect the artifact chain:
- CWP
- NWP
- CDP
- VDP
- Final Deck

Find which boundary failed before rewriting anything.

## Context Isolation Checklist

Before each stage, confirm:
- The stage sees only the allowed artifact.
- Frozen upstream artifacts are not modified.
- No later-stage content leaks backward.
- The skill only performs its assigned responsibility.
