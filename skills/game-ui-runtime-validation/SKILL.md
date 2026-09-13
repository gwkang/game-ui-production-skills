---
name: game-ui-runtime-validation
description: Use when an implemented game UI needs actual-runtime evidence for rendering, content, states, input, and fidelity before acceptance review.
---

## Role
Validate an unchanged build in its actual runtime. Static tests do not prove rendered fidelity, loaded assets, content boundaries, or usable input geometry.

## Inputs
- Approved screen specification, mockup, handoff comparison map, asset verdict, and implementation evidence.
- The implementation packet's current `Component runtime integration matrix` and matching catalog artifact fingerprint.
- Exact build fingerprint, launch/capture method, fixture data, expected states, targets, locales, and safe areas.
- Approved composite hashes and source-parity records.

Use the project's declared browser, engine, emulator, simulator, device, or capture harness. For each run record environment, scale, target dimensions, safe area, fixture, state, locale, timestamp, and fingerprint; recheck the fingerprint after capture.

Check the approved design artifact's identity separately from capture freshness. A historical approval record can remain intact after code changes, but it says nothing about the current build; changed design authorities require their own relevance review. Before presenting a capture as a current approval candidate, run the project's declared freshness/readiness check against the current source and build, not only the archived evidence snapshot. A scoped `PASS` or author-written readiness label never overrides an overall `BLOCKED`, missing required coverage rows, missing raw evidence, or changed capture inputs. If no executable check exists, compare the complete locked source/build inventories and required coverage against the raw evidence explicitly; unresolved or stale evidence stays `BLOCKED` and cannot be sent for acceptance or product-owner runtime approval.

Validation is repository-read-only. Interact only through normal runtime controls and isolated fixture state. Do not fix code, assets, data, or evidence, and never self-approve.

## Work and handoff
1. Observe an unchanged candidate in its actual runtime using selected screen/state/viewport coverage and source identity.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Return raw observations and coverage verdicts for acceptance review. Do not repair product or evidence during verification.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
