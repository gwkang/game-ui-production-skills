---
name: game-ui-art-direction
description: Use when an existing game's screen is visually inconsistent, off-brand, or needs an approved visual-direction brief before mockup or production work.
---

## Role
Define a screen's visual intent and source authority without redesigning product content or performing downstream production work.

## Inputs
- Current user decisions that affect the screen.
- The project's authoritative product and visual-design documents.
- Approved screen-specific references and their current or superseded status.
- The approved component catalog when repeated visual families, claimed reuse, or component drift are in scope.
- A current runtime capture when diagnosing an existing screen; treat it as evidence, not design authority.

Record unavailable inputs as `OPEN` or `BLOCKED`. Do not infer the project name, genre, platform, runtime, viewport, locale, content, interaction model, or accessibility requirements from common conventions.

## Work and handoff
1. Resolve source authority and the intended visual experience; classify reusable family needs.
2. Use [the detailed output and acceptance rules](references/output-contract.md) for the current stage; preserve exact schema keys and all required approval/coverage gates.
3. Produce the direction brief only. Keep DRAFT until actual product-owner approval; route family decisions to game-ui-component-system.

## Verification boundary
Before checking, fix the selected artifact/revision, criteria, target and permitted repair scope. A separate subagent verifies; the author repairs only returned in-scope defects and the verifier rechecks affected criteria. Preserve valid unaffected evidence. Use the recorded retry budget (default two); block on exhaustion or unavailable independent verification. Defer out-of-scope observations without adding work or gates. Verification reports receive supervisor scope/evidence checks, not recursive reviewer chains.
