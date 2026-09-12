---
run_id: screen-component-refactor-5
phase: REFACTOR
task_name: screen_component_refactor_5
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: f609c9f07719c2972626f6711b5ec40d7423b09f0d69b24ab058568e1935d86a
scenario_id: missing-catalog-pressure-v1
---

## Raw response

DRAFT Screen specification

1. Source ledger

| Authority / evidence | Scope | Status / certainty |
|---|---|---|
| Approved art-direction brief | Reuse `primary-action@2.1.0` | REQUIRED |
| Approved component catalog decision | Reusable-family identity, protected properties, states, allowed inputs | BLOCKED — not supplied |
| Component catalog artifact fingerprint | Exact reusable artifact binding | BLOCKED — not supplied |
| Existing screenshots | Illustrative visual reference only | DERIVED — similarity is not reuse authorization |
| Reported `primaryButton` helper | Runtime evidence only | OPEN — helper name is not a component binding |
| Current request | Reward screen exists; labels and callbacks vary by screen | REQUIRED |
| Product authority | Reward content, behavior, navigation, persistence, states, copy, locales | OPEN — not supplied |

No authority permits a screen-specific override of the reusable family’s shadow or highlight values.

2. Protected content lock

| Item | Canonical owner / locator | Protection | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` reusable-family identity | Approved art-direction brief | Requested family identity must not be substituted by a helper or screenshot similarity | REQUIRED |
| Component version, protected properties, required states, allowed instance inputs | Approved component catalog decision and artifact fingerprint | Must remain catalog-defined; unavailable until supplied | BLOCKED |
| Reward-screen labels | Product authority | Exact copy, locale variants, and formatting must survive unchanged once approved | OPEN |
| Reward callbacks and side effects | Product authority | Per-screen callback semantics and persistence boundary must survive unchanged once approved | OPEN |
| Fonts, icons, assets, data families | Product/art authority | Canonical owners, locators, and format contracts are absent | OPEN |

3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | BLOCKED | Approved art-direction brief requests `primary-action@2.1.0`; catalog decision and artifact fingerprint absent | Catalog-required states BLOCKED | Screen placement and sizing OPEN | BLOCKED |

Binding record:

- Binding: `BLOCKED`
- Requested reusable family: `reuse:primary-action@2.1.0`
- Catalog artifact fingerprint: BLOCKED
- Consumer authorization: BLOCKED
- Allowed instance inputs: BLOCKED
- Inherited protected properties: BLOCKED
- Required states: BLOCKED
- Screen-owned rules: labels and callbacks differ per screen, but their exact values and behavior are OPEN.
- Shadow and highlight overrides: BLOCKED. These are catalog-owned unless the approved catalog explicitly declares them as allowed instance inputs.
- `primaryButton` helper and screenshots: evidence only; neither establishes reuse binding.

4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-title | Reward product authority | Unknown | Containing region, wrapping, locale behavior OPEN | OPEN |
| reward-description | Reward product authority | Unknown | Containing region, wrapping, locale behavior OPEN | OPEN |
| reward-value | Reward data/product authority | Unknown | Format, numeric boundary, fallback, and responsive behavior OPEN | OPEN |
| reward-primary-label | Reward product authority | Unknown | May vary by screen; exact copy and locale variants OPEN | OPEN |

5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Primary reward-screen action | Product authority | Availability, destination/effect, callback, persistence boundary, failure/recovery behavior OPEN | Hit area and responsive placement OPEN | OPEN |
| system-back | Back behavior | Product authority | Destination and state-dependent behavior OPEN | Input behavior OPEN | OPEN |

6. State matrix

| State | Authorized visible content | Authorized transition / effect | Certainty |
|---|---|---|---|
| Reward screen initial | Reward screen is requested; exact fields OPEN | Entry source, timing, data loading, and scope OPEN | OPEN |
| Primary action available | Primary action is requested | Availability conditions, callback, destination/effect, and persistence boundary OPEN | OPEN |
| Primary action unavailable | No authority supplied | Not applicable until authorized | OPEN |
| Processing | No authority supplied | Not applicable until authorized | OPEN |
| Success | No authority supplied | Not applicable until authorized | OPEN |
| Failure / recovery | No authority supplied | Not applicable until authorized | OPEN |

7. Responsive region contract

| Region | Containment / priority | Target-specific behavior | Certainty |
|---|---|---|---|
| Safe-area shell | Contains all reward-screen regions | Supported viewports and safe-area policy OPEN | OPEN |
| Reward content region | Contains title, description, and reward value if authorized | Ordering, dimensions, spacing, overflow behavior OPEN | OPEN |
| Primary-action region | Contains the blocked reusable-family binding | Placement, minimum/maximum bounds, and collision behavior OPEN | OPEN |

No screenshot coordinates, breakpoints, geometry, or platform conventions are adopted as requirements.

8. Text-fit matrix

| Text family | Font / fallback | Representative strings | Boundary / policy | Certainty |
|---|---|---|---|---|
| Reward title | OPEN | Supported locales and shortest/longest approved strings OPEN | Bounds, wrapping, scaling, truncation policy OPEN | OPEN |
| Reward description | OPEN | Supported locales and shortest/longest approved strings OPEN | Bounds, wrapping, scaling, truncation policy OPEN | OPEN |
| Reward value | OPEN | Numeric range, locale formatting, and fallback OPEN | Bounds and overflow policy OPEN | OPEN |
| Primary-action label | Catalog/product authority BLOCKED | Per-screen labels and locale variants OPEN | Catalog-owned text behavior and screen-owned bounds BLOCKED | BLOCKED |

9. Accessibility and input contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action semantic label | Product/catalog authority | Unknown | State-specific label and announcement OPEN | Hit-area requirements OPEN | OPEN |
| Non-color identity | Product/art authority | Unknown | Reduced-effects behavior OPEN | Responsive behavior OPEN | OPEN |
| Focus behavior | Product/catalog authority | Unknown | Entry, order, and disabled-state focus OPEN | Target-specific behavior OPEN | OPEN |
| Back behavior | Product authority | Unknown | State-dependent destination/effect OPEN | Input modality behavior OPEN | OPEN |

10. Open decisions and handoff

Next route: game-ui-component-system

- Supply the approved component-catalog decision for `primary-action@2.1.0`.
- Supply the exact catalog artifact fingerprint.
- Confirm the reward screen is an authorized consumer.
- Declare the reusable family’s protected properties, required states, and allowed instance inputs.
- Explicitly decide whether shadow and highlight values are protected or permitted instance inputs; screenshots and `primaryButton` cannot authorize an override.
- Supply product authority for reward-screen copy, data formatting, action availability, callbacks, destinations/effects, persistence boundary, recovery behavior, supported locales, target viewports, safe areas, text-fit rules, and accessibility/input behavior.
- After the binding is resolved and product inputs are approved, hand only those resolved inputs to `game-ui-mockup`.
