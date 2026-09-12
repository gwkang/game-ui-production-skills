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
- The approved `game-ui-component-system` catalog decision and exact artifact fingerprint when a repeated family or reuse claim is in scope.
- Content, data, behavior, navigation, font, input, and accessibility contracts.
- Supported target environments, viewports, safe areas, locales, and runtime evidence when an implementation exists.

Record unavailable required inputs as `OPEN` or `BLOCKED`. Do not replace them with platform conventions, placeholder copy, remembered standards, or values from unrelated projects.

## Source and certainty rule

For every requirement, record its source and one certainty:

- `REQUIRED` — stated by a current authority.
- `DERIVED` — calculated from cited evidence; include the derivation and assumptions.
- `OPEN` — not yet authorized or measurable.

Product authority owns content and behavior. Art direction owns visual intent. The component catalog owns reusable-family identity, version, protected properties, required states, and allowed instance inputs. The screen specification owns only the consumer's authorized content, actions, placement, and responsive rules. Runtime code and captures are evidence, not permission to preserve a defect. Baked text, numbers, and icons in a visual reference are illustrative unless another authority makes them exact.

A supplied state or control name does not authorize its transitions, side effects, scope, timing, or recovery behavior. Record those fields as `OPEN` unless the authority states them explicitly.

## Output contract

Return one `DRAFT` **Screen specification** with these slots:

1. **Source ledger** — current authorities, conflicts, superseded material, missing inputs, and certainty labels.
2. **Protected content lock** — assets, fonts, icons, copy, data families, and behavior that must survive unchanged. Use reproducible locators and hashes when available; use canonical owners and format contracts for live content.
3. **Component binding inventory** — for every repeated family, record exactly `reuse:<componentId>@<version>`, `screen-specific-exception`, `new-family-required`, or `BLOCKED`; include the catalog artifact fingerprint, consumer, allowed instance inputs, inherited protected properties and required states, and the screen-owned rules. A helper name or visual similarity is not a binding.
4. **Content inventory** — each visible label and live field, its source, format, valid boundary, fallback, and certainty.
5. **Action and navigation inventory** — each control, availability rule, destination or effect, persistence boundary, and certainty.
6. **State matrix** — every authorized state and explicitly sourced transition; keep unspecified transitions, effects, timing, and state scope `OPEN`, and mark unsupported or non-applicable states explicitly.
7. **Responsive region contract** — ordered regions, containment, priority, target-specific behavior, safe areas, and evidence-based dimensions.
8. **Text-fit matrix** — approved fonts and fallbacks, representative shortest and longest strings for every supported locale, numeric boundaries, wrapping or scaling policy, and owned bounds.
9. **Accessibility and input contract** — authorized non-color identities, reduced-effects behavior, semantic labels, focus and Back behavior, and hit-area requirements.
10. **Open decisions and handoff** — when any binding is unresolved, start with exactly `Next route: game-ui-component-system` and then `Blocked downstream: game-ui-mockup`; otherwise start with exactly `Next route: game-ui-mockup`. Then list unresolved choices and the exact approved inputs that route needs.

Use this row shape for inventories: `ID | visible content or action | source | states | responsive rule | certainty`.

## Scope boundary

- Do not generate or outline a mockup.
- Do not create assets, write image-generation prompts, or write implementation code.
- Do not turn current coordinates or common platform values into requirements without cited authority or measurement.
- Do not invent copy, currency, prices, controls, states, breakpoints, geometry, fonts, limits, or accessibility thresholds.
- Do not omit conditional content merely because it is absent from one capture.
- Do not create, revise, approve, or version a component catalog. Do not turn screen-owned labels, callbacks, or placement into permission to override catalog-owned protected properties or required states.

## Verification and approval

- Trace every visible field, action, state, and responsive rule to the source ledger; there must be no orphan requirements.
- Exercise authorized content boundaries and supported locales without substituting invented examples for missing data.
- Confirm every cited locator exists or is explicitly `OPEN` or `BLOCKED`.
- Confirm every reuse binding matches the exact approved catalog artifact fingerprint and uses only declared instance inputs, consumers, and required states.
- Confirm every output slot is present and no downstream artifact was produced.
- Keep the specification `DRAFT` until the designated product owner explicitly approves it. Art-direction or mockup approval does not approve this contract.

Stop for a product decision when authorities conflict or a required product value is missing. Stop when a missing, stale, or conflicting component catalog decision or artifact fingerprint prevents binding; route to `game-ui-component-system` before `game-ui-mockup`. Also return there when a requested consumer, instance input, protected-property change, or required state is not covered. Stop after the draft specification and hand only resolved, approved input to `game-ui-mockup`.

## Runtime coverage map contract

The screen specification owns the coverage map consumed by runtime validation. Include it with the state/target specification, preserving existing output slots and approvals.

Emit `Runtime coverage map` and the plain pipe-delimited header:

`coverage ID | consumer | state | viewport | fixture | interaction | reason | baseline`

Each row has a unique stable ID, one declared consumer, one exact state and viewport, a reproducible authorized fixture, an interaction or observation, a selection reason, and baseline YES or NO. Declare exactly one baseline state per consumer and cover it at every supported viewport. Cover every other required state at least once, all primary actions and content stress boundaries, and extra targets where state/target interactions require them. Do not invent default states or expand to a full Cartesian product without a requirement.

Trace row values to current sources. Required unknowns remain OPEN/BLOCKED. Runtime validation must not choose substitute targets, fixtures or baseline states. Changes to this map reopen affected evidence and approvals under the existing contract.
