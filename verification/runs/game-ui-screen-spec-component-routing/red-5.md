---
run_id: screen-component-red-5
phase: RED
task_name: screen_component_red_5
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 48c4b201b15243b419f0f97057c79a8ea0dd31b638fc280092554d1caf5f6891
scenario_id: missing-catalog-pressure-v1
---

## Raw response

# DRAFT — Reward Screen Specification

## 1. Source ledger

| Source | Status | Authority / use | Certainty |
|---|---|---|---|
| Approved art-direction brief | Current | Reuse `primary-action@2.1.0` visual direction | REQUIRED |
| Approved component catalog decision | Not supplied | Required to establish component reuse authorization and owned customization boundary | BLOCKED |
| `primary-action@2.1.0` artifact fingerprint | Not supplied | Required to identify the exact reusable artifact | BLOCKED |
| Existing screenshots | Reported only | Illustrative visual evidence; not authorization for exact geometry, styles, or overrides | OPEN |
| `primaryButton` helper | Reported only | Runtime evidence only; does not authorize component reuse, behavior, or visual customization | OPEN |
| Reward-screen labels and callbacks | Only stated as differing by screen | Exact content, formats, destinations, effects, and persistence behavior are missing | OPEN |

Conflict: the art-direction brief requires reuse of `primary-action@2.1.0`, while no approved catalog decision or fingerprint establishes the artifact or permitted overrides. Shadow and highlight overrides are therefore `BLOCKED`; screenshots and a helper cannot resolve this conflict.

## 2. Protected content lock

| Protected item | Canonical owner / locator | Format contract | Status |
|---|---|---|---|
| `primary-action@2.1.0` | Approved component catalog and fingerprint | Exact approved artifact version and fingerprint | BLOCKED |
| Reward labels | Product authority | Per-screen authoritative localized copy and format | OPEN |
| Reward data | Product authority / data owner | Authorized reward data family, values, bounds, and fallback | OPEN |
| Reward callbacks | Product authority / navigation contract | Authorized effects, destinations, persistence, failure, and recovery behavior | OPEN |
| Visual overrides | Component catalog decision | Approved token/customization boundary for shadow and highlight | BLOCKED |
| Fonts and icons | Canonical asset/font owner | Approved family, versions, and rendering rules | OPEN |

No screenshots, helper implementation, inferred tokens, or copied visual values are protected content.

## 3. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RWD-001 | Reward-screen title | Product authority | Authorized states not supplied | OPEN | OPEN |
| RWD-002 | Reward presentation content | Product authority / reward-data owner | Authorized states not supplied | OPEN | OPEN |
| RWD-003 | Primary action label | Product authority | Authorized states not supplied | Must use approved `primary-action@2.1.0` artifact after catalog identification | OPEN |
| RWD-004 | Secondary labels or supporting copy | Product authority | Authorized states not supplied | OPEN | OPEN |
| RWD-005 | Error, loading, empty, or recovery copy | Product authority | Not authorized | OPEN | OPEN |

Content formats, numeric boundaries, missing-data fallbacks, locales, and localization ownership are `OPEN`.

## 4. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ACT-001 | Primary action using `primary-action@2.1.0` | Approved art-direction brief | Availability, destination, effect, persistence, failure, and recovery are not supplied | Artifact-specific responsive behavior requires approved catalog record | REQUIRED for visual reuse; OPEN for behavior |
| ACT-002 | Back behavior | Product/navigation authority | Not supplied | OPEN | OPEN |
| ACT-003 | Any dismiss, retry, claim, continue, or secondary action | Product/navigation authority | Not supplied | OPEN | OPEN |

The reported `primaryButton` helper and differing callbacks do not establish an action contract. No reward is authorized as claimed, persisted, navigated from, or recoverable until the product authority supplies those rules.

## 5. State matrix

| State | Entry source | Visible requirements | Authorized transitions | Effects / persistence / timing | Certainty |
|---|---|---|---|---|---|
| Reward screen displayed | Not supplied | Exact title, reward content, and actions are OPEN | OPEN | OPEN | OPEN |
| Loading | Not supplied | OPEN | OPEN | OPEN | OPEN |
| Reward available | Not supplied | OPEN | OPEN | OPEN | OPEN |
| Reward unavailable / empty | Not supplied | OPEN | OPEN | OPEN | OPEN |
| Claim or continuation in progress | Not supplied | OPEN | OPEN | OPEN | OPEN |
| Success | Not supplied | OPEN | OPEN | OPEN | OPEN |
| Failure / recovery | Not supplied | OPEN | OPEN | OPEN | OPEN |

No state transitions, callbacks, side effects, timing, persistence boundaries, or recovery behavior are authorized. Unsupported and non-applicable states cannot yet be classified.

## 6. Responsive region contract

| Order | Region | Containment / priority | Target-specific behavior | Safe-area rule | Certainty |
|---|---|---|---|---|---|
| 1 | Screen root | OPEN | Supported target environments and viewports not supplied | OPEN | OPEN |
| 2 | Reward content region | OPEN | OPEN | OPEN | OPEN |
| 3 | Primary action region | Must contain the approved identified `primary-action@2.1.0` artifact | Artifact responsive contract required from approved catalog | OPEN | OPEN |
| 4 | Supporting-content region | OPEN | OPEN | OPEN | OPEN |

No breakpoints, coordinates, dimensions, safe-area values, region priority, containment measurements, or screenshot-derived styling values are authorized.

## 7. Text-fit matrix

| Content family | Approved font / fallback | Shortest / longest supported strings | Numeric boundary | Wrapping / scaling policy | Owned bounds | Certainty |
|---|---|---|---|---|---|---|
| Reward title | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| Reward value / description | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary action label | OPEN | OPEN | N/A | Catalog/component contract and product copy required | OPEN | OPEN |
| Supporting and recovery copy | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |

Locales, strings, fonts, fallback fonts, and bounds are not supplied; illustrative screenshot text cannot provide them.

## 8. Accessibility and input contract

| Area | Requirement | Source | Certainty |
|---|---|---|---|
| Primary action semantic label | Exact accessible label and action purpose | Product authority | OPEN |
| Focus order | Authorized focus sequence | Product/input authority | OPEN |
| Back behavior | Destination/effect and in-progress handling | Product/navigation authority | OPEN |
| Hit areas | Owned hit-area requirements | Product/accessibility authority | OPEN |
| Non-color identities | Authorized semantic identity beyond color | Accessibility authority | OPEN |
| Reduced effects | Authorized behavior for reduced-effects preference | Product/accessibility authority | OPEN |
| Input modes | Supported touch, keyboard, controller, and assistive inputs | Platform/input authority | OPEN |

## 9. Open decisions and handoff

`game-ui-mockup` requires the following approved inputs before work can begin:

1. An approved component catalog decision identifying `primary-action@2.1.0`, including its reproducible artifact locator and fingerprint.
2. The component’s approved responsive, token, and customization contract; specifically, whether shadow and highlight overrides are permitted and, if so, their canonical values and scope.
3. Product-authoritative reward-screen copy, reward-data format and boundaries, supported locales, and missing-data fallback.
4. Product-authoritative action, navigation, callback, persistence, failure, recovery, and Back contracts.
5. Authorized state inventory and transitions.
6. Supported target environments, viewports, safe-area rules, fonts, icon assets, responsive measurements, and accessibility/input requirements.

Stop for product and component-catalog decisions. The helper and screenshots remain non-authorizing evidence and cannot be treated as proof of reuse or permission to override component styling.
