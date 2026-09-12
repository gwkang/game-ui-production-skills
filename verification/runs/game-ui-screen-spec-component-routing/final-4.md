---
run_id: screen-component-final-4
phase: FINAL
task_name: screen_component_final_4
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — reward screen

## 1. Source ledger

| Source | Authority | Status | Certainty |
|---|---|---|---|
| Approved art-direction brief (locator not supplied) | Visual intent; requests `primary-action@2.1.0` reuse | Current, but component binding is unverified | REQUIRED |
| Current request | Reward screen exists; labels and callbacks vary by screen | Current | REQUIRED |
| Existing screenshots (locators not supplied) | Illustrative appearance only | Not a component-reuse authority | OPEN |
| Reported `primaryButton` helper | Runtime evidence only; exact locator and behavior absent | Not a component-reuse authority | OPEN |
| Approved component catalog decision | Required for repeated-family binding | Missing | BLOCKED |
| Catalog artifact fingerprint for `primary-action@2.1.0` | Required for reuse binding | Missing | BLOCKED |
| Product content/behavior authority | Reward content, actions, transitions, persistence, locales, and accessibility | Missing | BLOCKED |

Conflict: the art-direction brief requests reuse while no approved catalog decision or fingerprint establishes that `primary-action@2.1.0` is bindable. Screenshot-matching shadow/highlight overrides are not authorized because those may be catalog-protected properties.

## 2. Protected content lock

| Item | Lock | Source | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` family identity, version, protected properties, required states | Must remain governed by the approved catalog; no consumer override is authorized | Missing catalog decision/fingerprint | BLOCKED |
| Reward-screen labels | Exact copy, locale set, and text ownership must come from product authority | Missing product content authority | BLOCKED |
| Reward values/data | Format, valid range, fallback, and data owner are required | Missing product/data authority | BLOCKED |
| Icons, imagery, fonts, and visual assets | Canonical locators, licenses, hashes, and allowed use are required | Missing approved asset/font inputs | OPEN |
| Reward action behavior and persistence | Must not change without product and platform authority | Missing behavior/persistence contract | BLOCKED |

## 3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | `BLOCKED` — requested `reuse:primary-action@2.1.0`; required catalog artifact fingerprint, approved consumer, allowed instance inputs, inherited protected properties, and required states are absent | Art-direction brief request; catalog decision/fingerprint missing | Required states unknown | Screen placement and target behavior unknown | BLOCKED |

Consumer: reward screen.

Allowed instance inputs: `OPEN`; differing labels and callbacks do not establish allowed inputs.

Inherited protected properties and required states: `BLOCKED` pending the approved catalog artifact fingerprint.

Screen-owned rules: placement, label selection, callback wiring, availability, and responsive behavior are `OPEN` pending product authority and catalog binding.

Requested shadow/highlight overrides: `BLOCKED`. They cannot be treated as screen-owned until the catalog explicitly declares them as allowed instance inputs.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-content | Reward title, description, reward value, labels, icons, and any conditional content | Product authority missing | Authorized states unknown | Target layout rules unknown | BLOCKED |

Content format, boundaries, fallbacks, and locales: `OPEN`.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Primary reward-screen action; exact label and callback differ per screen | Product authority missing; catalog binding blocked | Availability unknown | Hit area and placement unknown | BLOCKED |
| reward-navigation | Dismissal, destination, Back behavior, and recovery | Product authority missing | Transitions unknown | Target behavior unknown | BLOCKED |

Persistence boundary: `OPEN`.

## 6. State matrix

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen | Reward screen state scope, entry, exit, success, failure, loading, unavailable, and recovery states | Product authority missing | All transitions, effects, timing, and scope are `OPEN` | Unknown | BLOCKED |
| primary-action | Catalog-required component states | Approved catalog artifact fingerprint missing | `OPEN` | Unknown | BLOCKED |

Unsupported or non-applicable states: `OPEN`; no authority identifies them.

## 7. Responsive region contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-regions | Ordered reward-screen regions and containment | Missing approved screen/product evidence | Authorized states unknown | Safe areas, viewport targets, breakpoints, dimensions, priorities, and overflow behavior are `OPEN` | BLOCKED |

No screenshot-derived coordinates, spacing, shadow, or highlight values are requirements.

## 8. Text-fit matrix

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-copy | Every reward-screen string and live numeric field | Product authority missing | Authorized states unknown | Fonts, fallback fonts, locale set, shortest/longest strings, numeric boundaries, owned bounds, and wrap/scale policy are `OPEN` | BLOCKED |
| primary-action-label | Primary-action label | Product authority and catalog binding missing | Required states unknown | Label fit and component-owned bounds are `OPEN` | BLOCKED |

## 9. Accessibility and input contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-accessibility | Non-color identities, reduced-effects behavior, semantic labels, focus order, Back behavior, and hit areas | Accessibility/product authority missing | Authorized states unknown | Target input behavior unknown | BLOCKED |

## 10. Open decisions and handoff

Next route: game-ui-component-system
Blocked downstream: game-ui-mockup

- Supply the approved `primary-action@2.1.0` catalog decision and exact artifact fingerprint.
- Confirm the reward screen is an approved consumer, its permitted instance inputs, inherited protected properties, required states, and whether shadow/highlight values may be overridden.
- Supply the approved product authority for reward-screen copy, data formats and boundaries, action callbacks, navigation, persistence, state transitions, locales, and accessibility/input behavior.
- Supply supported target viewports, safe-area rules, approved fonts/assets, and measurable responsive evidence.
