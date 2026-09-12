---
run_id: screen-component-green-3
phase: GREEN
task_name: screen_component_green_3
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 0b97e9815e132c98ff918b5360bb9b442f2d0a93e6b62814e2f552fcb7d258f8
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT — Reward Screen Specification

## 1. Source ledger

| Authority / evidence | Scope | Status / certainty |
|---|---|---|
| Approved art-direction brief (reported) | Requests `primary-action@2.1.0` reuse | `REQUIRED`; locator unavailable |
| Current request | Reward screen exists; labels and callbacks vary by screen | `REQUIRED` |
| Approved component catalog decision | Reuse identity, protected properties, states, allowed inputs | `BLOCKED`; not supplied |
| Component artifact fingerprint | Exact reusable artifact verification | `BLOCKED`; not supplied |
| Product authority | Reward content, eligibility, persistence, navigation, behavior | `OPEN`; not supplied |
| Existing screenshots | Visual evidence only | `OPEN`; no locator supplied; not reuse permission |
| `primaryButton` helper | Runtime evidence only | `OPEN`; reported only; not a component binding |

Conflict: the requested reuse cannot be bound without the approved catalog decision and exact artifact fingerprint. Screenshot similarity and a helper name do not resolve that conflict.

## 2. Protected content lock

| Item | Canonical owner / locator | Contract | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` visual family | Approved component catalog and artifact fingerprint | Identity, version, protected properties, required states, and allowed instance inputs must remain catalog-owned | `BLOCKED` |
| Reward labels | Product authority | Exact copy, locales, and formatting must be supplied | `OPEN` |
| Reward data | Product authority / live data contract | Data family, validity boundaries, and fallback behavior must be supplied | `OPEN` |
| Callbacks and reward effects | Product authority | Effects, timing, persistence boundary, failure recovery, and navigation must be supplied | `OPEN` |
| Fonts, icons, and assets | Approved authority and reproducible locators | Exact assets and format contracts must be supplied | `OPEN` |

No screenshot-derived shadow or highlight override is authorized. Those values are catalog-owned unless an approved catalog decision explicitly declares them screen-owned instance inputs.

## 3. Component binding inventory

| Family / consumer | Binding | Catalog fingerprint | Allowed instance inputs | Inherited protected properties / required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---|
| Primary reward action / reward screen | `BLOCKED` | `BLOCKED` | `BLOCKED` | `BLOCKED` | Labels, callbacks, and placement remain screen-owned only after product and catalog authorization | `BLOCKED` |

Requested `reuse:primary-action@2.1.0` cannot be recorded because its approved catalog artifact fingerprint is absent. `primaryButton` and similar screenshots are not a binding. Shadow and highlight overrides are not authorized.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RWD-CONTENT-001 | Reward screen title | Product authority | `OPEN` | `OPEN` | `OPEN` |
| RWD-CONTENT-002 | Reward description / amount / item field | Product authority and data contract | `OPEN` | `OPEN` | `OPEN` |
| RWD-CONTENT-003 | Primary action label | Product authority | `OPEN` | Bound only after catalog decision; placement remains `OPEN` | `OPEN` |
| RWD-CONTENT-004 | Any secondary, status, error, or explanatory text | Product authority | `OPEN` | `OPEN` | `OPEN` |

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RWD-ACTION-001 | Primary reward action | Product authority | Availability, destination/effect, persistence, timing, and recovery are `OPEN` | Hit area and placement `OPEN` | `OPEN` |
| RWD-ACTION-002 | Back / dismissal behavior | Product authority | `OPEN` | `OPEN` | `OPEN` |

No callback or navigation behavior is authorized by a supplied control name.

## 6. State matrix

| State | Entry condition | Visible content | Authorized transition / effect | Certainty |
|---|---|---|---|---|
| Reward screen default | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Reward action available | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Reward action unavailable | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Reward processing | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Reward success | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Reward failure / recovery | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Loading / empty / expired | Unsupported or non-applicable status is `OPEN` | `OPEN` | `OPEN` | `OPEN` |

## 7. Responsive region contract

| Region order | Containment and priority | Target-specific behavior / safe area | Evidence | Certainty |
|---|---|---|---|---|
| 1. Screen shell | `OPEN` | `OPEN` | No supported viewport, safe-area, or runtime evidence supplied | `OPEN` |
| 2. Reward content region | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| 3. Primary action region | `OPEN` | Must remain separate from catalog-owned component geometry until a valid binding exists | `OPEN` | `OPEN` |
| 4. Navigation / dismissal region | `OPEN` | `OPEN` | `OPEN` | `OPEN` |

## 8. Text-fit matrix

| Field | Approved font / fallback | Locale strings and numeric boundaries | Wrap / scale policy | Owned bounds | Certainty |
|---|---|---|---|---|---|
| Reward title | `OPEN` | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Reward description / value | `OPEN` | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Primary action label | `OPEN` | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| Status / error copy | `OPEN` | `OPEN` | `OPEN` | `OPEN` | `OPEN` |

## 9. Accessibility and input contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RWD-A11Y-001 | Non-color reward and action identities | Product authority / accessibility contract | `OPEN` | `OPEN` | `OPEN` |
| RWD-A11Y-002 | Reduced-effects behavior | Product authority / component catalog | `OPEN` | `OPEN` | `OPEN` |
| RWD-A11Y-003 | Semantic labels, focus order, and Back behavior | Product authority / input contract | `OPEN` | `OPEN` | `OPEN` |
| RWD-A11Y-004 | Hit-area requirements | Product authority / component catalog | `OPEN` | `OPEN` | `OPEN` |

## 10. Open decisions and handoff

`BLOCKED` before `game-ui-mockup`.

Required approved inputs:

1. An approved `game-ui-component-system` catalog decision for `primary-action@2.1.0`, including the exact artifact fingerprint, permitted consumers, allowed instance inputs, protected properties, required states, and whether shadow/highlight values may ever be overridden.
2. Product authority for the reward model, exact content, labels, eligibility, actions, callbacks, persistence boundary, navigation, failure recovery, and state transitions.
3. Supported viewports, safe-area policy, locales, approved fonts, text boundaries, input behavior, and accessibility requirements.
4. Reproducible locators for the art-direction brief and any approved screen references or runtime evidence.

No mockup handoff is authorized until the component binding is resolved and the above screen-owned product contracts are approved.
