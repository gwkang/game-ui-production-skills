---
name: game-ui-implementation
description: Use when approved game UI specifications, handoff measurements, and independently reviewed assets are ready for runtime integration.
---

# Game UI Implementation

## Overview

Implement the approved UI contract without redesigning content, behavior, typography, navigation, or economy. Keep visual, live-data, layout, and input ownership explicit and testable.

## Required inputs

- Approved screen specification and handoff.
- Product-owner mockup approval bound to exact composite hashes.
- Asset-readiness packet in an explicit production mode and a matching independent `Decision: APPROVE ASSET QUALITY`.
- Source-parity records, supported targets, acceptance map, component/state IDs, and current code/data/input/test owners.

Before tests or code, recompute the input locks. Every visible art family must be `new production` or `verified reuse`, with none missing, and target-size evidence must use the intended runtime bytes. Return stale, incomplete, mismatched, or unapproved inputs upstream.

## Implementation contract

Inspect repository impacts and preserve unrelated changes using project-provided tools. For each behavior or layout requirement:

1. add the smallest focused test
2. run it and record the expected pre-change failure
3. implement only enough to pass
4. rerun focused tests before proceeding

Map every component and state to its asset, layout owner, live text/data owner, input owner, states, and fallback. Keep dynamic values live. Use declared intrinsic/visible geometry, anchors, safe areas, and fit modes. A mockup or screenshot is never a runtime hit surface.

Do not change approved copy, content, currency, font, navigation, Back behavior, persistence, availability, or state rules to simplify implementation. Do not use runtime tint, outline, scale, glow, or spacing to conceal missing or mismatched production art.

## Output contract

Maintain an **implementation evidence packet** with:

1. input lock, hashes, approvals, parity records, supported targets, and exclusions
2. impact map, consumers, shared files, and preserved changes
3. component integration map: ID, asset/frame, layout, live content, input rectangle, states, and fallback
4. RED evidence: focused command, expected failure, and pre-change output
5. GREEN implementation: minimal code path and passing focused output
6. contract preservation before/after for product-owned content and behavior
7. deviation ledger: zero deviations or exact source, reason, measured effect, owner decision, and approval
8. changed files, tests, purposes, and commands
9. open decisions and locked build inputs for `game-ui-runtime-validation`

## Scope and verification

- Do not generate, repair, or compensate for art; return art defects to `game-ui-asset-production`.
- Do not invent missing geometry, responsive behavior, states, or product facts.
- Run focused tests for layout, content binding, states, input geometry, navigation, persistence, and approved boundary cases.
- Confirm every handoff row has a runtime consumer and no extra UI or behavior was introduced.
- Run project-required test/build/audit commands, but do not claim rendered fidelity before runtime validation.

Stop for missing approval, source parity, measurements, states, assets, or product authority. Stop if work would change an out-of-scope product contract. After GREEN evidence, route the unchanged build to runtime validation.
