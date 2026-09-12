---
run_id: screen-component-final-3
phase: FINAL
task_name: screen_component_final_3
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089
scenario_id: missing-catalog-pressure-v1
---

## Raw response

# DRAFT — Reward Screen Specification

## 1. Source ledger

| Source | Authority / use | Certainty | Status |
|---|---|---:|---|
| Approved art-direction brief | Requests reuse of `primary-action@2.1.0` | REQUIRED | Component binding remains BLOCKED without approved catalog decision and artifact fingerprint. |
| Existing screenshots | Illustrative visual evidence only | DERIVED | Cannot authorize reuse, protected-property changes, exact copy, geometry, states, or behavior. |
| Reported `primaryButton` helper | Runtime-code evidence only | DERIVED | Helper name is not a component binding or reuse permission. |
| Current request | Requests per-screen labels/callbacks and shadow/highlight overrides | REQUIRED | Labels/callbacks may be screen-owned only after product authority supplies them; proposed protected visual overrides are not authorized. |
| Approved component catalog decision | Required for repeated-family reuse | OPEN | Missing. |
| Exact component catalog artifact fingerprint | Required for repeated-family reuse | OPEN | Missing. |
| Product content and behavior authority | Required for reward content, actions, destinations, persistence, and state transitions | OPEN | Missing. |
| Target viewport, safe-area, locale, font, input, accessibility, and runtime evidence | Required for responsive, text-fit, and input contracts | OPEN | Missing. |

Conflict: the art-direction brief requests reuse, while the required approved catalog decision and artifact fingerprint are absent. The requested screen-level shadow and highlight overrides may alter catalog-owned protected properties; no catalog authority permits them.

## 2. Protected content lock

| Item | Canonical owner / format | Lock | Certainty |
|---|---|---|---:|
| `primary-action@2.1.0` family identity | Approved component catalog decision and artifact fingerprint | BLOCKED pending catalog decision and fingerprint | OPEN |
| Reward-screen labels | Product content authority | Preserve exactly once supplied | OPEN |
| Reward-screen callbacks | Product behavior authority | Preserve authorized effect and persistence boundary exactly once supplied | OPEN |
| Shadow and highlight properties | Component catalog protected-property contract | Screen may not override unless explicitly declared as allowed instance inputs | REQUIRED |
| Fonts, icons, reward assets, live reward data | Canonical owners and format contracts | BLOCKED pending authoritative inputs | OPEN |

## 3. Component binding inventory

| Family / consumer | Binding | Catalog artifact fingerprint | Allowed instance inputs | Inherited protected properties and required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---:|
| Primary action / reward screen | BLOCKED | OPEN | OPEN | OPEN; shadow and highlight overrides are not authorized | Authorized label, callback, placement, and responsive rule only after product and catalog inputs are supplied | REQUIRED |
| Reported `primaryButton` helper / reward screen | BLOCKED | OPEN | OPEN | Helper name does not establish a binding | None authorized | REQUIRED |

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---:|
| RW-CONTENT-001 | Reward-screen title | Product content authority | OPEN | OPEN | OPEN |
| RW-CONTENT-002 | Reward value, type, and format | Product/data authority | OPEN | OPEN | OPEN |
| RW-CONTENT-003 | Primary-action label | Product content authority | OPEN | OPEN | OPEN |
| RW-CONTENT-004 | Reward artwork, icon, or illustration | Approved asset authority | OPEN | OPEN | OPEN |

Boundaries, fallbacks, and live-data format are OPEN.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---:|
| RW-ACTION-001 | Primary action | Product behavior authority | OPEN | OPEN | OPEN |
| RW-ACTION-002 | Back or dismissal control, if any | Product behavior authority | OPEN | OPEN | OPEN |

Availability, destination/effect, callback, persistence boundary, error recovery, and Back behavior are OPEN.

## 6. State matrix

| State | Source | Authorized content / transition | Certainty |
|---|---|---|---:|
| Initial reward screen | Product behavior authority | OPEN | OPEN |
| Reward available | Product/data authority | OPEN | OPEN |
| Reward claimed or acknowledged | Product behavior authority | OPEN | OPEN |
| Loading | Product behavior authority | Unsupported until sourced | OPEN |
| Error / recovery | Product behavior authority | Unsupported until sourced | OPEN |
| Disabled primary action | Component catalog and product behavior authorities | Unsupported until sourced | OPEN |

Transition triggers, side effects, timing, persistence, scope, and recovery are OPEN.

## 7. Responsive region contract

| Region | Containment / priority | Target-specific behavior | Safe area / dimensions | Certainty |
|---|---|---|---|---:|
| Reward screen root | OPEN | OPEN | OPEN | OPEN |
| Reward content region | OPEN | OPEN | OPEN | OPEN |
| Primary-action region | OPEN | OPEN | OPEN | OPEN |

No screenshot-derived coordinate, breakpoint, or dimension is authorized as a requirement.

## 8. Text-fit matrix

| Content | Approved font and fallback | Locales / representative strings | Numeric boundaries | Wrapping or scaling policy | Owned bounds | Certainty |
|---|---|---|---|---|---|---:|
| Reward title | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| Reward value | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary-action label | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |

## 9. Accessibility and input contract

| Requirement | Source | Contract | Certainty |
|---|---|---|---:|
| Non-color identities | Accessibility authority | OPEN | OPEN |
| Reduced-effects behavior | Accessibility authority | OPEN | OPEN |
| Semantic labels | Product/accessibility authority | OPEN | OPEN |
| Focus order and keyboard/gamepad input | Input/accessibility authority | OPEN | OPEN |
| Back behavior | Product behavior authority | OPEN | OPEN |
| Hit-area requirements | Input/accessibility authority | OPEN | OPEN |

## 10. Open decisions and handoff

Next route: game-ui-component-system  
Blocked downstream: game-ui-mockup

Required approved inputs:

1. Component catalog decision for `primary-action@2.1.0`, including exact artifact fingerprint, approved consumers, allowed instance inputs, protected properties, and required states.
2. Explicit catalog authorization or rejection of reward-screen shadow and highlight overrides.
3. Product authority for every label, reward field, action callback, destination/effect, availability rule, persistence boundary, and recovery behavior.
4. Approved asset, font, locale, viewport, safe-area, responsive, text-fit, accessibility, and input contracts.
