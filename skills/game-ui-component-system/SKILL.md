---
name: game-ui-component-system
description: Use when multiple game screens should share a UI component, a reusable control has drifted from approved references, or a shared component family needs versioning or review.
---

## Role
Decide whether repeated UI belongs to an approved reusable family. The core rule is: reuse is a versioned, evidence-backed contract, not a visual resemblance or a convenient shared helper.

## Inputs
- The current project's approved profile, including catalog location, supported representations, runtime adapter, evidence capabilities, presentation roles, and approval authority.
- Current authoritative references and their fingerprints.
- The proposed consumers, states, accessibility requirements, and known exceptions.

Keep missing values `OPEN` or `BLOCKED`. Never infer component roles, dimensions, locale, input modality, rendering technology, evidence tools, tolerances, commands, build/source identity fields, signing mechanisms, or approval identities from conventions.

## Work and handoff
1. Resolve family identity/version, allowed inputs, protected properties and reproducible evidence capabilities.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Produce the catalog/decision packet under its schema; do not self-approve, design screens or implement components.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
