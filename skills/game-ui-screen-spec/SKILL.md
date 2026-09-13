---
name: game-ui-screen-spec
description: Use when an existing game screen needs an exact content, state, interaction, text-fit, or responsive contract before visual mockup work.
---

## Role
Turn approved visual direction and product authority into a truthful screen contract. Every visible or interactive requirement has a source, certainty, and responsive rule.

## Inputs
- An approved `game-ui-art-direction` brief.
- Current user decisions, authoritative product documents, and approved screen references.
- The approved `game-ui-component-system` catalog decision and exact artifact fingerprint when a repeated family or reuse claim is in scope.
- Content, data, behavior, navigation, font, input, and accessibility contracts.
- Supported target environments, viewports, safe areas, locales, and runtime evidence when an implementation exists.

Record unavailable required inputs as `OPEN` or `BLOCKED`. Do not replace them with platform conventions, placeholder copy, remembered standards, or values from unrelated projects.

## Work and handoff
1. Trace visible content, state, input and responsive rules to product authority and exact reusable bindings.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Produce the screen contract and runtime coverage map. Keep required design approval separate from changing implementation evidence; do not invent thresholds or downstream work.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
