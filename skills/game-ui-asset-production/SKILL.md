---
name: game-ui-asset-production
description: Use when an approved game UI handoff has visible art families that need production readiness or reuse verification before implementation.
---

## Role
Turn an approved handoff into a reproducible, independently reviewable asset-readiness packet while keeping live content and input in code.

## Inputs
- Approved art direction, screen specification, mockup, and handoff.
- The handoff's current `Component implementation binding matrix` and the exact approved component catalog artifact or project-declared resolver for its fingerprint.
- Locked sources, hashes, geometry, states, fit rules, target slots, and consumers.
- Rights, license, bundle budget, runtime asset conventions, and migration authority.

## Work and handoff
1. Use only the handoff-authorized production/reuse mode. Preserve canonical identity, states, protected properties and deterministic provenance.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Produce the asset-readiness packet and exact disposition matrix; send to art-asset-review before implementation.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
