# Xiaohongshu Channel Profile

Load this profile only when Runtime is already active and the confirmed final output includes a Xiaohongshu image post. This is a conditional Runtime reference, not an outer Runtime, another Skill, or a replacement for Project, Cinema, ConceptDeck, VisualDirector, or Rendering.

## Purpose

Adapt the existing SlideDeck pipeline to a phone-first, self-explanatory image sequence with companion post copy and a release-readiness check.

The profile adds:

- public-source and claim verification when the topic comes from social/news/product sources;
- originality and material-rights boundaries;
- phone-first editorial copy requirements;
- 3:4 visual and thumbnail constraints;
- a pre-publication gate.

It does not add automatic publishing, account interaction, or another orchestration layer.

## Route Selection

Use the shortest valid route.

- Straightforward feature update, tutorial, or evidence-led explanation: Injection / Evidence Lock → Project → restrained Cinema translation → ConceptDeck → VisualDirector → Rendering. Cinema should preserve clarity and must not inflate a simple fact into artificial drama.
- Complex cultural, strategic, behavioral, emotional, or future-facing topic: Injection / Evidence Lock → Project → Cinema → ConceptDeck → VisualDirector → Rendering.
- Skip Cinema only when the active ConceptDeck contract explicitly accepts the available upstream artifact. Do not create an invalid handoff merely to shorten the route.
- Do not skip ConceptDeck when the output has multiple cards or requires final audience-facing copy.

Skipping is a Runtime decision recorded through the existing Injection / stage-routing rules. It does not create a separate “quick Runtime.”

## Evidence Lock

When a post begins with an X post, news item, product page, paper, repository, or another public source, freeze an Evidence Lock before creative production.

It contains:

- the exact approved claims and their status: verified, partially verified, unverified, or outdated;
- direct primary-source links and observation dates;
- version, region, price, capability, or license limitations when relevant;
- exact names that must not be rewritten;
- material classification: content, style reference only, user-owned asset, licensed asset, or unusable;
- required uncertainty and commercial-relationship disclosures.

Social engagement is a discovery signal, not proof. Do not pass the original post’s wording, image, sequence, or distinctive framing downstream as reusable creative material.

## Editorial Output

ConceptDeck owns both sequence and final audience-facing copy.

For the package, it must provide:

- one platform title;
- one cover line and at most one supporting deck line;
- page-ready title, narrative sentence, supporting copy, caption/source line, and any non-compressible limitation for every card;
- a companion post draft when requested;
- a Voice Contract and a clear title-to-content payoff.

Prefer concrete people, objects, actions, consequences, and lived states over technical taxonomy. A strong hook may invite imagination, but it cannot promise more than the Evidence Lock supports.

## Visual Output

Default static-card target:

- 1080 × 1440 pixels, 3:4;
- one primary task and one focal point per card;
- cover understandable at approximately 360 pixels wide;
- exact Chinese type composed deterministically after any generated, textless visual is approved;
- screenshots, outputs, diagrams, or test evidence treated as primary visual material when they carry the proof.

For a new, subjective, or account-defining cover direction, VisualDirector should first prepare up to three materially different proofs at approximately 360 pixels wide, recommend one, and let Runtime open a Visual Direction Gate. Do not involve the human for superficial alignment or color variants. Once the image-type relationship is approved, lock it before high-resolution rendering.

Do not imitate a paper magazine with fake barcodes, prices, issue numbers, filler labels, or decorative metadata. Do not force all pages into one repeated template.

Platform specifications can change. Recheck any unstable publishing limit or interface requirement at delivery time rather than treating this profile as permanent platform documentation.

## Renderer Handoff

Rendering receives the locked VDP, which carries the final copy and approved assets. The backend may use image generation, deterministic HTML/CSS composition, supplied screenshots, diagrams, or an unchanged external renderer as appropriate.

Apply [rendering-contract.md](rendering-contract.md) in addition to this channel profile.

The renderer may fix overflow, crop execution, resolution, and export defects. It may not rewrite the title, invent labels, change the visual direction, or hide an important limitation to make the layout easier.

The backend is replaceable. Do not copy third-party templates, code, or assets into Runtime merely to make the workflow appear self-contained.

## Runtime Locks

The same Runtime manages four channel-specific checkpoints:

| Lock | What becomes stable | Restart when |
| --- | --- | --- |
| Evidence Lock | approved claims, sources, limitations, rights | new evidence, stale source, changed capability, or rights conflict |
| Editorial Lock | angle, voice, title, page-ready copy | facts change, user changes positioning, or copy cannot be fulfilled |
| Visual Lock | page sequence, visual system, asset role, composition intent | copy changes, asset becomes unavailable, or rendering proves the direction infeasible |
| Release Lock | final images, post copy, attribution, risk status | any upstream artifact or platform condition changes |

These are states inside Runtime. They do not constitute another lifecycle or another Runtime.

Human intervention is required only when the relevant lock contains a material choice not already answered:

- Evidence / Editorial: public claim, title promise, positioning, or limitation changes what is said on the human's behalf;
- Visual: different proofs materially change emotional stance or durable account identity;
- Release: the final package is ready for acceptance before any publication.

Routine page design, object selection, camera, layout, deterministic text composition, crop execution, overflow repair, and export remain autonomous inside the approved locks.

## Review Cadence

When the user asks to observe every stage, stop after each completed lock and report:

1. what was decided;
2. what artifact changed;
3. what remains open;
4. the single next stage.

Do not proceed into the next lock until the user says to continue. Otherwise follow the normal Runtime checkpoint rules.

## Release Gate

Before declaring the package ready for publication, confirm:

- every important claim maps to the Evidence Lock;
- the cover promise is fulfilled by the cards and post copy;
- facts, source opinion, our inference, and imagined future are distinguishable;
- required limitations are visible rather than hidden in tiny text;
- every used visual has a recorded rights basis;
- names, versions, dates, and source lines are correct;
- output dimensions, crop, contrast, overflow, and 360-pixel legibility pass;
- no external post, image, layout, or distinctive expression was lightly rewritten or redrawn;
- the user has reviewed the package.

Runtime stops at release readiness. Publishing, logging in, uploading, commenting, liking, following, or other account interaction requires separate, current user authorization.

## Rework Routing

- Wrong claim, source, date, limitation, or rights state → Evidence Lock / Injection.
- Weak focus or no human relevance → Project.
- Broken emotional progression → Cinema, if Cinema was active.
- Weak title, voice, payoff, page order, or repeated copy → ConceptDeck.
- Wrong composition, visual metaphor, typography personality, or image–type relationship → VisualDirector.
- Overflow, crop execution, low resolution, export, or thumbnail rendering defect → Rendering.

Restart from the first failed owner and preserve every validated upstream artifact.
