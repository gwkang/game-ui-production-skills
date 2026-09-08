---
name: game-ui-screen-spec
description: Use when an existing game screen needs an exact content, state, interaction, text-fit, or responsive contract before visual mockup work.
---

# Game UI Screen Specification

## Overview

Turn approved visual direction and product authority into a truthful screen contract. Every visible or interactive requirement has a source, certainty, and responsive rule.

## Required inputs

- An approved `game-ui-art-direction` brief.
- Current user decisions, authoritative product documents, and approved screen references.
- Content, data, behavior, navigation, font, input, and accessibility contracts.
- Supported target environments, viewports, safe areas, locales, and runtime evidence when an implementation exists.

Record unavailable required inputs as `OPEN` or `BLOCKED`. Do not replace them with platform conventions, placeholder copy, remembered standards, or values from unrelated projects.

## Source and certainty rule

For every requirement, record its source and one certainty:

- `REQUIRED` — stated by a current authority.
- `DERIVED` — calculated from cited evidence; include the derivation and assumptions.
- `OPEN` — not yet authorized or measurable.

Product authority owns content and behavior. Art direction owns visual intent. Runtime code and captures are evidence, not permission to preserve a defect. Baked text, numbers, and icons in a visual reference are illustrative unless another authority makes them exact.

A supplied state or control name does not authorize its transitions, side effects, scope, timing, or recovery behavior. Record those fields as `OPEN` unless the authority states them explicitly.

## Output contract

Return one `DRAFT` **Screen specification** with these slots:

1. **Source ledger** — current authorities, conflicts, superseded material, missing inputs, and certainty labels.
2. **Protected content lock** — assets, fonts, icons, copy, data families, and behavior that must survive unchanged. Use reproducible locators and hashes when available; use canonical owners and format contracts for live content.
3. **Content inventory** — each visible label and live field, its source, format, valid boundary, fallback, and certainty.
4. **Action and navigation inventory** — each control, availability rule, destination or effect, persistence boundary, and certainty.
5. **State matrix** — every authorized state and explicitly sourced transition; keep unspecified transitions, effects, timing, and state scope `OPEN`, and mark unsupported or non-applicable states explicitly.
6. **Responsive region contract** — ordered regions, containment, priority, target-specific behavior, safe areas, and evidence-based dimensions.
7. **Text-fit matrix** — approved fonts and fallbacks, representative shortest and longest strings for every supported locale, numeric boundaries, wrapping or scaling policy, and owned bounds.
8. **Accessibility and input contract** — authorized non-color identities, reduced-effects behavior, semantic labels, focus and Back behavior, and hit-area requirements.
9. **Open decisions and handoff** — unresolved choices and the exact approved inputs needed by `game-ui-mockup`.

Use this row shape for inventories: `ID | visible content or action | source | states | responsive rule | certainty`.

## Scope boundary

- Do not generate or outline a mockup.
- Do not create assets, write image-generation prompts, or write implementation code.
- Do not turn current coordinates or common platform values into requirements without cited authority or measurement.
- Do not invent copy, currency, prices, controls, states, breakpoints, geometry, fonts, limits, or accessibility thresholds.
- Do not omit conditional content merely because it is absent from one capture.

## Verification and approval

- Trace every visible field, action, state, and responsive rule to the source ledger; there must be no orphan requirements.
- Exercise authorized content boundaries and supported locales without substituting invented examples for missing data.
- Confirm every cited locator exists or is explicitly `OPEN` or `BLOCKED`.
- Confirm every output slot is present and no downstream artifact was produced.
- Keep the specification `DRAFT` until the designated product owner explicitly approves it. Art-direction or mockup approval does not approve this contract.

Stop for a product decision when authorities conflict or a required product value is missing. Stop after the draft specification and hand approved input to `game-ui-mockup`.
