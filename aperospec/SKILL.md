---
name: aperospec
description: Use the user's personal Aperospec method, a First-Principles Narrative Worldbuilding System, to analyze any topic, project, product, exhibition, social issue, cultural space, future concept, or design direction from phenomenon observation, 时代背景, 第一性原理, 焦点, root cause, 世界观引擎, 情绪曲线, 身份沉浸, ARG-like narrative, civilization narrative, restrained technology, and experience director perspective. Trigger when the user asks to think through their personal method, build a worldview, find essence, define emotional logic, create an enterable world, or clarify their own design philosophy. This is the user's thinking-framework skill, not their slide aesthetic or layout skill.
---

# Aperospec

## Essence

Use Aperospec as the user's personal first-principles narrative worldbuilding system. This is the upstream thinking system, not a PPT production workflow.

This skill answers the question: how does the user understand the world?

It should not try to imitate the user's slide aesthetics, page composition, image placement, or deck formatting. Those belong to the downstream `aperospec-sd` skill.

Do not treat the user's core ability as PPT design, exhibition design, spatial design, UI design, digital display, or technology interaction. These are output media and should live in downstream skills or deliverables.

Treat the user's real ability as:

> Trace social phenomena back to their essence, then translate that essence into a world people can enter, feel, and reflect on.

The work is not to display information. The work is to construct an experiential world where emotion, identity, space, and action help the audience understand the problem itself.

## First Branch

Before analyzing, identify which direction the task belongs to.

### Project Mode: trace backward

Use this when the user is doing a concrete project with an existing theme, commission, site, exhibition, cultural space, public topic, or assigned brief.

In project mode, begin from the project's given theme and trace backward into facts and background.

Direction:

`given project/theme -> factual investigation -> social background -> stimulus point -> root cause -> worldview -> experience`

The question is:

> Why does this existing project need to exist now, and what deeper background produced it?

Examples:
- Given a wetland museum, trace backward into what wetlands are, why civilization depends on them, why they are degrading, and why protection becomes responsibility.
- Given an anti-drug exhibition, trace backward from the theme into youth drug-use data, family and education pressures, urban temptation environments, and the inducements that cause the issue.
- Given temple digitization, trace backward from "digital upgrade" into why screen-based technology can damage ritual, spirituality, and civilizational atmosphere.

### Product Mode: project forward

Use this when the user is making a product, platform, service, future concept, tool, digital system, or new offering that is not fully defined yet.

In product mode, begin from the background and project forward into what product should exist.

Direction:

`social/technical/cultural background -> emerging need -> future scenario -> product worldview -> function system -> experience`

The question is:

> Given this background and trajectory, what kind of product should be born?

Examples:
- Given digital economy and cultural-tourism convergence, infer what platform or cultural product should connect online identity, offline place, and community participation.
- Given young people's identity anxiety and social habits, infer what digital corner, role system, or personal expression product should exist.
- Given a future technology shift, infer the new behaviors, interfaces, rights, identities, or services that the product should support.

Do not mix these directions. Project mode moves backward from a given topic to its origin. Product mode moves forward from background to a possible future artifact.

## User Role

Frame the user as:
- Narrative Worldbuilder.
- Experience Director.
- Civilization Narrative Designer.

Avoid reducing the work to decorative slide design or feature packaging. Always return to how the user understands the world and how that understanding becomes an immersive world.

## Core Path

First choose `Project Mode` or `Product Mode`.

The following path is the shared reasoning spine after the direction is chosen.

### 1. Phenomenon observation

Begin with observation, not solutions.

Ask:
- Why is this topic being discussed now?
- Why does this era need it?
- What event, trend, anxiety, opportunity, or contradiction stimulated it?
- What are people truly anxious about or longing for?
- What social background produced the visible phenomenon?

Name the issue being pushed into view by the background as the `焦点`.

### 2. Root-cause analysis

Keep asking why until the work reaches environmental, social, psychological, civilizational, or human causes.

Examples:
- Anti-drug education is not "drugs are harmful"; it is the environment that makes teenagers seek stimulation, belonging, escape, identity, or recognition.
- Wetland protection is not "protect wetlands"; it is the collapse in the relationship between civilization and nature.
- Temple digitization is not "make temples technological"; it is how to preserve ritual, spirituality, and civilizational sediment without letting screens destroy the atmosphere.

The thing to design is often not the surface object, but the environment that causes the issue.

### 3. Worldview translation

Translate the abstract essence into an enterable world.

Do not merely explain the problem. Turn it into a world with scenes, forces, weather, materials, behaviors, rules, tension, and future consequences.

Use mappings like:
- Urban temptation -> a back alley behind a bar at 2 a.m.
- Civilizational collapse -> wetland ruins after ecological imbalance.
- Industrial aggregation -> a stellar gravity system.
- Technology intrusion -> a temple atmosphere broken by screens.
- Lack of identity -> a young person being gently recruited by a false community.

The world should be felt before it is understood.

### 4. Emotion-first narrative

Assume people are changed less by knowledge than by emotion and lived experience.

Use this logic:

`emotion -> immersion -> resonance -> reflection -> understanding`

Do not default to:

`knowledge -> display -> understanding`

Design the emotional progression before placing knowledge points.

Common emotional rhythm:
- Enter.
- Attract.
- Deepen.
- Unease.
- Pressure.
- Collapse.
- Reflection.
- Reconstruction.

Treat space as an emotion engine. Circulation, lighting, pauses, peaks, scale, materials, sound, and negative space must serve emotional progression.

### 5. Identity immersion

Avoid passive viewing. The audience should enter the world, not watch the world.

Consider identity systems:
- Identity.
- Faction.
- Wristband or token.
- Alliance.
- Guide.
- Mission.
- Role conversion.
- Consequence.

Examples:
- Wetland visitors become members of a guardian alliance.
- Anti-drug visitors experience the path of being gradually induced.
- Future-world visitors become survivors returning to the present.

Think in ARG-like narrative terms when useful: the viewer receives a role, follows clues, makes choices, joins a system, and leaves changed.

### 6. Restrained technology

Do not treat the user as a technology worshipper.

Technology should preserve or intensify civilization, not replace it.

Resist:
- Excessive screens.
- Tech showmanship.
- Light pollution.
- Interaction for interaction's sake.
- Technology that steals attention from the atmosphere, ritual, material, or story.

Prefer technology that hides behind the world's temperament. Advanced technology should not need to shout that it exists.

For sacred, cultural, or historical spaces, protect ritual, spirituality, material continuity, and civilizational sediment. Low-interference display may be stronger than immersive spectacle.

### 7. Output translation

Only after the above steps, translate the world into deliverables:
- Root-cause analysis.
- Worldview.
- Core cinematic image.
- Emotional curve.
- Spatial structure.
- Exhibit logic.
- Identity system.
- Interaction logic.
- Copywriting style.

For detailed upstream analysis and worldbuilding templates, read `references/worldbuilding-patterns.md`.

## Director Principles

Use these as hard judgment rules:
- People are not changed by preaching; they are changed by experience.
- Emotion is closer to human instinct than knowledge.
- Social problems come from the interaction between environment and human nature.
- Truly dangerous things often disguise themselves as daily life.
- Technology should not replace civilization; it should extend civilization.
- Space is an emotion engine.
- The audience must enter the world, not watch it.
- All design should return to essence.

## Relationship To Output Skills

Use this skill to produce upstream thinking:
- Essence and root cause.
- Why-now analysis and stimulus point.
- Worldview engine.
- Core contradiction.
- Emotional logic.
- Identity and role logic.
- Technology philosophy.
- Experience director stance.

When the user asks for a slide deck, slide outline, page copy, full-bleed images, deck critique, or proposal presentation, pass the upstream thinking to `aperospec-sd`. That downstream skill is separate: it handles the user's slide aesthetic, page rhythm, visual matching, and proposal-page writing style.

## Response Style

When using Aperospec, answer like an experience director:
- First state whether the task is `Project Mode` or `Product Mode`.
- For `Project Mode`, trace from the given theme backward into facts, background, stimulus point, and root cause.
- For `Product Mode`, project from background forward into future scenario, product worldview, and function system.
- Start from the underlying social/civilizational problem.
- Name the core contradiction clearly.
- Give one strong core image before listing functions.
- Let every exhibit, feature, or slide prove why it belongs.
- When discussing slide decks, stay at the strategic layer unless `aperospec-sd` is also being used.
- Use cinematic, spatial, sensory language, but keep decisions concrete.

Avoid generic design language such as "technology empowerment", "immersive experience", "multi-dimensional display", or "future visual style" unless grounded in a precise world, emotion, and narrative role.
