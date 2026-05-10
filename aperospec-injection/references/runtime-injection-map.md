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

## 5. CONTINUE GENERATION RULES

Continue generating:
- [layer / artifact]

Generation must preserve:
- [existing content or constraint]

## 6. SKIP RULES

Skip:
- [layer / skill]

Reason:
[Why this layer already exists or is unnecessary.]

## 7. ASSISTED GENERATION RULES

Assist generation for:
- [layer / skill]

Missing parts to complete:
- [missing part]

Must be based on:
- [existing content]

## 8. RUNTIME HANDOFF

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
| Already rendered slides or deck files | Rendering Layer |

## Validation Checklist

Before finalizing, confirm:
- Existing content was preserved first.
- Detected Layer is explicit.
- Runtime Decision covers every Pipeline skill.
- Lock Mode clearly forbids modification.
- Assisted Generation clearly lists what is missing.
- Continue Generation explains what the next skill should do.
- The final output is RIM, not CWP, NWP, CDP, VDP, or Final Deck.
