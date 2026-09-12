---
name: game-ui-acceptance-review
description: Use when a completed game UI and runtime evidence need an independent, read-only fidelity verdict before broader feature review.
---

# Game UI Acceptance Review

## Overview

Decide whether the shipped screen matches approved visual, content, state, input, and runtime contracts. Passing code tests or isolated asset review alone is insufficient.

## Required inputs

- Approved art direction, screen specification, mockup, handoff, and matching `Decision: APPROVE ASSET QUALITY`.
- Implementation evidence and complete runtime-validation packet.
- Product-owner runtime decision bound to the exact build fingerprint and cited side-by-side evidence.
- Verified source parity, passing full-screen art fidelity, current build/commit fingerprint, working-tree state, and author/reviewer identities.

The reviewer must be independent of mockup, asset, and implementation authorship. Recompute current locks and reproduce critical or high-risk samples; do not trust summaries alone. All evidence must share the submitted fingerprint.

Review is read-only. Do not edit code, assets, documents, data, or evidence. A current product-owner fidelity objection reopens prior approval.

## Output contract

Return one **UI acceptance report** with:

1. reviewer identity, excluded roles, conflicts, and date
2. commit/build fingerprint, working-tree state, and evidence match
3. artifact/state/content/target/input evidence sufficiency and gaps
4. visual landmark fidelity for every supported target
5. composed-screen art quality for every visible family and actual representative content
6. exact content, font, data, navigation, availability, persistence, input, and accessibility fidelity
7. runtime quality: clipping, overflow, aspect, edge artifacts, states, hit geometry, logs, font/asset load, and unwanted scroll
8. findings with severity, evidence, requirement, actual, owner, and reopen condition
9. exactly `Decision: APPROVE UI` or `Decision: REJECT UI`, with one rationale
10. next route: broader feature review or the owning upstream stage

Use project severity definitions when supplied; otherwise use the runtime-validation defaults.

`Decision: APPROVE UI` requires matching asset approval, passing full-screen art fidelity, complete current evidence, product-owner runtime approval for the same fingerprint, verified parity, no open P0/P1/P2, and no unapproved difference. A P3 may remain only when the product owner accepts that exact deviation and fingerprint. Missing, stale, conflicting, partial, or substitute evidence requires rejection.

## Verification and stop conditions

- Recompute the fingerprint and confirm no file changes during review.
- Inspect original-detail runtime evidence beside exact approved composites.
- Trace every screen-spec field, state, action, and required target to evidence.
- Reproduce a risk-based sample of boundaries, center/edge inputs, disabled behavior, navigation, persistence, logs, fonts, and assets.
- Reject missing families, craft/style mismatch, stale runtime approval, parity conflict, or approval for another fingerprint.
- Route defects without fixing them and stop after the report.

This is a UI gate, not broader feature approval. Product-owner approval is required but does not replace independent evidence review.
