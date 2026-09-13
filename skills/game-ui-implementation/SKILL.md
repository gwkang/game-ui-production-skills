---
name: game-ui-implementation
description: Use when approved game UI specifications, handoff measurements, and independently reviewed assets are ready for runtime integration.
---

## Role
Implement the approved UI contract without redesigning content, behavior, typography, navigation, or economy. Keep visual, live-data, layout, and input ownership explicit and testable.

## Inputs
- Approved screen specification and handoff.
- The handoff's current `Component implementation binding matrix`.
- Product-owner mockup approval bound to exact composite hashes.
- Asset-readiness packet in an explicit production mode and its matching independent asset-review disposition.
- The asset packet's current `Component production disposition matrix`, binding readiness, and packet readiness.
- Source-parity records, supported targets, acceptance map, component/state IDs, and current code/data/input/test owners.

Before tests or code, recompute the input locks. Every visible art family must be `new production` or `verified reuse`, with none missing, and target-size evidence must use the intended runtime bytes. Return stale, incomplete, mismatched, or unapproved inputs upstream.

The independent asset-review disposition is `NOT APPLICABLE` only when the packet has no produced or file-backed art. `Decision: APPROVE ASSET QUALITY` remains required when the packet has any produced or file-backed art. In both cases require packet readiness, source parity, and target-size rendered evidence; `NOT APPLICABLE` waives only the nonexistent file-art verdict.

For every reusable binding, require the same catalog identity and `catalog artifact fingerprint` in the handoff, asset packet, and current catalog. The handoff row must be `READY`, the asset binding must be `READY_FOR_IMPLEMENTATION`, and the asset packet must be `READY_FOR_IMPLEMENTATION`. A code-native or native-widget component may be `ASSET_NOT_REQUIRED`, but that never waives binding or packet readiness.

## Work and handoff
1. Implement only approved content, geometry, components and reviewed assets; separate live data, layout and input ownership.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Return the implementation packet for runtime validation. Do not redesign or claim acceptance from successful compilation.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
