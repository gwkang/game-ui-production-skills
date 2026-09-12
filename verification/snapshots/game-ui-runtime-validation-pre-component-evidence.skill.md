---
name: game-ui-runtime-validation
description: Use when an implemented game UI needs actual-runtime evidence for rendering, content, states, input, and fidelity before acceptance review.
---

# Game UI Runtime Validation

## Overview

Validate an unchanged build in its actual runtime. Static tests do not prove rendered fidelity, loaded assets, content boundaries, or usable input geometry.

## Required inputs

- Approved screen specification, mockup, handoff comparison map, asset verdict, and implementation evidence.
- Exact build fingerprint, launch/capture method, fixture data, expected states, targets, locales, and safe areas.
- Approved composite hashes and source-parity records.

Use the project's declared browser, engine, emulator, simulator, device, or capture harness. For each run record environment, scale, target dimensions, safe area, fixture, state, locale, timestamp, and fingerprint; recheck the fingerprint after capture.

Validation is repository-read-only. Interact only through normal runtime controls and isolated fixture state. Do not fix code, assets, data, or evidence, and never self-approve.

## Evidence contract

Maintain a raw manifest binding every screenshot, video, input trace, and log to its hash, build fingerprint, environment, target, fixture, coverage ID, font/asset/runtime health, and timestamp. Summaries without raw values do not satisfy the gate.

Use screen-spec coverage IDs and a risk-based pairwise matrix rather than a full Cartesian product. Cover every target for default, primary-action, maximum-stress, and target-sensitive cases; cover every other applicable state at least once and add combinations where dimensions interact or defects were found.

## Output contract

Return a **runtime validation evidence packet** with:

1. build lock, build result, and unchanged confirmation
2. runtime environment and capture configuration
3. full-screen and focused evidence for every supported target
4. state/content/target/input coverage matrix with evidence IDs
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
- Exercise representative actual content, exact live formatting, all input edges, navigation, and persistence where applicable.
- Invalidate evidence if the build or fingerprint changes.
- Stop as blocked when required runtime, fixture, state, target, font, asset, or fingerprint cannot be reproduced.
- Stop after reporting findings and route defects to their owning stage without editing them.

Technical or geometry success does not prove art fidelity. The independent `game-ui-acceptance-review` owns the final UI verdict.
