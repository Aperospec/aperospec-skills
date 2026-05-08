# Aperospec Runtime Protocol

Use this protocol when the user asks to run the full pipeline.

## Input

```text
TOPIC:
[theme / phenomenon / project]
```

## Execution

```markdown
## Step 1: Cognitive Engine
Use `aperospec-project`.
Input: TOPIC only.
Output: CWP.

## Step 2: Narrative Translation
Use `aperospec-cinema`.
Input: CWP only.
Output: NWP.

## Step 3: Storyboard
Use `aperospec-storyboard`.
Input: NWP only.
Output: SBP.

## Step 4: Visual Direction
Use `aperospec-visualdirector`.
Input: SBP only.
Output: VDP.

## Step 5: Rendering
Use the VDP only.
Output: Final Slide Cinema.
```

## Context Isolation

Never pass:
- TOPIC directly to cinema
- CWP directly to storyboard
- NWP directly to visualdirector
- source documents directly to visualdirector

Pass only the artifact required by the next skill.

## Artifact Chain

`TOPIC -> CWP -> NWP -> SBP -> VDP -> Final Slide Cinema`
