---
run_id: screen-component-red-2
phase: RED
task_name: screen_component_red_2
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 48c4b201b15243b419f0f97057c79a8ea0dd31b638fc280092554d1caf5f6891
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Authority | Scope | Certainty | Status |
|---|---|---|---|---|
| Approved art-direction brief | Art direction | Reuse `primary-action@2.1.0` visual family | REQUIRED | Available; catalog decision and fingerprint are missing |
| Current request | Product/request context | Reward screen is needed today; labels and callbacks differ per screen | REQUIRED | Content, actions, states, destinations, and behavior are unspecified |
| Existing screenshots | Runtime/reference evidence | Similar visual appearance only | DERIVED | Not authority for reuse, geometry, or visual overrides |
| Reported `primaryButton` helper | Runtime code evidence | Possible existing implementation helper only | OPEN | Existence, version correspondence, and supported customization are unverified |
| Component catalog decision | Component-system authority | Ownership, compatible variants, override policy | BLOCKED | Required before treating helper as approved reuse |
| Artifact fingerprint | Component evidence | Exact `primary-action@2.1.0` artifact identity | BLOCKED | Required before reuse can be confirmed |

The reported helper and screenshots do not prove approved component reuse. Shadow and highlight overrides are `OPEN`; they cannot be authorized from a screenshot alone.

## 2. Protected content lock

| Item | Owner/source | Lock | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` | Approved art-direction brief | Preserve the named visual-family intent; do not assume a helper or screenshot is its canonical artifact | REQUIRED |
| Reward screen labels | Product authority | Exact copy, localization, and formatting must remain product-owned | OPEN |
| Reward values and data | Product/data authority | Data family, bounds, formatting, and fallback must be defined before mockup | OPEN |
| Callbacks and navigation | Product authority | Per-screen action behavior and persistence boundary must be defined | OPEN |
| Fonts, icons, and assets | Canonical owners | Use only approved, reproducibly located artifacts | OPEN |

## 3. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RWD-001 | Reward screen title | Product authority | All authorized states | OPEN | OPEN |
| RWD-002 | Reward description or reward value | Product/data authority | Applicable reward-present state | OPEN | OPEN |
| RWD-003 | Primary action label | Product authority | Applicable actionable state | Must use the approved component family only after catalog/fingerprint confirmation | OPEN |
| RWD-004 | Secondary labels, notices, errors, or progress text | Product authority | OPEN | OPEN | OPEN |

No exact labels, numerical formats, localization set, fallback copy, or boundaries were supplied.

## 4. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ACT-001 | Primary action using `primary-action@2.1.0` family | Art-direction brief; product authority required for behavior | OPEN | OPEN | OPEN |
| ACT-002 | Back/dismiss behavior | Product authority | OPEN | OPEN | OPEN |
| ACT-003 | Reward claim, acknowledgement, or continuation effect | Product authority | OPEN | OPEN | OPEN |

The primary action’s callback, availability rule, destination/effect, failure recovery, and persistence boundary are `OPEN`. No secondary action is authorized.

## 5. State matrix

| State | Entry condition | Visible content | Authorized transition/effect | Certainty |
|---|---|---|---|---|
| Reward screen initial state | OPEN | OPEN | OPEN | OPEN |
| Reward available | OPEN | OPEN | OPEN | OPEN |
| Reward unavailable/already claimed | OPEN | OPEN | OPEN | OPEN |
| Claim or action in progress | OPEN | OPEN | OPEN | OPEN |
| Success | OPEN | OPEN | OPEN | OPEN |
| Recoverable failure | OPEN | OPEN | OPEN | OPEN |

No state transitions, timing, side effects, scopes, or recovery behavior are currently authorized.

## 6. Responsive region contract

| Region | Order/containment | Target behavior | Safe-area behavior | Dimensions | Certainty |
|---|---|---|---|---|---|
| Top/title region | OPEN | OPEN | OPEN | OPEN | OPEN |
| Reward content region | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary action region | OPEN | OPEN | OPEN | OPEN | OPEN |
| System/navigation region | OPEN | OPEN | OPEN | OPEN | OPEN |

Screenshots are not sufficient authority for coordinates, breakpoints, dimensions, safe-area treatment, or overflow behavior.

## 7. Text-fit matrix

| Field family | Approved font/fallback | Locales | Shortest/longest representative strings | Numeric bounds | Fit policy | Certainty |
|---|---|---|---|---|---|---|
| Title | OPEN | OPEN | OPEN | N/A | OPEN | OPEN |
| Reward value/description | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary action label | OPEN | OPEN | OPEN | N/A | OPEN | OPEN |
| Status/error text | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |

## 8. Accessibility and input contract

| Contract | Source | Requirement | Certainty |
|---|---|---|---|
| Non-color state identity | Accessibility/product authority | OPEN | OPEN |
| Reduced-effects behavior | Accessibility/product authority | OPEN | OPEN |
| Semantic labels | Product/accessibility authority | OPEN | OPEN |
| Focus order and keyboard/controller behavior | Input authority | OPEN | OPEN |
| Back behavior | Product/navigation authority | OPEN | OPEN |
| Hit-area requirements | Input/accessibility authority | OPEN | OPEN |

## 9. Open decisions and handoff

`game-ui-mockup` requires the following approved inputs:

1. Component catalog decision confirming whether `primary-action@2.1.0` is reusable for this screen, its canonical artifact locator/fingerprint, and its allowed variant/override surface.
2. Explicit decision on shadow and highlight values: approved component variant, a new versioned variant, or an approved exception. Screenshot matching alone is insufficient.
3. Reward screen copy, localization scope, reward data format and bounds, empty/error/loading/claimed content, and fallbacks.
4. Authorized controls, callbacks, destinations, persistence boundary, availability rules, and recovery behavior.
5. Supported viewports, safe-area policy, responsive measurements or evidence, approved fonts/icons/assets, text-fit policy, and accessibility/input requirements.

Stop here pending those product and component-system decisions.
