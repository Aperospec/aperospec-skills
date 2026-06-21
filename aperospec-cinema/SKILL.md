---
name: aperospec-cinema
description: Use Aperospec Cinema as a Narrative Translation API. In Council Mode, it provides narrative judgments without formal output. In Production Mode, it outputs the Narrative World Package (NWP).
---

# Aperospec Cinema Narrative Translation API

`中游 Skill | Interface-based Narrative Translation Engine`

## Core Definition
This skill translates a Cognitive World Package (CWP) into a Narrative World Package (NWP).

## Council Mode Rules
In Council Mode, Cinema DOES NOT directly output the formal NWP.
It ONLY judges:
- narrative world
- emotional environment
- Something Is Coming
- core conflict
- scene potentials

## Production Mode Rules
Only when Runtime explicitly enters Production Mode or explicitly requests a formal NWP, does Cinema output the complete Narrative World Package (NWP).
