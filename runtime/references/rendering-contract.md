# Rendering and Technical QA Contract

Read this reference before Stage 5 or when debugging asset generation, crop execution, text composition, overflow, resolution, assembly, or export.

Rendering is a replaceable execution layer. It realizes the locked VDP; it does not become another creative authority or user-visible Runtime.

## 1. Allowed Input

Rendering receives:

- the locked VDP;
- only the source or generated assets explicitly enumerated by that VDP;
- required fonts, templates, or backend resources whose identity and rights are recorded;
- active channel specifications already carried in the VDP.

It must not read upstream artifacts to reinterpret intent. If the VDP is incomplete, return to VisualDirector rather than guessing from CWP, NWP, CDP, raw research, or user references.

## 2. Execution Ownership

Rendering owns:

- generating or acquiring the textless assets called for by the VDP;
- deterministic composition of exact text;
- converting crop intent into exact coordinates;
- sizing, spacing, alignment, font loading, color execution, and export;
- overflow, clipping, contrast, resolution, safe-area, and file-integrity checks;
- producing required variants and technical proof images;
- targeted technical repair inside VDP tolerances.

Rendering does not own:

- title, copy, claims, page order, visual metaphor, Art Direction, typography personality, asset role, or public promise;
- deleting limitations or adding labels to make a layout easier;
- copying external templates, code, images, or branded styles without a recorded rights basis.

## 3. Preflight

Before execution, confirm:

- output format, canvas, aspect ratio, variants, and color mode;
- exact text payload and approved short variants;
- font availability and documented fallback;
- asset identity, rights state, resolution, and intended role;
- protected subjects, allowed crop regions, safe zones, and platform overlays;
- evidence, source, and limitation visibility;
- required thumbnail or distance proofs;
- backend can execute the VDP without a generic fallback layout.

If a required field is missing, stop before production and return to VisualDirector or the first failed owner.

## 4. Asset Realization

- Generate a Hero image only when the VDP assigns a Hero-image task.
- Generated visuals should be textless unless the VDP calls for non-language marks or texture.
- Screenshots, outputs, diagrams, source material, and failure evidence remain primary visual assets when the VDP says they carry proof.
- Preserve character, product, diagram, and evidence consistency across required pages.
- Use only an approved fallback. A generic illustration may not replace evidence or a specific subject relationship.

## 5. Deterministic Text Composition

- Use exact CDP text carried by the VDP.
- Follow semantic line-break intent rather than breaking only by container width.
- Use an approved short variant only in the condition named by the VDP.
- Preserve names, negation, numbers, source lines, and `Do Not Compress` content.
- Do not create decorative English, issue data, category labels, or filler microcopy.

Overflow repair order:

1. apply the approved semantic line break;
2. use the approved short variant when allowed;
3. make a small geometric adjustment inside VDP tolerances;
4. use the approved fallback structure;
5. return to VisualDirector if hierarchy or composition must change;
6. return to ConceptDeck if wording must change.

Never solve overflow by hiding a limitation, shrinking essential text below the viewing condition, or silently rewriting copy.

## 6. Crop and Responsive Execution

- Convert the VDP's protected subject and allowed crop regions into exact crop coordinates.
- Preserve gaze, action, subject relationship, evidence labels, and narrative protection zones.
- Generate each required aspect ratio as an intentional composition, not a blind center crop, when the VDP requires separate variants.
- Record any crop that approaches a forbidden boundary and compare it against the small-size or distance proof.

## 7. Technical QA

Verify each intended page or card for:

- exact pixel dimensions, aspect ratio, file format, and export count;
- font loading and deterministic Chinese text;
- missing glyphs, overflow, clipping, orphaned lines, and accidental truncation;
- crop, safe area, platform overlay, edge collision, and subject integrity;
- contrast and legibility at the declared viewing condition;
- image resolution, screenshot clarity, diagram labels, and evidence visibility;
- required limitation, source, date, version, and attribution visibility;
- no invented text, unexplained decoration, or generic safe-layout substitution;
- cross-page identity, color, typography, and asset consistency;
- openable files and complete output package.

When the output is visual, render and inspect the actual export. Source-file correctness alone is not acceptance.

## 8. Targeted Repair and Stopping Rule

Repair only the failed technical dimension while preserving validated ones. Runtime must set a bounded attempt budget appropriate to cost and risk.

Stop and escalate when:

- the same failure persists after targeted attempts;
- a repair causes a validated dimension to regress;
- the only fallback materially lowers promised quality;
- the renderer cannot realize the locked VDP;
- a proposed fix changes copy, hierarchy, Art Direction, rights, scope, or cost.

Routine technical repairs do not require human intervention. A material quality downgrade, changed visual direction, new rights decision, or final acceptance does.

## 9. Completion Record

Record:

- renderer / backend and version when relevant;
- input assets and rights state;
- outputs, dimensions, formats, and hashes when appropriate;
- font and fallback used;
- crop and overflow decisions;
- technical QA results;
- unresolved limitations;
- whether a human Acceptance Gate remains.

The backend remains replaceable. Runtime may use an unchanged external renderer under its own license, but must not copy third-party templates, code, or assets into the SlideDeck system merely to make it appear self-contained.
