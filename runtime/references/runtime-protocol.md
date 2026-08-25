# Runtime Protocol

Use this protocol when the user asks to run the full Aperospec slide-deck pipeline or when an active request genuinely spans multiple pipeline Skills.

Do not apply it to unrelated tasks or requests that one Skill can handle directly.

## Input

Runtime may receive:
- Runtime Injection Map (RIM)
- project topic
- original materials
- completed Aperospec V2 Stage 1 model, when already available
- user-selected focus, when already explicit
- optional user-confirmed Aperospec Stage 2 position and interest lock for a strategy-bearing deck
- Existing Scene Library
- confirmed final-output format
- active channel profile, when one is required
- Evidence Lock containing approved claims, exact names, required limitations, rights notes, and source metadata
- optional Brand Visual Lock containing human-approved, durable visual-identity relationships

If a valid RIM is provided from `injection`, apply it first.
Locked content must remain locked.
Skip / Assisted Generation / Continue Generation rules must be respected before entering Pipeline Stage 1.

Normalize unresolved upstream material into the Aperospec Stage 1 input only.

Do not pass raw input to later stages.

## Runtime Role

Runtime is the user's direct PM for the active Aperospec V2 slide-deck pipeline.

It is responsible for:
- accepting the full project brief
- choosing the correct pipeline entry point
- establishing or validating the Aperospec V2 Stage 1 model
- preserving the user's authority over focus selection and Stage 2 interests
- activating only the required channel profile
- preserving artifact boundaries
- deciding whether to continue, pause, reroute, rework, or escalate to the user

It is not responsible for:
- creating worldview
- rewriting narrative
- inventing visual content
- overriding locked assets

## User Confirmation Checkpoints

Apply the material-gate and autonomy rules in `runtime-management-rules.md`.

Runtime continues through ordinary professional and technical decisions without asking. It stops only for an unresolved material gate, a requested stage-by-stage checkpoint, a lock or authority conflict, a required rollback, a material quality downgrade, or final acceptance / external authorization.

Do not ask again for a decision the human already supplied earlier in the pipeline.

## Injection Re-entry Decision

If new existing content appears mid-pipeline, Runtime must decide whether it changes the layer map.

Use the following rule:
- if the new content only clarifies the current unresolved stage, keep the current stage and continue
- if the new content can change the active frame, material contradictions, temporal formation, operating force field, baseline future judgment, or focus set, reopen Aperospec Stage 1
- if the new content explicitly changes the user's selected focus or confirmed Stage 2 interests, update the corresponding user-owned lock and restart from the earliest affected artifact
- if the new content introduces new locked names, prebuilt structure, narrative material, or visual guidelines from another layer, rerun `injection`
- if the new content changes Skip / Lock / Assisted Generation decisions, rerun `injection`

## Optional Stage 0: injection

If present, read:

> Runtime Injection Map (RIM)

Use it to determine:
- whether supplied material reopens Aperospec Stage 1 or explicitly updates a user-owned focus or Stage 2 lock
- which layer is already fixed
- which stage should be skipped
- which stage should run in Assisted Generation mode
- which content is locked and cannot be rewritten

## Optional Stage 0A: Evidence and Channel Lock

When the output depends on current public facts, third-party materials, source attribution, commercial claims, or platform-specific release constraints:

1. activate the one required channel profile;
2. separate signal, fact, opinion, inference, visual reference, and locked asset;
3. verify unstable claims before creative production;
4. freeze an Evidence Lock containing only approved claims, exact names, required limitations, rights notes, and source/caption metadata.

Do not pass raw research pages, social posts, or unverified claims downstream. A channel profile may add checkpoints, but it does not create another Runtime.

## Stage 0B: Aperospec V2 Upstream Gate

Before Pipeline Stage 1 (`project`), Runtime must establish an `Aperospec Upstream Lock`.

### Stage 1 Reality Model

If a completed and valid Aperospec V2 Stage 1 model is not already supplied, invoke Aperospec Stage 1 with the project topic, approved original materials, RIM impact classification, and Evidence Lock.

The Stage 1 result must contain:

- active frame and its limits
- material contradictions
- temporal formation
- actors' positions and operating force field
- baseline future judgment
- causally grounded focus set
- evidence status, material unknowns, and revision signals

### User Focus Selection

The user selects one focus from the focus set or names another focus grounded in the analysis.

- Runtime may compare factual attributes such as urgency, scope, reversibility, evidence strength, and time sensitivity.
- Runtime, Project, downstream Skills, channel conventions, and prior biography must not choose or rank the focus for the user.
- If the user already selected the focus in the current brief, record it without asking again.
- Formal production cannot enter Pipeline Stage 1 until the Stage 1 model and user-selected focus are both locked.

Freeze:

> `Aperospec Upstream Lock = Stage 1 reality model + user-selected focus`

### Optional Stage 2 Strategic Lock

Use Aperospec Stage 2 only when the user requests strategic judgment or the deck must advance a subject's concrete strategy.

Before strategy enters the pipeline, the user must confirm:

- represented subject
- underlying interest drivers and their priority
- desired direction
- resources, capabilities, dependencies, and vulnerabilities
- time horizon
- acceptable and unacceptable loss

Freeze these confirmed fields as the `Aperospec Stage 2 Lock`. Do not infer them from the selected focus or user biography.

## Pipeline Stage 1: project

Call:

> `project.skill`

Allowed Context:
- Aperospec Upstream Lock
- project topic and only the approved original materials needed to preserve factual meaning
- Existing Scene Library
- Evidence Lock, when present
- optional Aperospec Stage 2 Lock, only for a strategy-bearing deck

Output:

> Cognitive World Package (CWP)

Freeze:

> CWP is frozen immediately after generation.

The CWP must translate the valid upstream lock. Project may not reopen the focus choice or reduce the Stage 1 model to a single root cause.

## Pipeline Stage 2: cinema

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

## Pipeline Stage 3: conceptdeck

Call:

> `conceptdeck.skill`

Allowed Context:

> NWP, plus the minimal Evidence Lock fields required to write accurate copy.

Evidence Lock may contribute only:
- approved claims
- exact product / project / person names
- required limitations and uncertainty labels
- source and caption metadata
- content or voice constraints explicitly locked by the user

Forbidden:
- original project documents
- CWP
- VDP
- rendering instructions
- raw research pages or unverified source material

Output:

> Concept Deck Package (CDP)

Freeze:

> CDP is frozen immediately after generation.

## Pipeline Stage 4: visualdirector

Call:

> `visualdirector.skill`

Allowed Context:

> CDP, plus only the optional locked visual-system inputs and output constraints listed below.

Exception:
- Style DNA Map from RIM may be included only when `injection` classified user reference images as Style Reference Only.
- Style DNA is a late-stage visual execution input. It must enter only after CDP is frozen.
- A Brand Visual Lock may be included only when Runtime records it as human-approved and Locked.
- Confirmed output format and active channel visual constraints may be included only to shape the VDP handoff.

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

> If no material Visual / Brand Direction Gate is active, freeze the validated VDP immediately after generation.

> If a material gate is active, VisualDirector first provides the representative proofs and a Human Decision Card. Runtime waits for approval, records the selected relationship, then generates and freezes the formal VDP. A formal VDP cannot be frozen with a pending material gate.

VDP must be complete enough for Stage 5 to render without inventing:
- missing copy logic
- page role
- page energy level
- visual reading and Art Direction thesis
- editorial hierarchy and primary visual task
- typography / image relationship
- typography personality and semantic line-break intent
- asset role, evidence role, and approved fallback structure
- Style DNA application rules when Style Reference Only images are provided
- Brand Visual Lock application and conflict notes when present
- forbidden-transfer boundaries for reference-image content
- crop intent, protected regions, safe zones, and small-size survival rules
- renderer tolerances, execution plan, QA proof, and repair routing
- target format and active channel constraints

## Pipeline Stage 5: Rendering Agent

Call:

> Rendering Agent

Before execution, read:

> `references/rendering-contract.md`

Allowed Context:

> Locked VDP and only the assets, fonts, backend resources, and channel specifications explicitly enumerated by that VDP.

Forbidden:
- CWP
- NWP
- CDP
- original project documents

Output:

> Final Output in the human-confirmed format.

Examples include a `.pptx`, PDF, HTML deck, image sequence, or a channel-specific package. A channel profile may define companion artifacts, but it may not change the locked creative direction.

Rendering Rule:

Pipeline Stage 5 must execute final rendering.

Rendering must:
- read VDP as the only creative source
- use the confirmed renderer and output format
- generate a Hero Image only where the VDP calls for one
- preserve screenshots, evidence, diagrams, or supplied assets when the VDP assigns them the visual role
- assemble every intended page or card into the confirmed deliverable
- compose exact text deterministically and preserve semantic line breaks, approved short variants, and `Do Not Compress` content
- convert crop intent and protected regions into exact execution coordinates
- run the technical QA defined by the rendering contract and active channel profile
- strictly follow VDP and not redesign Narrative

If image generation fails on a page:
- retry generation for that page
- preserve the page's narrative role and VDP instruction
- do not rewrite upstream artifacts to compensate for rendering weakness

If slide assembly fails:
- retry slide execution without modifying `VDP`
- keep all upstream artifacts frozen

Pipeline Stage 5 completion requires:
- every intended page or card exists
- every required Hero Image, screenshot, diagram, or evidence asset is present or explicitly marked as an approved fallback
- no locked formal name is altered
- no generic safe layout replaces the VDP-defined visual logic
- no missing VDP field forces generic left-text/right-image safety layout
- actual exports pass overflow, crop, safe-area, contrast, resolution, font, and file-integrity inspection
- any material quality downgrade or unresolved Acceptance Gate has been returned to Runtime

Forbidden:
- outputting only text
- outputting only VDP
- outputting only image prompts
- outputting only a concept plan

## Artifact Chain

Preserve internally:

`RIM / Evidence Lock (when needed) -> Aperospec Stage 1 -> user-selected focus -> Aperospec Upstream Lock -> [optional Stage 2 Lock] -> CWP -> NWP -> CDP -> [Style DNA / Brand Visual Lock when approved] -> VDP -> Final Output`

## User Visibility

Default user-facing output:

> The final artifact in the confirmed format.

Intermediate artifacts are internal build artifacts unless the user asks to inspect them.

## Pipeline Debug

If the final output fails because of factual drift, Narrative drift, generic layout, emotional fracture, missing visual evidence, or broken rhythm, inspect the artifact chain:
- Evidence Lock, when present
- Aperospec Upstream Lock and optional Stage 2 Lock
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
| Active frame, temporal formation, operating force field, baseline future, or focus set is false, weak, or contradicted | Aperospec Stage 1 model | Stage 0B / Aperospec Stage 1 |
| User-selected focus or confirmed Stage 2 interests changed | Aperospec user-owned lock | Stage 0B focus selection / Stage 2 clarification |
| CWP mis-translates a valid Aperospec Upstream Lock | CWP | Pipeline Stage 1 |
| Narrative world or emotional universe misreads a valid CWP | NWP | Pipeline Stage 2 |
| Copy, title promise, deck rhythm, concept sequence, or page cognition breaks a valid NWP / Evidence Lock | CDP | Pipeline Stage 3 |
| Visual hierarchy or content fidelity breaks a valid CDP | VDP | Pipeline Stage 4 |
| Image realization, crop, overflow, slide assembly, resolution, or export drifts from a valid VDP | Final rendering | Pipeline Stage 5 |
| A claim, source, limitation, or rights status is wrong | Evidence Lock | Stage 0A |

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
- The Aperospec Upstream Lock contains a user-selected focus, not an Agent-selected priority.
- Any Stage 2 strategic fields are user-confirmed and remain separate from the Stage 1 reality model.
- The active channel profile contributes only its declared constraints.
- Frozen upstream artifacts are not modified.
- No later-stage content leaks backward.
- The skill only performs its assigned responsibility.

## Completion Checklist

Before declaring the pipeline complete, confirm:
- the correct entry point was used
- the Aperospec V2 Stage 1 model was completed and the focus was selected by the user
- no unconfirmed interest function or strategic direction entered the artifact chain
- all frozen artifacts remain preserved
- no locked asset was renamed or rewritten
- any interruption was classified and handled by rule
- the Final Output meets Stage 5 and active channel-profile completion requirements
- the user has been asked for final acceptance
