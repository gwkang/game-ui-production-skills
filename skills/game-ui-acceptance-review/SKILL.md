---
name: game-ui-acceptance-review
description: Use when a completed game UI and runtime evidence need an independent, read-only fidelity verdict before broader feature review.
---

# Game UI Acceptance Review

## Overview

Decide whether the shipped screen matches approved visual, content, state, input, and runtime contracts. Passing code tests or isolated asset review alone is insufficient.

## Required inputs

- Approved art direction, screen specification, mockup, handoff, and matching independent asset-review disposition.
- Implementation evidence and complete runtime-validation packet.
- The implementation packet's current `Component runtime integration matrix` and the runtime packet's current `Component runtime evidence matrix`.
- Product-owner runtime decision bound to the exact build fingerprint and cited side-by-side evidence.
- Verified source parity, passing full-screen art fidelity, current build/commit fingerprint, working-tree state, and author/reviewer identities.

The reviewer must be independent of mockup, asset, and implementation authorship. Recompute current locks and reproduce critical or high-risk samples; do not trust summaries alone. All evidence must share the submitted fingerprint.

Review is read-only. Do not edit code, assets, documents, data, or evidence. A current product-owner fidelity objection reopens prior approval.

## Component acceptance contract

Emit one **Component acceptance matrix**. Emit this exact title once, followed by the exact header on the next line with no blank line:

`Component acceptance matrix`

`binding | catalog artifact fingerprint | build fingerprint | consumer | declared adapter | required states | runtime evidence IDs | protected-property verdict | open severity | component verdict`

Build every row by this ten-cell recipe. Index the implementation and runtime matrices by their exact headers. Copy binding, catalog artifact fingerprint, consumer, declared adapter, and required states verbatim; insert the reviewed build fingerprint; list the exact raw runtime evidence IDs for every required state; summarize only their current protected-property result; record `NONE`, `P0`, `P1`, `P2`, or `P3`; and put only `ACCEPTED` or `REJECTED` in component verdict. In `runtime evidence IDs`, join the exact IDs in required coverage order with comma-space (`, `) only; do not append fingerprints, status, annotations, or prose.

- `ACCEPTED` requires evidence at the same build fingerprint for every required state and protected property, complete required target coverage, no identity conflict, and no open P0/P1/P2.
- `REJECTED` covers missing evidence, stale evidence, conflicting evidence, partial evidence, substitute evidence, a missing required state or protected property, identity mismatch, or any open P0/P1/P2.

Aggregate screen results cannot replace component-by-component state, identity, and protected-property closure. A row labeled verified in a stale runtime packet remains stale runtime evidence; product-owner approval, asset approval, passing geometry, or aggregate logs cannot make it current.

For missing, stale, or incomplete runtime capture/probe evidence, emit `Next route: game-ui-runtime-validation`. For a current observed adapter, state, input, or protected-property implementation defect, emit `Next route: game-ui-implementation`. For binding identity, contract, declared-adapter, or catalog-fingerprint conflict, emit `Next route: game-ui-component-system`. Keep art-quality defects with the existing art owner.

Any `REJECTED` component requires a line containing only `Decision: REJECT UI`; put its one rationale on the next line. It blocks broader feature review. Never emit `Decision: APPROVE FEATURE`; this skill can only route an accepted UI to the separate broader feature review.

## Output contract

Return one **UI acceptance report** with:

1. reviewer identity, excluded roles, conflicts, and date
2. commit/build fingerprint, working-tree state, and evidence match
3. artifact/state/content/target/input evidence sufficiency and gaps, including the Component acceptance matrix
4. visual landmark fidelity for every supported target
5. composed-screen art quality for every visible family and actual representative content
6. exact content, font, data, navigation, availability, persistence, input, and accessibility fidelity
7. runtime quality: clipping, overflow, aspect, edge artifacts, states, hit geometry, logs, font/asset load, and unwanted scroll
8. findings with severity, evidence, requirement, actual, owner, and reopen condition
9. exactly `Decision: APPROVE UI` or `Decision: REJECT UI`, with one rationale
10. next route: broader feature review or the owning upstream stage

Use project severity definitions when supplied; otherwise use the runtime-validation defaults.

The independent asset-review disposition is `NOT APPLICABLE` only when the packet has no produced or file-backed art. `Decision: APPROVE ASSET QUALITY` remains required when the packet has any produced or file-backed art. `NOT APPLICABLE` waives only the nonexistent file-art verdict; it does not waive packet readiness, full-screen rendered fidelity, source parity, or component runtime evidence.

`Decision: APPROVE UI` requires that applicable asset-review condition, passing full-screen art fidelity, complete current evidence, product-owner runtime approval for the same fingerprint, verified parity, no open P0/P1/P2, and no unapproved difference. A P3 may remain only when the product owner accepts that exact deviation and fingerprint. Missing, stale, conflicting, partial, or substitute evidence requires rejection.

## Verification and stop conditions

- Recompute the fingerprint and confirm no file changes during review.
- Inspect original-detail runtime evidence beside exact approved composites.
- Trace every screen-spec field, state, action, and required target to evidence.
- Reproduce a risk-based sample of boundaries, center/edge inputs, disabled behavior, navigation, persistence, logs, fonts, and assets.
- Reject missing families, craft/style mismatch, stale runtime approval, parity conflict, or approval for another fingerprint.
- Route defects without fixing them and stop after the report.

This is a UI gate, not broader feature approval. Product-owner approval is required but does not replace independent evidence review.
