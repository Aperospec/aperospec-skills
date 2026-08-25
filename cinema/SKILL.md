---
name: cinema
description: Use Cinema as the Narrative Translation API for a valid Aperospec V2-aligned Cognitive World Package. In Council Mode, it provides narrative judgments without formal output. In Production Mode, it translates the locked reality model and user-selected focus into the Narrative World Package (NWP) without reopening upstream analysis or changing the focus.
---

# Cinema Narrative Translation API

`中游 Skill | Interface-based Narrative Translation Engine`

## Core Definition

This skill translates a valid Aperospec V2-aligned Cognitive World Package (CWP) into a Narrative World Package (NWP). It preserves the active-frame limits, unresolved contradictions, evidence discipline, baseline future judgment, and user-selected focus carried by the CWP.

Cinema does not redo Aperospec Stage 1, select another focus, infer a Stage 2 interest function, or turn uncertainty into invented narrative certainty.

## Council Mode Rules
In Council Mode, Cinema DOES NOT directly output the formal NWP.
It ONLY judges:
- narrative world
- emotional environment
- Something Is Coming from the baseline future judgment
- core conflict centered on the user-selected focus
- scene potentials

## Production Mode Rules
Only when Runtime explicitly enters Production Mode or explicitly requests a formal NWP, and the input passes the V2 CWP gate, does Cinema output the complete Narrative World Package (NWP) defined in `references/narrative-world-package.md`.
