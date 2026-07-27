# Runtime Protocol

Use this protocol when the user asks to run the full Aperospec slide-deck pipeline or when an active request genuinely spans multiple pipeline Skills.

Do not apply it to unrelated tasks or requests that one Skill can handle directly.

## Input

Runtime may receive:
- Runtime Injection Map (RIM)
- project topic
- original materials
- Existing Scene Library

If a valid RIM is provided from `injection`, apply it first.
Locked content must remain locked.
Skip / Assisted Generation / Continue Generation rules must be respected before entering Stage 1.

Normalize unresolved upstream material into the Stage 1 input only.

Do not pass raw input to later stages.

## Runtime Role

Runtime is the user's direct PM for the active Aperospec slide-deck pipeline.

It is responsible for:
- accepting the full project brief
- choosing the correct pipeline entry point
- preserving artifact boundaries
- deciding whether to continue, pause, reroute, rework, or escalate to the user

It is not responsible for:
- creating worldview
- rewriting narrative
- inventing visual content
- overriding locked assets

## User Confirmation Checkpoints

Runtime may continue without asking only when the pipeline is moving normally from one validated stage to the next.

Runtime must stop and ask the user when:
- project direction changes
- a new existing asset is introduced after the pipeline has already started
- a locked asset conflicts with downstream generation
- rollback to an earlier stage is required
- the Final Deck is ready for acceptance

## Injection Re-entry Decision

If new existing content appears mid-pipeline, Runtime must decide whether it changes the layer map.

Use the following rule:
- if the new content only clarifies the current unresolved stage, keep the current stage and continue
- if the new content introduces new locked names, prebuilt structure, narrative material, or visual guidelines from another layer, rerun `injection`
- if the new content changes Skip / Lock / Assisted Generation decisions, rerun `injection`

## Optional Stage 0: injection

If present, read:

> Runtime Injection Map (RIM)

Use it to determine:
- which layer is already fixed
- which stage should be skipped
- which stage should run in Assisted Generation mode
- which content is locked and cannot be rewritten

## Stage 1: project

Call:

> `project.skill`

Allowed Context:
- project topic
- original materials
- Existing Scene Library

Output:

> Cognitive World Package (CWP)

Freeze:

> CWP is frozen immediately after generation.

## Stage 2: cinema

Call:

> `cinema.skill`

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

## Stage 3: conceptdeck

Call:

> `conceptdeck.skill`

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

## Stage 4: visualdirector

Call:

> `visualdirector.skill`

Allowed Context:

> CDP only.

Exception:
- Style DNA Map from RIM may be included only when `injection` classified user reference images as Style Reference Only.
- Style DNA is a late-stage visual execution input. It must enter only after CDP is frozen.

Forbidden:
- original project documents
- CWP
- NWP
- upstream analysis
- raw reference images as semantic content
- reference-image subjects, objects, characters, logos, scenes, layouts, poses, or narrative events

Output:

> Visual Directing Package (VDP)

Freeze:

> VDP is frozen immediately after generation.

VDP must be complete enough for Stage 5 to render without inventing:
- missing copy logic
- page role
- page energy level
- typography / image relationship
- fallback poster structure
- Style DNA application rules when Style Reference Only images are provided
- forbidden-transfer boundaries for reference-image content

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

If image generation fails on a page:
- retry generation for that page
- preserve the page's narrative role and VDP instruction
- do not rewrite upstream artifacts to compensate for rendering weakness

If slide assembly fails:
- retry slide execution without modifying `VDP`
- keep all upstream artifacts frozen

Stage 5 completion requires:
- every intended slide exists
- every intended Hero Image is present or explicitly marked as approved fallback
- no locked formal name is altered
- no corporate PPT fallback layout replaces the VDP-defined narrative poster logic
- no missing VDP field forces generic left-text/right-image safety layout

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

## Rework Matrix

Use the first failed boundary to decide the restart point.

| Observed failure | First failed artifact | Restart from |
| --- | --- | --- |
| Root cause feels false, weak, or shallow | CWP | Stage 1 |
| Narrative world or emotional universe misreads a valid CWP | NWP | Stage 2 |
| Deck rhythm, concept sequence, or page cognition breaks a valid NWP | CDP | Stage 3 |
| Visual hierarchy or content fidelity breaks a valid CDP | VDP | Stage 4 |
| Images, slide assembly, or export drift from a valid VDP | Final rendering | Stage 5 |

Rework rule:
- preserve every validated upstream artifact
- do not restart earlier stages without a stated reason
- if the user changes direction, restart from the earliest affected stage

## Locked Asset Conflict Rule

If downstream generation conflicts with a locked formal name, chapter, exhibit item, or existing structure:
- pause the pipeline
- preserve the locked asset unchanged
- report the conflict to the user
- resume only after the user confirms the authority rule

Runtime must not silently "optimize" the locked asset.

## Context Isolation Checklist

Before each stage, confirm:
- The stage sees only the allowed artifact.
- Frozen upstream artifacts are not modified.
- No later-stage content leaks backward.
- The skill only performs its assigned responsibility.

## Completion Checklist

Before declaring the pipeline complete, confirm:
- the correct entry point was used
- all frozen artifacts remain preserved
- no locked asset was renamed or rewritten
- any interruption was classified and handled by rule
- the Final Deck meets Stage 5 completion requirements
- the user has been asked for final acceptance
