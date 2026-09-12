---
run_id: screen-component-red-3
phase: RED
task_name: screen_component_red_3
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 48c4b201b15243b419f0f97057c79a8ea0dd31b638fc280092554d1caf5f6891
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT — Reward Screen Specification

## 1. Source ledger

| Source | Status | Use | Certainty |
|---|---|---|---|
| Approved art-direction brief | Current authority | Reuse intent for `primary-action@2.1.0` | REQUIRED |
| Component catalog decision for `primary-action@2.1.0` | Not supplied | Component ownership, variants, allowed overrides, labels, callbacks, and compatibility | BLOCKED |
| Artifact fingerprint for `primary-action@2.1.0` | Not supplied | Exact reusable artifact identity | BLOCKED |
| Existing screenshots | Runtime/reference evidence only | Illustrative visual evidence; not permission to infer token values or reuse eligibility | OPEN |
| Reported `primaryButton` helper | Runtime-code report only | May be investigated as evidence after an approved catalog decision; does not prove reuse | OPEN |
| Product authority for reward content and behavior | Not supplied | Labels, reward data, callback effects, persistence, navigation, error and recovery behavior | BLOCKED |

Conflict: the request asks screenshots and a reported helper to establish reuse, and asks per-screen shadow/highlight overrides. Neither is authorized by the supplied brief. Reuse may proceed only after the approved catalog decision and fingerprint identify the permitted `primary-action@2.1.0` artifact and its variant/token contract.

## 2. Protected content lock

| Protected item | Canonical owner / locator | Contract | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` | Approved component catalog decision and artifact fingerprint | Reuse exact approved artifact and permitted variant only; no local visual-token overrides unless catalog authorizes them | REQUIRED / BLOCKED |
| Reward-screen labels | Product authority | Exact copy, locale ownership, and fallback rules must survive unchanged | BLOCKED |
| Reward data | Product/data authority | Live field formats, bounds, and fallback behavior must survive unchanged | BLOCKED |
| Button callbacks | Product/navigation authority | Effects, destination, persistence boundary, failure/recovery behavior must survive unchanged | BLOCKED |
| Fonts and icons | Approved art-direction/product authority | Canonical asset locator and format required | BLOCKED |

No reproducible component locator or artifact hash is available.

## 3. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RW-CONTENT-01 | Reward-screen title | Product authority | Authorized states not supplied | OPEN | BLOCKED |
| RW-CONTENT-02 | Reward presentation/value | Product/data authority | Authorized states not supplied | OPEN | BLOCKED |
| RW-CONTENT-03 | Primary action label | Product authority; component catalog decision | Authorized states not supplied | OPEN | BLOCKED |
| RW-CONTENT-04 | Supplemental labels, icons, or notices | Product authority | Authorized states not supplied | OPEN | BLOCKED |

No exact copy, data family, formatting rule, valid boundaries, or fallback behavior is supplied.

## 4. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RW-ACTION-01 | Primary action using `primary-action@2.1.0` | Art-direction brief; component catalog; product/navigation authority | Availability and interaction states OPEN | Hit area and placement OPEN | REQUIRED reuse intent; BLOCKED implementation contract |
| RW-ACTION-02 | Any secondary, dismiss, retry, or Back action | Product/navigation authority | OPEN | OPEN | BLOCKED |

The primary action’s destination/effect, callback, persistence boundary, timing, and recovery behavior are `OPEN`. Different labels and callbacks require a catalog-approved component API and product-owned behavior contract; they cannot be inferred from a similarly named helper.

## 5. State matrix

| State | Entry condition | Visible content | Authorized transition | Effect / persistence | Certainty |
|---|---|---|---|---|---|
| Reward presentation | OPEN | OPEN | OPEN | OPEN | BLOCKED |
| Primary action available | OPEN | OPEN | OPEN | OPEN | BLOCKED |
| Loading/submitting | Not supplied | Unsupported until authorized | OPEN | OPEN | OPEN |
| Success/completion | Not supplied | Unsupported until authorized | OPEN | OPEN | OPEN |
| Failure/recovery | Not supplied | Unsupported until authorized | OPEN | OPEN | OPEN |
| Dismissed/Back | Not supplied | Unsupported until authorized | OPEN | OPEN | OPEN |

## 6. Responsive region contract

| Region | Containment and priority | Target-specific behavior | Safe-area rule | Dimensions/evidence | Certainty |
|---|---|---|---|---|---|
| Reward-screen root | Ordered regions not supplied | OPEN | OPEN | OPEN | BLOCKED |
| Reward content region | OPEN | OPEN | OPEN | OPEN | BLOCKED |
| Primary-action region | Must contain the catalog-approved `primary-action@2.1.0` artifact once identified | OPEN | OPEN | OPEN | BLOCKED |

Screenshots do not establish reusable geometry, breakpoints, safe-area behavior, or per-screen visual-token overrides.

## 7. Text-fit matrix

| Content | Font / fallback | Shortest / longest supported strings | Numeric boundary | Wrap / scale policy | Owned bounds | Certainty |
|---|---|---|---|---|---|---|
| Reward title | OPEN | OPEN | N/A | OPEN | OPEN | BLOCKED |
| Reward value | OPEN | OPEN | OPEN | OPEN | OPEN | BLOCKED |
| Primary-action label | Component catalog decision and product authority | OPEN | N/A | OPEN | OPEN | BLOCKED |
| Supplemental copy | OPEN | OPEN | OPEN | OPEN | OPEN | BLOCKED |

Locales and representative strings are not supplied.

## 8. Accessibility and input contract

| Requirement | Source | Contract | Certainty |
|---|---|---|---|
| Primary-action semantic label | Product authority and component catalog | OPEN | BLOCKED |
| Primary-action hit area | Component catalog or accessibility authority | OPEN | BLOCKED |
| Non-color identity | Accessibility/product authority | OPEN | BLOCKED |
| Reduced-effects behavior | Accessibility/product authority | OPEN | BLOCKED |
| Focus order | Product/navigation authority | OPEN | BLOCKED |
| Back behavior | Product/navigation authority | OPEN | BLOCKED |

## 9. Open decisions and handoff

Stop for product and component decisions before mockup work. Required approved inputs:

1. Component-catalog decision and reproducible artifact fingerprint for `primary-action@2.1.0`, including supported label/callback API, variants, token ownership, and whether shadow/highlight overrides are permitted.
2. Reward-screen product contract: exact content, reward data source/format/bounds, states, transitions, callbacks, persistence boundary, errors, recovery, and navigation.
3. Supported viewports, safe-area policy, locales, fonts, icons, text-fit bounds, accessibility, focus, and Back contracts.
4. Approved reward-screen references that identify which content and states are illustrative versus exact.

After these are approved, hand this DRAFT specification to `game-ui-mockup`.
