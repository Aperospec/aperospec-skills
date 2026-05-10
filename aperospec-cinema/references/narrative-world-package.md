# Narrative World Package API Template

Use this template only when the input is a complete Cognitive World Package (CWP) from `aperospec-project`.

## Input Gate

Before translation, confirm the CWP contains:
- WORLD EVOLUTION
- ROOT CAUSE
- DRIVING FORCES
- CORE CONTRADICTION
- BEHAVIORAL CHANGE
- FUTURE PROJECTION
- COGNITIVE TRIGGERS
- NARRATIVE POTENTIAL

If these fields are missing, do not improvise. Ask for a valid CWP.

## Mapping Table

| CWP field | NWP translation |
| --- | --- |
| WORLD EVOLUTION | WORLD |
| ROOT CAUSE | hidden pressure inside WORLD and EMOTIONAL ENVIRONMENT |
| DRIVING FORCES | invisible forces inside EMOTIONAL ENVIRONMENT and CORE CONFLICT |
| CORE CONTRADICTION | CORE CONFLICT |
| BEHAVIORAL CHANGE | IMMERSIVE EXPERIENCE and EMOTIONAL CURVE |
| FUTURE PROJECTION | SOMETHING IS COMING |
| COGNITIVE TRIGGERS | SCENE POTENTIALS |
| NARRATIVE POTENTIAL | visual/narrative direction across the NWP |

## Required Output

```markdown
# Narrative World Package (NWP)

## INPUT SOURCE

Cognitive World Package:
[Briefly name the source TOPIC only.]

## 1. WORLD

This is a narrative world where:
[Translate WORLD EVOLUTION into civilizational state, world atmosphere, Opening background, and social state.]

The world is not:
[Avoid surface framing.]

It opens through:
[Opening background, not slide opening.]

## 2. EMOTIONAL ENVIRONMENT

The collective emotion is:
[Translate root cause and driving forces into emotional climate.]

Pressure comes from:
[Hidden Narrative Pressure.]

Loneliness / anxiety / desire / fear appears as:
[Narrative temperature and human condition.]

## 3. SOMETHING IS COMING

What is approaching:
[Translate FUTURE PROJECTION.]

What is losing control:
[System, behavior, desire, society, civilization, or environment.]

What is about to change:
[Approaching transformation.]

## 4. CORE CONFLICT

The narrative core conflict is:
[Translate CORE CONTRADICTION into dramatic tension.]

It is a conflict between:
- People and environment:
- People and systems:
- People and desire:
- People and civilization:

## 5. EMOTIONAL CURVE

The audience moves through:

`immersion -> resonance -> pressure -> lostness -> release -> aftertaste`

Immersion:
[Entry feeling.]

Resonance:
[Where the audience recognizes themselves.]

Pressure:
[Where hidden pressure becomes felt.]

Lostness:
[Where control weakens or meaning collapses.]

Release:
[Where the narrative opens a way out or a pause.]

Aftertaste:
[What remains emotionally.]

## 6. IMMERSIVE EXPERIENCE

The audience feels as if they are entering:
[State / world / condition.]

They move through:
[Behavior path translated from BEHAVIORAL CHANGE.]

They do not merely understand:
[Concept.]

They experience:
[Perceptible condition.]

## 7. VISUAL WORLD

Light and shadow:
[Derived from NARRATIVE POTENTIAL and emotional environment.]

Atmosphere:
[Density, silence, air, pressure, warmth/coldness.]

Spatial feeling:
[Scale, enclosure, distance, threshold, openness.]

Civilizational feeling:
[Historical, technological, ritual, ruin, migration, or future condition.]

## 8. SCENE POTENTIALS

The most cinematic scene potentials are:
- Scene:
  State:
  Behavior:
  Space:
  Emotional trigger:
- Scene:
  State:
  Behavior:
  Space:
  Emotional trigger:
- Scene:
  State:
  Behavior:
  Space:
  Emotional trigger:

These are not slides yet.
They are narrative scene potentials for `aperospec-conceptdeck` to later translate into a Concept Deck Package (CDP).
```

## Validation Checklist

Before finalizing, confirm:
- The input was a CWP.
- The output is an NWP.
- No new root-cause analysis was invented outside the CWP.
- No slide titles, page structures, typography, layout, or motion design appear.
- CWP fields were mapped rather than ignored.
- Scene potentials are cinematic but not yet concept deck beats.
- The NWP can be passed directly to `aperospec-conceptdeck`.

## Forbidden Drift

Do not drift into:
- upstream cognitive analysis
- free worldbuilding unrelated to the CWP
- slide deck outline
- concept deck
- visual design instructions
- business structure
- PPT language

When uncertain, map:
- WORLD EVOLUTION to world
- ROOT CAUSE to pressure
- DRIVING FORCES to invisible forces
- CORE CONTRADICTION to conflict
- BEHAVIORAL CHANGE to human transition
- FUTURE PROJECTION to approaching change
- COGNITIVE TRIGGERS to scene potentials
- NARRATIVE POTENTIAL to tone and pacing
