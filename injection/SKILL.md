---
name: injection
description: Use Injection as the content injection and structure fusion engine. It analyzes existing user content, detects pipeline layers, identifies whether material reopens an Aperospec V2 Stage 1 model, records only explicit user changes to focus or Stage 2 interests, and confirms formal names and locks. In Council Mode, it provides material attribution and lock advice without creative generation.
---

# Injection

`内容注入与结构融合引擎`

## Core Definition

`injection.skill` is not a creative skill. Its core responsibility is analyzing existing user content and connecting it to Aperospec V2 and the downstream Slide Deck artifact chain.

For each material, distinguish whether it:

- updates or contradicts the Stage 1 reality model, baseline future judgment, or focus set
- explicitly records the user's focus selection
- explicitly updates a user-confirmed Stage 2 subject, interest, desired direction, resource, dependency, or loss boundary
- belongs only to a downstream cognitive, narrative, concept, visual, or rendering layer

Do not infer focus selection or interest confirmation from the material's prominence, emotional intensity, source, or placement. Only the user's explicit choice can change those locks.

**Update**: Injection is not just a pre-processor. It can be called at any stage by Runtime. It is used to judge whether new material is content asset, style reference, locked asset, old proposal, feedback material, or invalid material.

## Council Mode Rules
In Council Mode, Injection ONLY outputs:
- Material attribution (which layer the material belongs to)
- Aperospec V2 impact attribution and evidence status
- Lock advice (what must be locked)
- Style reference boundaries
It DOES NOT generate creative content.

## Original Pipeline Execution (Production Mode)
- Identifies the pipeline layer for existing content.
- Generates Runtime Injection Map (RIM).
- Marks whether the material reopens Aperospec Stage 1 or changes an explicit user-owned lock.
- Protects Locked Assets.
- Classifies references into Content Reference, Style Reference Only, or Brand/Asset Lock.
