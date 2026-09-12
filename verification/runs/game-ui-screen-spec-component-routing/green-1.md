---
run_id: screen-component-green-1
phase: GREEN
task_name: screen_component_green_1
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 0b97e9815e132c98ff918b5360bb9b442f2d0a93e6b62814e2f552fcb7d258f8
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — Reward screen (today)

## 1. Source ledger

| Authority/input | Scope | Status | Certainty |
|---|---|---|---|
| Approved art-direction brief | Requires reuse of `primary-action@2.1.0` | Current | REQUIRED |
| Approved component catalog decision | Reusable-family identity, allowed inputs, protected properties, required states | Not supplied | BLOCKED |
| Component artifact fingerprint for `primary-action@2.1.0` | Exact reusable artifact verification | Not supplied | BLOCKED |
| Existing screenshots | Illustrative visual evidence only | Reported, not an approved authority | OPEN |
| `primaryButton` runtime helper | Implementation evidence only | Reported, not a component binding | OPEN |
| Reward-screen product authority | Reward content, actions, callbacks, persistence, navigation, state behavior | Not supplied | BLOCKED |
| Viewport, safe-area, locale, font, accessibility contracts | Responsive and accessibility requirements | Not supplied | BLOCKED |

Conflict: the requested use of screenshots and a helper name as proof of reuse conflicts with the component-binding requirement. The reported per-screen labels and callbacks do not authorize changes to component-owned shadow or highlight properties.

## 2. Protected content lock

| Item | Canonical owner/source | Contract | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` reusable-family identity | Approved art-direction brief; catalog decision required | Must remain the named intended reusable family; exact artifact and protected properties cannot be verified | BLOCKED |
| Reward-screen labels | Product authority | Copy, locale strings, formatting, and fallback are not supplied | OPEN |
| Reward content/data | Product authority | Reward type, value, currency/data family, valid range, and fallback are not supplied | OPEN |
| Action callbacks and persistence | Product authority | Effects and save/acknowledgement boundary are not supplied | OPEN |
| Fonts, icons, assets | Product/art authority | Canonical assets, formats, and locators are not supplied | OPEN |

No reproducible asset locator or hash is available.

## 3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| C-01 | Primary reward-screen action | Approved art-direction brief requires `primary-action@2.1.0`; catalog decision and fingerprint absent | Required states unknown | Unknown | BLOCKED |

Binding record:

- Binding: `BLOCKED`
- Intended component: `reuse:primary-action@2.1.0`
- Consumer: reward screen — not approved by the catalog
- Catalog artifact fingerprint: `BLOCKED` — not supplied
- Allowed instance inputs: `BLOCKED` — not supplied
- Inherited protected properties: `BLOCKED` — not supplied
- Required states: `BLOCKED` — not supplied
- Screen-owned rules: labels and callbacks are reported to differ by screen, but their allowed binding surface is `BLOCKED`
- Requested shadow/highlight overrides: `BLOCKED`; those may be catalog-owned protected properties and cannot be authorized from screenshots or a helper name

`primaryButton` and similar-looking screenshots are not a reusable-component binding.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| CT-01 | Reward-screen title | Product authority | Unknown | Unknown | OPEN |
| CT-02 | Reward description | Product authority | Unknown | Unknown | OPEN |
| CT-03 | Reward value and unit/data representation | Product authority | Unknown | Unknown | OPEN |
| CT-04 | Primary action label | Product authority; component catalog defines whether it is an allowed instance input | Unknown | Unknown | BLOCKED |
| CT-05 | Supplementary/error/loading text, if any | Product authority | Unknown | Unknown | OPEN |

For all content, source locators, formats, valid boundaries, locale coverage, and fallbacks are `OPEN`.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| AC-01 | Primary reward-screen action | Product authority; intended component from art-direction brief | Availability, effect, callback, destination, and persistence boundary unknown | Unknown | BLOCKED |
| AC-02 | Dismissal, Back, or secondary action, if any | Product authority | Unknown | Unknown | OPEN |

No action effect, navigation destination, persistence confirmation rule, failure recovery, or callback contract has been supplied.

## 6. State matrix

| State | Authorized transition/effect | Scope/timing/recovery | Certainty |
|---|---|---|---|
| Reward screen initial display | Not supplied | OPEN | OPEN |
| Reward available | Not supplied | OPEN | OPEN |
| Reward claim/continue action | Not supplied | OPEN | OPEN |
| Reward persistence pending | Not supplied | OPEN | OPEN |
| Reward persistence success | Not supplied | OPEN | OPEN |
| Reward persistence failure | Not supplied | OPEN | OPEN |
| Loading/unavailable reward | Not supplied | OPEN | OPEN |
| Disabled primary action | Required-state applicability not supplied by catalog or product authority | OPEN | BLOCKED |
| Pressed/focused/selected primary action | Required-state applicability not supplied by catalog | OPEN | BLOCKED |
| Unsupported/non-applicable states | No authority supplied | OPEN | OPEN |

## 7. Responsive region contract

| Region | Ordered containment/priority | Target behavior | Safe-area/dimensions | Certainty |
|---|---|---|---|---|
| R-01 | Reward-screen root | Unknown | Unknown | OPEN |
| R-02 | Reward content region | Unknown | Unknown | OPEN |
| R-03 | Primary action region | Unknown | Unknown | BLOCKED |
| R-04 | Optional secondary/navigation region | Unknown | Unknown | OPEN |

No supported viewport, orientation, safe-area, breakpoint, measurement, or runtime evidence is supplied. Screenshots cannot establish reusable responsive requirements.

## 8. Text-fit matrix

| Content | Font/fallback | Locales | Shortest/longest strings | Numeric boundary | Wrapping/scaling/owned bounds | Certainty |
|---|---|---|---|---|---|---|
| Reward title | OPEN | OPEN | OPEN | N/A | OPEN | OPEN |
| Reward description | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Reward value | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary action label | OPEN; component constraints may be catalog-owned | OPEN | OPEN | N/A | OPEN | BLOCKED |
| Supplementary state text | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |

## 9. Accessibility and input contract

| Requirement | Source | Contract | Certainty |
|---|---|---|---|
| Non-color state identities | Accessibility/product authority | Not supplied | OPEN |
| Reduced-effects behavior | Accessibility/product authority | Not supplied | OPEN |
| Semantic labels | Accessibility/product authority | Not supplied | OPEN |
| Focus order and focus indication | Accessibility/product authority; component catalog for the primary action | Not supplied | BLOCKED |
| Back behavior | Product authority | Not supplied | OPEN |
| Hit-area requirements | Accessibility/product authority; component catalog where applicable | Not supplied | BLOCKED |

## 10. Open decisions and handoff

This specification remains `DRAFT`.

Before mockup work, route to `game-ui-component-system` for:

1. An approved `primary-action@2.1.0` catalog decision.
2. The exact artifact fingerprint.
3. Approved reward-screen consumer status.
4. Declared allowed instance inputs, including whether label and callback binding are permitted.
5. Protected properties and required states.
6. An explicit decision on shadow/highlight customization; screenshots and `primaryButton` do not authorize an override.

Before completing the screen contract, obtain product authority for reward content, copy, action effects, callbacks, navigation, persistence behavior, error/recovery states, target viewports, locales, typography, responsive rules, and accessibility/input requirements.

No mockup handoff is authorized until the blocked component binding is resolved and the product inputs are approved.
