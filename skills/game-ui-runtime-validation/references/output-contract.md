# Detailed output and acceptance rules

Read the sections for the current production or verification stage before performing that stage. Exact headers, tables, approval and recovery rules below are normative.

## Evidence contract

Maintain a raw manifest binding every screenshot, video, input trace, and log to its hash, build fingerprint, environment, target, fixture, coverage ID, font/asset/runtime health, and timestamp. Summaries without raw values do not satisfy the gate.

Use screen-spec coverage IDs and a risk-based pairwise matrix rather than a full Cartesian product. Cover every target for the baseline state declared by the screen-spec coverage map, plus every primary-action, maximum-stress, and target-sensitive case; cover every other applicable state at least once and add combinations where dimensions interact or defects were found. Never invent or require the literal state name `default` unless it is declared.

## Component runtime evidence contract

Emit one **Component runtime evidence matrix**. Emit this exact plain-text title once, followed by the header on the next line with no blank line between them:

`Component runtime evidence matrix`

Use this exact plain-text header once, with no leading or trailing pipe:

`binding | catalog artifact fingerprint | build fingerprint | consumer | declared adapter | viewport | required state | protected-property evidence | runtime evidence IDs | coverage status`

Build every row by this ten-cell recipe. First index the approved `Component runtime integration matrix` by its exact header names. Copy binding, catalog artifact fingerprint, consumer, declared adapter, and protected-property evidence verbatim from those named source cells; copy the selected viewport verbatim from the screen-spec coverage map; insert the unchanged build fingerprint, one required state, raw runtime evidence IDs, and only `VERIFIED`, `OPEN`, or `BLOCKED`. The declared adapter comes only from the `declared adapter` source cell, never from `implementation target`, component name, or allowed inputs. Runtime observations belong only in `runtime evidence IDs`; never rewrite copied protected-property evidence with `none`, `missing`, or observed values.

Create coverage rows for the baseline state declared by the screen-spec coverage map at every supported target and each other required state at least once at the viewport selected by that map. Never invent or require the literal state name `default` unless it is declared. Never invent a viewport, combine alternatives with `or`, or choose one from prose. Add a non-baseline state at more targets only when the state is target-sensitive, dimensions interact, or a defect requires it; do not expand this into an automatic Cartesian product. If the map does not explicitly identify its baseline state, or an exact copied value or selected viewport is unavailable, stop and mark the input blocked instead of synthesizing a row.

- `VERIFIED` requires actual runtime evidence for the declared adapter, every protected property, and that required state at the same build fingerprint.
- `OPEN` is limited to optional exploratory coverage outside the required risk-based matrix; it never contributes to downstream readiness.
- `BLOCKED` covers a missing capture, missing state, missing protected-property evidence, unavailable raw evidence ID, stale or mismatched build fingerprint, or an observed adapter/identity conflict.

Catalog declarations, implementation tests, static snapshots, and matching dimensions are upstream context, not actual runtime evidence. Never infer a protected property or required state from them.

When the screen-spec coverage map does not explicitly identify its baseline state, emit `Next route: game-ui-screen-spec`. When required evidence is merely not captured and the unchanged runtime is reproducible, emit `Next route: game-ui-runtime-validation`. When actual runtime evidence shows that the approved implementation renders the wrong adapter, protected property, or state, emit `Next route: game-ui-implementation`. When binding identity, declared adapter, contract, or catalog fingerprint conflicts across locked artifacts, emit `Next route: game-ui-component-system`. Keep asset and art defects with their existing owning upstream stages.

Until every required component row is `VERIFIED`, emit this exact line:

`Blocked downstream: game-ui-acceptance-review`

## Output contract

Return a **runtime validation evidence packet** with:

1. build lock, build result, and unchanged confirmation
2. runtime environment and capture configuration
3. full-screen and focused evidence for every supported target
4. state/content/target/input coverage matrix with evidence IDs, including the Component runtime evidence matrix
5. shortest/longest text, numeric/data boundaries, fallbacks, and missing assets
6. center/edge input, disabled behavior, conditional controls, focus, and Back/navigation evidence
7. handoff landmark comparison with expected, observed, delta, and rejection rule
8. full-screen art fidelity by visible family at actual target size
9. logs, errors/warnings, font/asset load, surface size, performance signals, and unwanted scroll/overflow
10. findings with reproduction, expected/actual, severity, owner, and route
11. product-owner runtime checkpoint bound to the exact fingerprint and evidence IDs

Use project severity definitions when supplied; otherwise: P0 app/data failure, P1 primary or required failure, P2 secondary use or fidelity failure, P3 polish.

## Verification and stop conditions

- Inspect original-detail evidence for clipping, overlap, overflow, edge artifacts, distortion, and safe-area collision.
- Compare approved mockup and runtime side by side for material, contour, lighting, perspective, detail density, color harmony, style coherence, and hierarchy.
- For decoded-pixel comparisons, measure the visible color channels explicitly and record the channels and metric. A no-difference bound on a multichannel difference image is not proof of visual identity when an unchanged alpha channel can hide color changes. Evaluate required baseline component properties before expanding state captures; a scoped capture `PASS` cannot clear a failed approved threshold.
- Exercise representative actual content, exact live formatting, all input edges, navigation, and persistence where applicable.
- Invalidate evidence if the build or fingerprint changes.
- Stop as blocked when required runtime, fixture, state, target, font, asset, or fingerprint cannot be reproduced.
- Stop after reporting findings and route defects to their owning stage without editing them.

Technical or geometry success does not prove art fidelity. The independent `game-ui-acceptance-review` owns the final UI verdict.

## Coverage map input binding

Read the approved `Runtime coverage map` by named columns and copy exact selected values. New maps use unique coverage IDs. If the project explicitly approved shared capture-group IDs, index each required observation by group ID, declared component/consumer, and state; one screenshot for the group does not verify all observations. Attach raw evidence IDs to each observation and keep the existing component evidence matrix unchanged.

Return duplicate observation keys, conflicting shared-group targets or fixtures, undeclared states/targets, absent required rows, absent baseline, multiple baseline states per consumer, or missing baseline target coverage to game-ui-screen-spec. Missing executable fixtures are blocked with the declared fixture owner. Do not modify source or substitute data. Repeated component/state rows at different selected viewports represent separate required observations.
