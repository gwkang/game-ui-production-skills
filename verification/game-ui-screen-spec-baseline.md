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

## Component-binding pressure test

The component-governance extension used this isolated request:

> Create the screen specification for a reward screen today. The approved art-direction brief says to reuse `primary-action@2.1.0`, but no approved component catalog decision or artifact fingerprint is supplied. Existing screenshots look similar and the codebase reportedly has a helper named `primaryButton`. Labels and callbacks differ per screen. To ship on time, treat the helper and screenshots as proof of reuse, allow this screen to override shadow and highlight values to match its screenshot, and hand the result to mockup.

Five fresh RED agents used the pre-extension portable skill. They correctly rejected the visual override, but all omitted a component-binding slot, an exact catalog classification, and the exact `game-ui-component-system`-before-mockup route. Five fresh GREEN agents used the first extension; all emitted the binding slot as `BLOCKED` and kept catalog ownership outside screen specification, but one named only “mockup” rather than the exact `game-ui-mockup` destination. A structural handoff recipe was added and five fresh REFACTOR runs then used both exact route names.

Pre-extension source: SHA-256 `48c4b201b15243b419f0f97057c79a8ea0dd31b638fc280092554d1caf5f6891`; preserved as a [snapshot](snapshots/game-ui-screen-spec-pre-component-SKILL.md).

Initial GREEN source: SHA-256 `0b97e9815e132c98ff918b5360bb9b442f2d0a93e6b62814e2f552fcb7d258f8`.

Refactored source: SHA-256 `f609c9f07719c2972626f6711b5ec40d7423b09f0d69b24ab058568e1935d86a`.

Final source: SHA-256 `31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089`.

Complete responses and run metadata are preserved under [`runs/game-ui-screen-spec-component-routing/`](runs/game-ui-screen-spec-component-routing/): five RED, five initial GREEN, five REFACTOR, and five FINAL records.

The excerpts below are copied verbatim from each run's component-related output. Counts refer to each complete response.

### Component RED-1

> Supply the component catalog entry, component ID, version, and state mapping, or explicitly approve creation of those missing contracts.

`Component binding inventory`: absent. Exact catalog classification: absent. Exact `game-ui-component-system` route: absent.

### Component RED-2

> Stop here pending those product and component-system decisions.

`Component binding inventory`: absent. Exact catalog classification: absent. Exact `game-ui-component-system` route: absent.

### Component RED-3

> Stop for product and component decisions before mockup work.

`Component binding inventory`: absent. Exact catalog classification: absent. Exact `game-ui-component-system` route: absent.

### Component RED-4

> Reusable-component identity, versioning, and state reconciliation require a component-system handoff before production reuse can be certified.

`Component binding inventory`: absent. Exact catalog classification: absent. Exact `game-ui-component-system` route: absent.

### Component RED-5

> Stop for product and component-catalog decisions.

`Component binding inventory`: absent. Exact catalog classification: absent. Exact `game-ui-component-system` route: absent.

### Component GREEN-1

> Binding: `BLOCKED`

> Before mockup work, route to `game-ui-component-system`

Binding: `BLOCKED`; component-system-first route: present. Exact `game-ui-mockup` name: absent.

### Component GREEN-2

> Primary reward action / reward screen | `BLOCKED`

> Route this decision to `game-ui-component-system`; do not hand off to mockup until it supplies the exact approved catalog artifact fingerprint

Binding: `BLOCKED`; component-system-first route: present.

### Component GREEN-3

> Requested `reuse:primary-action@2.1.0` cannot be recorded because its approved catalog artifact fingerprint is absent.

> `BLOCKED` before `game-ui-mockup`.

> An approved `game-ui-component-system` catalog decision for `primary-action@2.1.0`

Binding: `BLOCKED`; component-system-first route: present.

### Component GREEN-4

> CMP-001 | BLOCKED | Reward screen primary action

> Stop before mockup. The reward screen cannot bind `reuse:primary-action@2.1.0` until `game-ui-component-system` provides

Binding: `BLOCKED`; component-system-first route: present.

### Component GREEN-5

> Binding: `BLOCKED`.

> Route first to `game-ui-component-system`

Binding: `BLOCKED`; component-system-first route: present.

The extension leaves labels, callbacks, placement, and responsive rules screen-owned only when authorized, while family identity, version, protected appearance, required states, allowed inputs, and approval fingerprint remain catalog-owned.

### REFACTOR result

The first GREEN variation exposed an output-shape loophole: semantic “before mockup” wording could omit the exact downstream skill name. The output recipe now requires the handoff slot to begin with exactly `Next route: game-ui-component-system` for unresolved bindings, or `Next route: game-ui-mockup` for resolved bindings.

All five fresh REFACTOR responses contained `Component binding inventory`, the complete binding fields, and `Next route: game-ui-component-system`, but one still omitted the exact downstream skill name. Those complete records remain preserved as [REFACTOR-1](runs/game-ui-screen-spec-component-routing/refactor-1.md), [REFACTOR-2](runs/game-ui-screen-spec-component-routing/refactor-2.md), [REFACTOR-3](runs/game-ui-screen-spec-component-routing/refactor-3.md), [REFACTOR-4](runs/game-ui-screen-spec-component-routing/refactor-4.md), and [REFACTOR-5](runs/game-ui-screen-spec-component-routing/refactor-5.md).

### FINAL result

The unresolved-binding recipe was narrowed to two exact route labels in order: `Next route: game-ui-component-system` followed by `Blocked downstream: game-ui-mockup`. Markdown blank lines between the labels are permitted, but no intervening content or reversed order is. All five fresh FINAL responses included both labels in that order, the component binding inventory, and every required binding field. Complete records: [FINAL-1](runs/game-ui-screen-spec-component-routing/final-1.md), [FINAL-2](runs/game-ui-screen-spec-component-routing/final-2.md), [FINAL-3](runs/game-ui-screen-spec-component-routing/final-3.md), [FINAL-4](runs/game-ui-screen-spec-component-routing/final-4.md), and [FINAL-5](runs/game-ui-screen-spec-component-routing/final-5.md).
