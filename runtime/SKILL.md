---
name: runtime
description: Use Runtime to coordinate a multi-stage SlideDeck pipeline when a request spans two or more of Injection, Project, Cinema, ConceptDeck, VisualDirector, or final rendering, or when the user explicitly asks to run, resume, debug, or rework the full pipeline. It enforces the Aperospec V2 upstream gate, including a completed Stage 1 reality model and user-selected focus before Project, then manages Council and Production modes, locks, artifact handoffs, and conditional channel profiles. Do not use it for ordinary conversation, standalone analysis or research, coding, file management, GitHub work, or a request handled by one skill.
---

# Runtime Orchestrator

`Slide Deck 多 Skill 协作总控`

## Core Definition

`runtime.skill` is the interactive executive PM for one active SlideDeck pipeline built on Aperospec V2. It coordinates only the relevant stages, establishes the upstream reality model, preserves the user's authority over focus and interests, synthesizes professional judgments, manages checkpoints, reallocates feedback, and enters formal production only after the human explicitly approves and freezes the plan.

Runtime remains one system. A target surface such as Xiaohongshu may activate a conditional channel profile, but a profile is not another Runtime or another user-visible workflow.

## Invocation Boundary

- Invoke Runtime only for a multi-stage SlideDeck workflow or an explicit request to run, resume, debug, or rework the full pipeline.
- Let a single relevant Skill handle a single-layer request directly.
- A channel-specific output does not by itself justify Runtime when one Skill can complete the request.
- Do not run Runtime as a global preflight, request classifier, or default analysis layer.
- Do not invoke Runtime for unrelated conversation, standalone analysis or research, coding, file operations, GitHub work, or other ordinary tasks.

## Core Protocols

### 0. Aperospec V2 Upstream Gate

- Before Project produces or freezes a CWP, Runtime must hold a completed Aperospec Stage 1 model containing the active frame and limits, material contradictions, temporal formation, positions and operating force field, baseline future judgment, causally grounded focus set, evidence status, and revision signals.
- The user selects the focus. Runtime, Project, channel conventions, biography, and downstream creative Skills must not select or rank it on the user's behalf.
- If the user already selected a focus in the request, record that choice and continue without asking again.
- Freeze the Stage 1 model and selected focus as the `Aperospec Upstream Lock` before Pipeline Stage 1 (`project`).
- Aperospec Stage 2 strategic play is not automatic. Use it only when the user requests strategic judgment or a strategy-bearing deck. Then confirm the represented subject, interest function, desired direction, resources, dependencies, time horizon, and loss boundaries before strategy enters the pipeline.

### 1. Council Mode
- **Default after invocation**: Start here after Runtime has legitimately been invoked, unless the user explicitly requests a formal production run.
- **Purpose**: Used for brainstorming, cross-skill collaboration, draft generation, and feedback discussion.
- **Constraint**: Does not directly produce the final deliverable (CWP/NWP/CDP/VDP/Final Output).

### 2. Production Mode
- **Trigger**: Starts ONLY after the human explicitly confirms the plan is frozen and ready for production.
- **Purpose**: Used to formally generate the final CWP, NWP, CDP, VDP, and Final Output.

### 3. Cross-Skill Collaboration Protocol
- When user input spans multiple skills, Runtime must not force single-point delegation.
- Runtime must decompose the input and pull relevant Skills to provide judgments from their respective professional perspectives.
- Runtime synthesizes the results and outputs a Team Synthesis Brief.

### 4. Team Synthesis Brief
Runtime must output the following fixed structure during Council Mode:

```markdown
# Team Synthesis Brief

## 1. Current Human Input
Summarize what the human provided in this round.

## 2. Runtime Layer Assessment
Identify which layers and skills are involved.

Active Channel Profile:
[none / named profile and why it is required]

Aperospec V2 Upstream State:
[Stage 1 needed / Stage 1 in progress / awaiting user focus selection / Upstream Lock complete / Stage 2 clarification needed / Stage 2 lock complete]

## 3. Skill Contributions
- Aperospec:
- Injection:
- Project:
- Cinema:
- ConceptDeck:
- VisualDirector:

## 4. Runtime Synthesis
Integrate the skill judgments into one draft proposal.

## 5. Unresolved Questions
List what remains uncertain or deferred.

## 6. Recommended Next Step
Suggest whether to continue discussion, revise, lock, defer, or enter production.

## 7. Human Confirmation Needed
Ask only the key decisions that require human judgment.
```

### 5. Progressive Input Protocol
- The user is not required to provide all materials at once.
- Runtime must support fragmented inputs: documents, reference images, old proposals, style preferences, late-stage ideas, lock commands, etc.
- Missing content enters Deferred Decisions and does not block the workflow.

### 6. Feedback Reallocation Protocol
- When the user provides feedback, Runtime must determine which layer it affects:
  - Fact, evidence, rights, or asset classification issues -> Injection / Runtime evidence gate
  - Active-frame, contradiction, temporal-formation, operating-force, baseline-future, or focus-set issues -> Aperospec Stage 1
  - User focus, represented subject, interests, desired direction, resources, dependencies, or loss boundaries -> preserve as a user-owned Aperospec lock; clarify only what remains unresolved
  - Translation of a valid Aperospec Upstream Lock into the CWP -> Project
  - Narrative issues -> Cinema
  - Editorial copy, title, voice, or page-structure issues -> ConceptDeck
  - Visual style issues -> VisualDirector
  - Overflow, resolution, crop execution, or export issues -> Rendering
  - Material ownership, reference images, asset locking -> Injection
- Runtime must not treat all feedback as a full-pipeline rework.

### 7. Late Input Protocol
- Late-stage new ideas are not process failures.
- Runtime must first assess the impact scope of the new input:
  - Purely visual -> VisualDirector / Rendering
  - Copy or page structure -> ConceptDeck and downstream
  - Narrative direction -> Cinema and downstream
  - Reality model, baseline future, or focus set -> Aperospec Stage 1 and affected downstream stages
  - Cognitive translation of a valid selected focus -> Project and downstream
  - New factual evidence or material-rights information -> Injection / Runtime evidence gate and affected downstream stages

### 8. Draft Lifecycle Protocol
All content must have a state:
- **Pending**: To be discussed
- **Draft**: Draft stage
- **Approved**: Confirmed by human
- **Locked**: Locked and immutable
Only **Locked** content can enter the formal production blueprint. Runtime must not mistake discussion ideas for final commands.

The `Aperospec Upstream Lock` contains the completed Stage 1 model and the user's selected focus. A separate optional `Aperospec Stage 2 Lock` contains only user-confirmed strategic position and interests. Neither lock may be silently rewritten downstream.

### 9. Human Intervention Protocol

- Runtime is autonomous by default for research execution, ordinary creative choices, stage translation, asset production, layout execution, technical repair, and QA inside approved scope.
- Ask the human only when a decision materially changes project intent, public promise, durable visual identity, rights, cost or scope, a locked asset, or an external / irreversible action.
- Always return Aperospec focus selection and any unresolved ranking of competing interests to the human; these are user-authority gates, not ordinary creative choices.
- A decision already answered in the brief or earlier feedback is already resolved; do not ask it again.
- When a gate is needed, recommend one option, show only materially different alternatives, explain the consequence, and state what becomes locked. Do not ask the human to design the solution.
- Final acceptance and any publishing, upload, payment, or other external mutation always retain their normal authorization boundary.
- Detailed gate and continuation rules live in [references/runtime-management-rules.md](references/runtime-management-rules.md).

### 10. Channel Profile Protocol

- A channel profile is a conditional reference loaded inside this Runtime. It is never a second Runtime, a new creative authority, or a reason to expose more Skill choices to the user.
- Profiles may add evidence gates, copy/output requirements, platform constraints, renderer handoff fields, and release checks.
- Profiles must not replace the core artifact chain, override locked content, or let platform conventions decide the project's cognitive, narrative, editorial, or visual direction.
- Load only the profile required by the confirmed output. Do not build or load a broad multi-platform matrix speculatively.
- For Xiaohongshu image posts, read [references/channel-xiaohongshu.md](references/channel-xiaohongshu.md).

## External Research Protocol

Runtime must not assume that user-provided input is always complete.
Runtime may identify missing external context during Council Mode.
Runtime may initiate external research only when it is necessary to clarify reality-based, industry-based, policy-based, market-based, technical, cultural, case-study, or visual-reference context.
External research must be managed by Runtime, not by individual Skills independently.
External research is supporting context by default. It is not user intent, not locked content, and not final creative direction.
If external research changes the project direction, contradicts user input, or introduces a major new interpretation, Runtime must submit it to the human for confirmation before using it as a basis for production.
Runtime must track source, purpose, relevance, and confidence for externally gathered information.
Runtime must not silently inject external information into CWP / NWP / CDP / VDP as if it came from the human.

### When to Consider External Research

Runtime should consider external research when:
1. The human input is too sparse but the project depends on real-world context.
2. The project involves current industry trends, business models, policies, technologies, market examples, cultural context, or public facts.
3. Council Mode reveals unresolved factual assumptions.
4. Aperospec Stage 1 needs stronger evidence for temporal formation, positions and operating forces, the baseline future judgment, or the focus set.
5. ConceptDeck needs case references, comparable projects, or structural precedents.
6. VisualDirector needs style, layout, exhibition, spatial, poster, or visual-system references.
7. The human explicitly asks Runtime to search, verify, compare, or collect external information.

### When NOT to Initiate External Research

Runtime must not initiate external research when:
1. The task is purely based on user-provided materials.
2. The human explicitly says not to search.
3. The missing information is a creative preference that should be decided by the human.
4. The project is already in Production Mode and the missing information would alter locked direction, unless Runtime first returns to Council Mode and asks for human approval.
5. Research would introduce unnecessary noise or drift from the user's intent.

### Research Request

When Runtime determines that external research is needed, it must not directly search and mix the results. Instead, it must first form a Research Request:

```markdown
# Research Request

## 1. Why Research Is Needed
Explain what is missing or uncertain.

## 2. Research Questions
List the specific questions to answer.

## 3. Intended Use
Explain whether the research will support Aperospec Stage 1, Project, Cinema, ConceptDeck, VisualDirector, or Injection.

## 4. Risk of Not Researching
Explain what may go wrong if the pipeline continues without this context.

## 5. Human Approval Needed
Ask whether to proceed with external research if the research may affect direction, cost, scope, or factual claims.
```

Rules:
* If the user explicitly requested the search, Runtime may execute the Research Request directly.
* If the search may change project direction, affect positioning, introduce sensitive facts, or expand scope, Runtime must ask for human confirmation first.
* A Research Request is not a final artifact, but Runtime's external data collection plan.

### Research Synthesis Brief

After external research is complete, Runtime must output a Research Synthesis Brief:

```markdown
# Research Synthesis Brief

## 1. Research Scope
What was searched and why.

## 2. Key Findings
Summarize only relevant findings.

## 3. Source Notes
Record source type, recency, reliability, and limitations.

## 4. Pipeline Relevance
Explain which findings are relevant to:
- Aperospec Stage 1
- Project
- Cinema
- ConceptDeck
- VisualDirector
- Injection

## 5. Conflicts With Human Input
Identify any conflict with existing user direction or locked content.

## 6. Runtime Recommendation
Explain whether the research should be:
- used as background context
- incorporated into the draft
- sent to a specific Skill
- ignored
- submitted to human for decision

## 7. Human Confirmation Needed
Ask only the decisions that require human judgment.
```

### External Research Allocation Logic

1. Industry facts / policy / market / social background
   → mainly supports Aperospec Stage 1; after the user selects a focus, the locked result supports `project`.
2. Cultural context / emotional atmosphere / narrative references
   → mainly supports `cinema`.
3. Comparable cases / presentation structure / exhibition precedents / deck logic
   → mainly supports `conceptdeck`.
4. Visual references / style references / spatial references / poster references / layout references
   → mainly supports `visualdirector`.
5. User-provided URLs, documents, reference images, old proposals, or locked assets
   → should first be handled by `injection`.

### External Material State Rules

External research findings must be labeled as one of the following:

1. `Background Context`: Can inform understanding but cannot directly become locked content.
2. `Supporting Evidence`: Can support Project / Cinema / ConceptDeck reasoning, but must retain source awareness.
3. `Reference Material`: Can guide VisualDirector or ConceptDeck, but must not be copied or treated as user-owned material.
4. `Potential Direction Change`: Must be submitted to the human before being used.
5. `Rejected / Not Relevant`: Must not enter downstream artifacts.

## Final Output Format Decision Protocol

Runtime must not assume the final delivery format.

The final output format is a human-owned decision. It may include, but is not limited to, HTML slide deck, PPTX, PDF, Markdown document, image sequence, web page, or any custom format requested by the human.

If the human has not specified the final output format, Runtime must record it as a Deferred Decision.

Runtime may continue Council Mode without a confirmed final output format.

Runtime must not enter Production Mode until the human confirms the final output format.

Runtime should ask for this decision during Production Readiness review if it has not already been confirmed.

Once confirmed, the final output format must be recorded in the Production Blueprint.

Runtime must not silently default to HTML, PPTX, PDF, or any other format.

## Original Pipeline & Artifact System (Retained for Production Mode)

The original stage system (Stage 0 to Stage 5) and artifact freezing rules are strictly retained but are now executed inside **Production Mode**.

### Upstream Gate: Aperospec Stage 1 -> user focus selection -> Aperospec Upstream Lock
### Optional Strategic Gate: user-confirmed Aperospec Stage 2 Lock
### Pipeline Stage 1: Cognitive Engine (`project.skill`) -> CWP
### Pipeline Stage 2: Narrative Universe (`cinema.skill`) -> NWP
### Pipeline Stage 3: Concept Deck (`conceptdeck.skill`) -> CDP
### Pipeline Stage 4: Visual Director (`visualdirector.skill`) -> VDP
### Pipeline Stage 5: Rendering Agent -> Final Output

Runtime is responsible for ensuring context isolation during Production Mode and protecting Locked Assets.

## Supporting References

- Read [references/runtime-protocol.md](references/runtime-protocol.md) when entering or debugging formal Production Mode.
- Read [references/runtime-management-rules.md](references/runtime-management-rules.md) for checkpoints, locks, rework, and acceptance.
- Read [references/rendering-contract.md](references/rendering-contract.md) before Stage 5 rendering or when debugging crop, overflow, resolution, assembly, or export.
- Read a channel profile only when the final output requires it; currently supported: [references/channel-xiaohongshu.md](references/channel-xiaohongshu.md).
