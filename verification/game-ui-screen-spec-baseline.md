# game-ui-screen-spec baseline

## Scenario

The baseline agent was not given the skill and was asked to create a final shop screen specification under deadline pressure while no product, art-direction, runtime, viewport, locale, content, state, accessibility, or navigation authority was available.

## Observed baseline

The agent correctly called its answer provisional, but still invented a portrait viewport, responsive breakpoints, layout percentages, English labels, touch sizes, product states, purchase behavior, accessibility thresholds, and seven downstream mockup frames.

Exact excerpts:

> Reference viewport: 390 × 844 dp, portrait. Support 320–430 dp widths and safe-area insets.

> Header: 8% of usable height; back button, centered “Shop” title, optional currency balance.

> Touch targets: minimum 48 × 48 dp with at least 8 dp separation.

> Temporary labels: Screen title: “Shop”; Categories: “Featured”, “Items”, “Decor”.

> A purchase requiring confirmation uses a modal with item, quantity if applicable, price, balance impact, confirm, and cancel.

> Prepare these frames first: Default loaded shop at 390 × 844 dp ... Purchase confirmation modal ... Empty category state.

## Required behavior

With the skill, every requirement must trace to a supplied authority and carry a certainty. Missing product facts and measurements remain `OPEN` or `BLOCKED`; they are not replaced with common conventions or placeholders. The response stops at a `DRAFT` screen specification and does not outline or generate a mockup.

## Refactor trigger

The first complete-input forward test inferred transitions such as loading to loaded/empty and retry to loading from state and control names alone. That result was rejected. The skill was tightened so names do not authorize transitions, side effects, scope, timing, or recovery behavior; all remain `OPEN` without an explicit source.

## Forward-test results

| Scenario | Required result | Result |
|---|---|---|
| Missing authority plus deadline pressure | Keep unsupported content, geometry, states, accessibility values, and navigation `OPEN` or `BLOCKED`; do not outline a mockup | PASS |
| Product contract conflicts with an incomplete runtime capture | Preserve required Back/loading/empty/error behavior, treat capture coordinates as evidence, reject a conventional hit-area value, and stop before mockup | PASS |
| Complete bounded authority | Produce a useful specification from supplied facts while leaving unspecified transitions, effects, timing, state scope, layout, and content bounds `OPEN` | PASS after one refactor |

All accepted responses remained `DRAFT`, included the nine required slots, and produced no mockup, asset, prompt, code, or file change. Tests were isolated from the host repository and original project-specific skill.
