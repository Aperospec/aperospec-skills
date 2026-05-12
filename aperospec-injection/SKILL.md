---
name: aperospec-injection
description: Use Aperospec Injection as the content injection and structure fusion engine before aperospec-runtime. It analyzes existing user content, detects which Aperospec Pipeline layer it belongs to, confirms formal names for existing assets, locks confirmed names in Lock Asset State, decides whether each layer should use Full Generation, Assisted Generation, Injection, Lock, Skip, or Continue Generation, and outputs a Runtime Injection Map (RIM). It is not a creative skill and does not create worldview, narrative, concept deck, or visual design.
---

# Aperospec Injection

`内容注入与结构融合引擎`

## Core Definition

`aperospec-injection.skill` is not a creative skill.

It does not handle:
- worldview creation
- Narrative creation
- concept deck creation
- visual creation

Its core responsibility is:

> analyzing existing user content and correctly connecting it to the Aperospec Pipeline.

## System Position

This skill sits before:

> `aperospec-runtime.skill`

It is responsible for:

> content injection.

## Core Responsibility

This skill must:

1. Identify which Pipeline layer the existing content belongs to.
2. Decide which content should be locked, completed, skipped, or continued.
3. Generate a Runtime Injection Map.

It must not:
- rewrite the project direction
- improvise downstream creative content
- rename existing confirmed assets
- bypass Runtime and directly continue the pipeline on its own

## Naming Confirmation System

Injection Layer is responsible for:

> formal naming confirmation for all Existing Assets.

Existing Assets include:
- constructed content
- existing user plans
- confirmed exhibit items
- confirmed chapters
- client-locked content
- existing Narrative Structure
- existing spatial names
- existing function modules

## Once Confirmed

Once Injection Layer confirms a formal name, that name enters:

> Lock Asset State.

## Lock Asset State Rules

After entering Lock Asset State, all downstream Skills are forbidden to:
- rename
- replace with summary wording
- "upgrade" the name
- rename it narratively
- replace it with synonyms
- create a stylized name
- automatically optimize the name with AI

## Allowed Actions

Downstream Skills may only:
- reference
- arrange in layout
- connect through Narrative
- organize rhythm
- structure pages

## Important Naming Principle

Formal names are not decided temporarily by:

> ConceptDeck Layer.

They must be completed in:

> Injection Layer Naming Confirmation.

## Existing Content Protection

User-provided names for the following are treated as Confirmed Assets by default:
- exhibit item names
- exhibition zone names
- chapter names
- spatial names
- constructed content

## Default Naming Rule

Unless the user explicitly requests renaming, downstream Skills are forbidden to:

> modify formal names.

Injection itself must also follow this rule.

## Runtime Handoff Rule

Injection does not continue the pipeline by itself.

After layer detection and lock decisions are complete, Injection must hand off only:
- the detected layer
- the lock decisions
- the skip decisions
- the assisted-generation decisions
- the confirmed formal names

to:

> `aperospec-runtime.skill`

Runtime is the only role allowed to decide actual stage execution order.

## Multiple Asset Rule

If the user provides multiple existing assets across multiple layers, Injection must:
- identify each asset's layer
- preserve each confirmed formal name
- decide which layer is already fixed
- output a single merged RIM

Injection must not collapse all assets into one vague summary if that would erase layer boundaries.

## Important Principle

Real-world projects never start from zero.

Therefore, the Pipeline must support:

> Existing Content Injection.

## Existing Content Types

The system must allow existing:
- worldview
- Narrative
- concept deck
- exhibit items
- brand assets
- visual guidelines
- constructed content
- client requirements
- non-modifiable parts

## Pipeline Layer Recognition

This skill must automatically determine which Pipeline layer the existing content belongs to.

### Layer 1: Cognitive Layer

Includes:
- root-cause analysis
- drive forces
- world understanding
- civilizational structure

Corresponds to:

> `aperospec-project.skill`

### Layer 2: Narrative Layer

Includes:
- worldview
- Emotional Environment
- Narrative Universe
- Emotional Curve

Corresponds to:

> `aperospec-cinema.skill`

### Layer 3: Concept Deck Layer

Includes:
- exhibit items
- Scene
- Concept Sequence
- Cognitive Triggers
- Atmosphere Directions
- Narrative Rhythm

Corresponds to:

> `aperospec-conceptdeck.skill`

### Layer 4: Visual Direction Layer

Includes:
- visual guidelines
- composition
- Typography
- color
- lighting
- brand visuals

Corresponds to:

> `aperospec-visualdirector.skill`

## Detection Rules

Analyze the user's existing content and identify which layer it belongs to.

### Example A: Existing Narrative Document

Runtime Decision:

| Layer | Decision |
| --- | --- |
| Cognitive Layer | Skip |
| Narrative Layer | Lock |
| Concept Deck Layer | Continue Generation |
| Visual Direction Layer | Continue Generation |

### Example B: Existing Exhibit Plan

Runtime Decision:

| Layer | Decision |
| --- | --- |
| Cognitive Layer | Assisted Generation |
| Narrative Layer | Assisted Generation |
| Concept Deck Layer | Lock |
| Visual Direction Layer | Full Generation |

### Example C: Existing Visual Plan

Runtime Decision:

| Layer | Decision |
| --- | --- |
| Visual Direction Layer | Lock |
| Rendering Layer | Continue Rendering |

## Runtime Modes

Every layer must support:

### 1. Full Generation Mode

Generate completely.

### 2. Assisted Generation Mode

Complete missing parts based on existing content.

### 3. Injection Mode

Inject existing content into the specified layer.

### 4. Lock Mode

Do not modify existing content.

## Lock Rules

After a layer enters Lock Mode, the system must not:
- modify
- rewrite
- delete
- reconstruct Narrative
- rewrite Scenes
- change Emotional Logic

## Injection Principles

The system must prioritize:

> preserving existing content.

Not:

> regenerating from scratch.

## Important Rule

The core of an advanced Pipeline is not:

> generation ability.

It is:

> fusion ability.

## Output Protocol

This skill must output:

> Runtime Injection Map (RIM)

For the reusable template, read `references/runtime-injection-map.md`.

RIM must contain:
- Existing Content
- Detected Layer
- Runtime Decision
- Confirmed Asset Names
- Lock Asset State
- Lock Rules
- Continue Generation Rules
- Skip Rules
- Assisted Generation Rules

## Runtime Relationship

`aperospec-injection.skill` is responsible for:

> how Existing Content is connected.

`aperospec-runtime.skill` is responsible for:

> how the Pipeline runs.

Difference:
- Injection decides where content belongs.
- Runtime decides how the Pipeline executes.

## Most Important Principle

The real world always contains:
- half-finished work
- legacy material
- client insistence
- constructed content
- non-modifiable parts

Therefore, an advanced AI Pipeline must support:

> Existing Content Injection.

## Ultimate Definition

`aperospec-injection.skill` is not:

> a generation system.

It is:

> a content fusion system in AI creative industry.
