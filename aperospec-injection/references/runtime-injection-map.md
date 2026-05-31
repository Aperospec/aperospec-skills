# Runtime Injection Map Template

Use this template when `aperospec-injection` receives existing user content.

## Required Output

```markdown
# Runtime Injection Map (RIM)

## 1. EXISTING CONTENT

Content name:
[Name the existing content.]

Content summary:
[Briefly summarize what exists.]

Non-modifiable parts:
[List anything that must not be changed.]

## 2. DETECTED LAYER

Detected Pipeline Layer:
[Cognitive Layer / Narrative Layer / Concept Deck Layer / Visual Direction Layer / Rendering Layer]

Reason:
[Why this content belongs to that layer.]

Corresponding Skill:
[aperospec-project / aperospec-cinema / aperospec-conceptdeck / aperospec-visualdirector / Rendering Agent]

## 2A. STYLE DNA MAP

Include this section only when the user provides reference images.

Reference classification:
[Content Reference / Style Reference Only / Brand / Asset Lock]

If Style Reference Only:

Extracted Style DNA:
- Brushwork:
- Line quality:
- Surface texture:
- Material feeling:
- Color system:
- Lighting atmosphere:
- Edge treatment:
- Rendering method:
- Grain / print / noise feeling:
- Composition temperament:
- Typography compatibility:

Forbidden transfer:
- depicted subject
- object
- character
- building
- product
- logo
- symbol
- exact layout
- exact pose
- exact scene
- narrative event

Pipeline boundary:
[Confirm Style DNA must not enter Cognitive, Narrative, or Concept Deck layers and may only be passed to VisualDirector after CDP is frozen.]

## 3. RUNTIME DECISION

| Pipeline Skill | Mode | Reason |
| --- | --- | --- |
| aperospec-project | [Full Generation / Assisted Generation / Injection / Lock / Skip / Continue Generation] | [reason] |
| aperospec-cinema | [Full Generation / Assisted Generation / Injection / Lock / Skip / Continue Generation] | [reason] |
| aperospec-conceptdeck | [Full Generation / Assisted Generation / Injection / Lock / Skip / Continue Generation] | [reason] |
| aperospec-visualdirector | [Full Generation / Assisted Generation / Injection / Lock / Skip / Continue Generation] | [reason] |
| aperospec-runtime | Continue Pipeline | [how runtime should execute] |

## 4. LOCK RULES

Locked content:
- [content]

Forbidden operations:
- modify
- rewrite
- delete
- reconstruct Narrative
- rewrite Scenes
- change Emotional Logic

## 5. CONFIRMED ASSET NAMES

Confirmed Asset Names:
- [formal asset name]

Asset type:
- [exhibit item / chapter / spatial name / function module / constructed content / client-locked content]

Name source:
- [user-provided / existing document / client-locked / constructed site]

Lock Asset State:
- [Locked / Not Locked]

Downstream forbidden operations:
- rename
- replace with summary wording
- "upgrade" the name
- narratively rename
- replace with synonyms
- stylize the name
- AI-optimize the name

Downstream allowed operations:
- reference
- arrange in layout
- connect through Narrative
- organize rhythm
- structure pages

## 6. CONTINUE GENERATION RULES

Continue generating:
- [layer / artifact]

Generation must preserve:
- [existing content or constraint]

## 7. SKIP RULES

Skip:
- [layer / skill]

Reason:
[Why this layer already exists or is unnecessary.]

## 8. ASSISTED GENERATION RULES

Assist generation for:
- [layer / skill]

Missing parts to complete:
- [missing part]

Must be based on:
- [existing content]

## 9. RUNTIME HANDOFF

Pass this RIM to:

> `aperospec-runtime.skill`

Runtime should:
[Explain how to start or continue the pipeline.]
```

## Layer Detection Cheatsheet

| Existing content | Likely layer |
| --- | --- |
| Root-cause analysis, drive forces, world understanding | Cognitive Layer |
| Worldview, emotional environment, narrative universe, emotional curve | Narrative Layer |
| Exhibit items, concept sequence, cognitive triggers, atmosphere directions | Concept Deck Layer |
| Brand assets, visual guidelines, typography, color, lighting | Visual Direction Layer |
| Style Reference Only images, brushwork, texture, material feeling, color system, lighting, rendering method | Visual Direction Layer as Style DNA Map |
| Already rendered slides or deck files | Rendering Layer |

## Validation Checklist

Before finalizing, confirm:
- Existing content was preserved first.
- Detected Layer is explicit.
- Runtime Decision covers every Pipeline skill.
- Lock Mode clearly forbids modification.
- Confirmed Asset Names are listed when the user provides existing names.
- Style Reference Only images are converted into Style DNA Map rather than treated as reusable content.
- Style DNA Map is blocked from Cognitive, Narrative, and Concept Deck layers.
- Lock Asset State forbids downstream renaming unless the user explicitly requests renaming.
- Assisted Generation clearly lists what is missing.
- Continue Generation explains what the next skill should do.
- The final output is RIM, not CWP, NWP, CDP, VDP, or Final Deck.
