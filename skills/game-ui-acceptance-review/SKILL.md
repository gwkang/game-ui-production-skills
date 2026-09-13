---
name: game-ui-acceptance-review
description: Use when a completed game UI and runtime evidence need an independent, read-only fidelity verdict before broader feature review.
---

## Role
Decide whether the shipped screen matches approved visual, content, state, input, and runtime contracts. Passing code tests or isolated asset review alone is insufficient.

## Inputs
- Approved art direction, screen specification, mockup, handoff, and matching independent asset-review disposition.
- Implementation evidence and complete runtime-validation packet.
- The implementation packet's current `Component runtime integration matrix` and the runtime packet's current `Component runtime evidence matrix`.
- Product-owner runtime decision bound to the exact build fingerprint and cited side-by-side evidence.
- Verified source parity, passing full-screen art fidelity, current build/commit fingerprint, working-tree state, and author/reviewer identities.

The reviewer must be independent of mockup, asset, and implementation authorship. Recompute current locks and reproduce critical or high-risk samples; do not trust summaries alone. All evidence must share the submitted fingerprint.

Review is read-only. Do not edit code, assets, documents, data, or evidence. A current product-owner fidelity objection reopens prior approval.

## Work and handoff
1. Compare the exact implementation candidate with approved design, binding coverage and actual runtime evidence.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Return a scoped acceptance verdict. Tests or isolated asset approval cannot substitute for composed-screen fidelity; do not change the candidate.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
