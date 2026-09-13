---
name: game-ui-handoff
description: Use when an approved game UI mockup needs a measurable implementation contract before asset or code work.
---

## Role
Translate approved visual evidence into measurable geometry, ownership, scaling, and state rules without producing assets or code.

## Inputs
- Approved `game-ui-art-direction`, `game-ui-screen-spec`, and `game-ui-mockup` artifacts.
- The approved mockup's `Component reuse-fidelity matrix`, with a current `MATCH` row for every reusable binding.
- Exact selected composite paths, dimensions, hashes, represented states, provenance, and product-owner decision.
- Protected-content and source-parity records.
- Supported targets, safe areas, reusable components, and current implementation evidence when available.

Stop when an input is missing, stale, conflicting, or bound to a different hash.

## Work and handoff
1. Measure approved references and transfer catalog state IDs plus mockup evidence into the binding contract.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Produce geometry, ownership and state rules with the exact binding matrix. Do not produce assets/code; unresolved bindings return to component-system.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
