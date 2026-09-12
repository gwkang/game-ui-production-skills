---
run_id: screen-component-final-1
phase: FINAL
task_name: screen_component_final_1
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Authority / evidence | Status |
|---|---|---|
| Current request | A reward screen is needed today. | REQUIRED |
| Approved art-direction brief | Requests reuse of `primary-action@2.1.0`. | REQUIRED visual intent; BLOCKED component binding |
| Component catalog decision | No approved catalog decision supplied. | BLOCKED |
| Component artifact fingerprint | No exact fingerprint supplied. | BLOCKED |
| Existing screenshots | Visually similar references. | Evidence only; not reuse permission |
| Reported `primaryButton` helper | Reported runtime helper exists. | Evidence only; not reuse permission |
| Screen-specific labels and callbacks | Differ per screen. | REQUIRED distinction; exact values and behavior OPEN |
| Shadow/highlight override request | Requested to match a screenshot. | BLOCKED; catalog-owned protected-property change cannot be authorized by this screen specification |

## 2. Protected content lock

| Item | Contract | Source | Certainty |
|---|---|---|---|
| Art-direction visual intent | Preserve the approved reward-screen visual direction. Exact locator unavailable. | Approved art-direction brief | REQUIRED |
| `primary-action@2.1.0` identity | Do not claim or implement reuse until the approved catalog decision and exact artifact fingerprint are supplied. | Approved art-direction brief; missing catalog inputs | BLOCKED |
| Shadow and highlight values | Do not override at screen level. Ownership and permitted instance inputs are unknown. | Missing catalog decision | BLOCKED |
| Reward content, labels, reward data, callbacks | Preserve only once product authority supplies exact content, format, behavior, and persistence rules. | Current request | OPEN |
| Fonts, icons, assets, live data format | No canonical owner, locator, hash, or format supplied. | Missing inputs | OPEN |

## 3. Component binding inventory

| ID | Binding | Consumer | Catalog fingerprint | Allowed instance inputs | Inherited protected properties / required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---|---|
| CMP-PRIMARY-ACTION | BLOCKED | Reward screen primary action, if product authority requires one | BLOCKED | BLOCKED | BLOCKED, including shadow and highlight | Labels, callbacks, placement, and availability remain OPEN pending product authority and catalog binding | BLOCKED |

`primaryButton` and similar screenshots are not component bindings. The requested screenshot-specific shadow/highlight override is not authorized.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| CNT-REWARD-SCREEN | Reward-screen title or heading | Current request; exact copy absent | OPEN | OPEN | OPEN |
| CNT-REWARD-VALUE | Reward type, amount, format, and fallback | Current request; exact data contract absent | OPEN | OPEN | OPEN |
| CNT-REWARD-DESCRIPTION | Explanatory or eligibility content, if any | No product authority supplied | OPEN | OPEN | OPEN |
| CNT-PRIMARY-ACTION-LABEL | Primary-action label | Labels reportedly vary by screen; exact label absent | OPEN | OPEN | OPEN |

No copy, currency, icon, numeric boundary, fallback, or data format is authorized.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ACT-PRIMARY | Reward-screen primary action, if required | Current request; callback, destination, availability, effect, persistence boundary, failure handling, and recovery absent | OPEN | OPEN | OPEN |
| ACT-BACK | Back or dismissal behavior, if applicable | No authority supplied | OPEN | OPEN | OPEN |

## 6. State matrix

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ST-REWARD | Reward-screen state model | Current request does not define states, transitions, effects, timing, scope, loading, success, failure, retry, dismissal, or recovery | OPEN | OPEN | OPEN |
| ST-PRIMARY-ACTION | Component states for a primary action, if used | Requires approved component catalog decision and fingerprint | BLOCKED | BLOCKED | BLOCKED |

Unsupported and non-applicable states cannot be identified until product and component authorities are supplied.

## 7. Responsive region contract

| Region | Containment / priority | Target-specific behavior | Safe-area rule | Evidence / certainty |
|---|---|---|---|---|
| Reward-screen regions | Region order, containment, geometry, priority, breakpoints, and target viewport behavior are not supplied. | OPEN | OPEN | Current request; OPEN |
| Primary-action placement | Depends on an approved component binding and screen layout authority. | BLOCKED | OPEN | Missing catalog and responsive evidence; BLOCKED |

## 8. Text-fit matrix

| Content | Approved font / fallback | Shortest and longest locale strings | Numeric boundaries | Wrapping / scaling policy | Owned bounds | Certainty |
|---|---|---|---|---|---|---|
| All reward-screen copy | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary-action label | BLOCKED pending binding; screen-specific copy remains OPEN | OPEN | Not applicable unless product authority supplies dynamic text | BLOCKED | OPEN | BLOCKED |

## 9. Accessibility and input contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| A11Y-REWARD | Semantic labels, non-color identities, reduced-effects behavior, focus order, hit areas, and Back behavior | No authority supplied | OPEN | OPEN | OPEN |
| A11Y-PRIMARY-ACTION | Component accessibility and input requirements | Requires approved component catalog decision and artifact fingerprint | BLOCKED | BLOCKED | BLOCKED |

## 10. Open decisions and handoff

Next route: game-ui-component-system  
Blocked downstream: game-ui-mockup

- Provide the approved component-catalog decision for `primary-action@2.1.0`, its exact artifact fingerprint, allowed instance inputs, protected properties, required states, approved consumers, and accessibility/input contract.
- Decide whether shadow and highlight values are protected component properties or approved instance inputs; if an override is desired, authorize and version it through the component catalog.
- Provide product authority for reward type, value, copy, dynamic-data format, availability, action callback, destination/effect, persistence boundary, failure/recovery behavior, and Back/dismissal behavior.
- Provide supported viewports, safe-area rules, locales, approved fonts and fallbacks, responsive evidence, and text-fit boundaries.
- After those inputs resolve the component binding, hand only the resolved approved contract to `game-ui-mockup`.
