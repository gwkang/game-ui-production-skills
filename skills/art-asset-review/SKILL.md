---
name: art-asset-review
description: Use when game UI assets need an independent quality, provenance, target-slot, or composed-screen fidelity verdict before implementation.
---

## Role
Independently decide whether production assets and verified reuse meet both technical and composed-screen craft requirements. Review is read-only; the producer cannot approve their own work.

## Inputs
- Approved art direction, production-representative mockup, handoff, and asset-readiness packet.
- Exact source/output hashes, rights, transforms, geometry, target slots, consumers, and production status.
- Source-parity rows for every visible art family.
- Target-size composites for every supported target using the exact intended runtime bytes.

## Work and handoff
1. Read the locked production/reuse packet and inspect both exact bytes and target-size composed screens.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Return the independent verdict and criterion-linked defects to game-ui-asset-production; never repair assets or evidence.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
