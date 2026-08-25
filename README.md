# SlideDeck

SlideDeck is a six-Skill editorial and visual production system for Codex. It turns a user-selected focus into a structured cognitive model, narrative world, concept sequence, final audience-facing copy, visual direction, and a render-ready handoff.

It is designed as one coordinated system, not a collection of unrelated generators.

## Architecture

```text
Aperospec V2 Stage 1
  -> user-selected focus
  -> Project (CWP)
  -> Cinema (NWP)
  -> ConceptDeck (CDP + final editorial copy)
  -> VisualDirector (VDP)
  -> replaceable rendering backend
```

Runtime coordinates the pipeline. Injection classifies new material, preserves locks, and routes changes to the first affected layer.

The six included Skills are:

- `injection` — material attribution, evidence status, reference boundaries, and lock routing;
- `project` — Aperospec V2 reality model and selected focus to Cognitive World Package;
- `cinema` — Cognitive World Package to Narrative World Package;
- `conceptdeck` — page sequence, editorial voice, titles, and final audience-facing copy;
- `visualdirector` — original art direction, editorial hierarchy, cover logic, visual system, and render-ready VDP;
- `runtime` — Council/Production coordination, human decision gates, artifact locks, rendering QA, and conditional channel profiles.

## Upstream dependency

SlideDeck expects [Aperospec V2](https://github.com/Aperospec/Aperospec) upstream. Aperospec is intentionally maintained as a separate Skill and repository; it is not duplicated here.

The repository also does not bundle image-generation models, third-party renderers, social-card templates, user assets, case materials, or platform credentials. Rendering remains a replaceable downstream implementation.

## Operating model

- Council Mode is for cross-Skill judgment, synthesis, and unresolved decisions.
- Production Mode begins after the user approves the plan and freezes the required upstream locks.
- The system is autonomous for ordinary in-scope creative and technical choices.
- The user retains decisions that change intent, selected focus, public promise, durable visual identity, rights, cost, scope, or external publication.
- Feedback reopens only the first failed layer and its downstream artifacts; it does not restart the entire pipeline by default.

The optional Xiaohongshu profile is a channel constraint inside the same Runtime. It is not a second Runtime and does not override the core editorial or visual system.

## Installation

Copy the six Skill directories into your Codex personal skills directory and keep automatic Skill discovery enabled. Install Aperospec V2 separately when the workflow needs the full upstream reasoning gate.

Each Skill contains its own `SKILL.md`, UI metadata, and only the references needed for progressive disclosure.

## Repository status

This repository currently does not include an open-source license. Do not infer permission to copy, modify, or redistribute it beyond rights granted by applicable law or a separate agreement.
