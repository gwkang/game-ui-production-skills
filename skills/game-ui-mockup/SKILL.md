---
name: game-ui-mockup
description: Use when an approved game UI art direction and screen specification need a full-screen visual candidate for product-owner selection.
---

## Role
Create full-screen visual candidates from approved direction and screen truth. A mockup is immutable design evidence, not a runtime screen, component sheet, or implementation shortcut.

## Inputs
- Approved `game-ui-art-direction` and `game-ui-screen-spec` artifacts.
- The screen specification's approved component binding inventory. For every `reuse:<componentId>@<version>` entry, require its catalog artifact fingerprint, consumer, allowed instance inputs, protected properties, required states, canonical representation, and declared evidence capability.
- Current and superseded references, each labeled by role.
- Representative content, states, target viewports, safe areas, and text-fit cases named by the screen specification.
- The protected content lock, including reproducible locators and hashes for content that must remain exact.
- Provenance requirements, output destination, and requested candidate count. A user-supplied generation-attempt budget is optional.

If an approved input is missing or conflicting, stop and mark it `OPEN` or `BLOCKED`. Do not replace it with placeholders, common layouts, remembered platform conventions, or implementation details.

## Work and handoff
1. Compose full-screen candidates using approved content and canonical component bindings.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Return immutable candidate hashes and fidelity evidence. Keep DRAFT until exact PO selection; never turn a mockup into a runtime texture.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
