---
name: aperospec-project
description: Use Aperospec Project as a standardized upstream Cognitive Engine that accepts only a TOPIC input and outputs a Cognitive World Package (CWP). Use for structured cognitive analysis of a topic, phenomenon, social issue, project theme, product theme, cultural question, future concept, or behavioral change through world evolution, root cause, driving forces, core contradiction, behavioral change, future projection, cognitive triggers, and narrative potential. This skill preserves the original aperospec skill's divergent thinking by providing a separate machine-readable pipeline engine for downstream aperospec-cinema, aperospec-conceptdeck, and aperospec-visualdirector.
---

# Aperospec Project Cognitive Engine

`上游 Skill | 标准化 Cognitive Engine`

## Core Definition

This skill is not the original divergent `aperospec` thinking-description system.

It is a standardized AI pipeline engine based on the Aperospec thinking framework.

Its task is not:
- thinking philosophy
- worldview expression
- narrative generation
- cinematic direction
- slide design
- presentation planning

Its task is:

> automatically infer a world from one topic and output a standardized Cognitive World Package.

## System Position

This skill is the upstream layer in the Aperospec Pipeline.

Pipeline:

`INPUT: TOPIC -> aperospec-project -> Cognitive World Package (CWP) -> aperospec-cinema -> Narrative World Package (NWP) -> aperospec-conceptdeck -> CDP -> aperospec-visualdirector -> VDP -> Final Slide Cinema`

Responsibilities:

| Skill | Position | Responsibility |
| --- | --- | --- |
| aperospec | original divergent framework | preserve open-ended thinking and philosophy |
| aperospec-project | upstream cognitive engine | understand the world and output CWP |
| aperospec-cinema | middle narrative translation engine | translate CWP into a cinematic narrative world |
| aperospec-conceptdeck | concept narrative engine | translate NWP into Concept Deck Package (CDP) |
| aperospec-visualdirector | visual director engine | translate CDP into Visual Directing Package (VDP) |

## Input Protocol

This skill can only receive:

```text
INPUT

TOPIC:
[topic / phenomenon]
```

Examples:

```text
INPUT

TOPIC:
addiction
```

```text
INPUT

TOPIC:
young people are increasingly unable to stop
```

```text
INPUT

TOPIC:
AI companions
```

Forbidden input forms:
- long explanation
- narrative description
- PPT structure
- scene design
- module list
- business framework

If the user provides long source material, first compress it into a single `TOPIC` before running the engine.

If existing locked content is already provided from Injection or Runtime, treat it as upstream constraint, not as permission to drift into narrative or deck logic.

## Output Protocol

Always output:

> Cognitive World Package (CWP)

Do not output:
- narrative world
- film script
- visual direction
- slide deck
- presentation outline
- page structure

The output target is not primarily a human reader.

It is a standardized cognitive input for:

> `aperospec-cinema`

For the reusable output template, read `references/cognitive-world-package.md`.

## Escalation Rule

If the topic is unclear, contradictory, or impossible to normalize into one real `TOPIC`, do not solve the ambiguity by generating a blended world.

Instead:
- state that the topic is unresolved
- ask Runtime or the user for normalization

## Downstream Protection Rule

`aperospec-project` may create narrative potential.

It may not:
- write scenes
- write page sequence
- define emotional rhythm of the deck
- define visual hierarchy

Those belong downstream.

## Cognitive World Package Structure

### 1. WORLD EVOLUTION

Answer:

> How did this phenomenon form?

Must include:
- historical background
- long-term change
- civilizational environment
- technological environment
- social environment

### 2. ROOT CAUSE

Answer:

> What is the real root cause?

Forbidden:
- official explanation
- surface logic

Must search for:
- deep structure
- long-term causality
- emotional root
- civilizational inertia

### 3. DRIVING FORCES

Answer:

> What truly drives the system?

Must include:
- desire
- fear
- emotion
- reward mechanism
- group identity
- environmental induction
- survival pressure

### 4. CORE CONTRADICTION

Answer:

> What is the real structural conflict?

Requirements:
- contains tension
- can be translated into narrative
- contains emotional conflict potential

### 5. BEHAVIORAL CHANGE

Answer:

> How are people being changed?

Must include:
- behavior path change
- emotional change
- social change
- attention change
- identity change

### 6. FUTURE PROJECTION

Answer:

> If the trend continues, what will happen?

Must include:
- civilizational change
- social change
- emotional change
- change in the relationship between people and systems

### 7. COGNITIVE TRIGGERS

Answer:

> What most easily pierces people?

Triggers must be translated from abstraction into perceptible states.

Examples:
- cold phone light late at night
- Restart button
- message seen but not replied to
- empty room
- dormitory breathing sounds

Forbidden:
- pure conceptual expression
- slogans
- general themes

### 8. NARRATIVE POTENTIAL

Answer:

> What type of cinematic world is this topic most suitable to become?

Must include:

#### Narrative Genre

Examples:
- Psychological Sci-Fi
- Slow Collapse
- Urban Isolation
- Future Documentary

#### Narrative Tone

Examples:
- oppressive
- slow falling
- civilizational alienation
- emotional escape

#### Something Is Coming

Define:

> What change is approaching?

## System Rules

### RULE 1

Forbidden:
- PPT structure
- slide description
- page design

### RULE 2

Forbidden:
- typography
- layout
- motion
- visual design

### RULE 3

Forbidden:

> directly entering narrative.

### RULE 4

This system can only generate:

> a cognitive world that can later be narrativized.

## Machine Interface Definition

The output is not a final human-facing article.

It is:

> standardized Cognitive Input for `aperospec-cinema`.

Keep the structure stable. Do not rename output sections unless the user explicitly changes the protocol.

## Final Principle

This system is not:

> helping analyze a problem.

It is:

> automatically inferring a world and generating a cognitive structure that can be narrativized.
