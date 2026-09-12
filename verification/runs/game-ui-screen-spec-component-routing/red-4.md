---
run_id: screen-component-red-4
phase: RED
task_name: screen_component_red_4
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 48c4b201b15243b419f0f97057c79a8ea0dd31b638fc280092554d1caf5f6891
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT — Reward Screen Specification

## 1. Source ledger

| Source | Status | Scope | Certainty |
|---|---|---|---|
| Approved art-direction brief | Current authority | Reuse intent for `primary-action@2.1.0` | REQUIRED |
| Current request | Current authority | Reward screen requested; labels and callbacks vary by screen | REQUIRED |
| Approved component catalog decision | Not supplied | Whether `primary-action@2.1.0` is approved, canonical, and reusable | BLOCKED |
| Component artifact fingerprint | Not supplied | Exact reusable artifact identity and version integrity | BLOCKED |
| Existing screenshots | Evidence only | Illustrative visual reference; no exact geometry, tokens, or component reuse authority | OPEN |
| Reported `primaryButton` helper | Runtime evidence only; locator not supplied | Possible implementation evidence, not component approval | OPEN |
| Shadow/highlight overrides | Requested but unsupported | No approved token/exception authority supplied | OPEN |

Conflict: the request asks screenshots and the reported helper to prove reuse and authorize shadow/highlight overrides. They cannot establish component approval, artifact identity, or visual-token exceptions. The approved brief’s reuse intent remains protected, but implementation/mockup reuse is `BLOCKED` until the catalog decision and artifact fingerprint are supplied.

## 2. Protected content lock

| Protected item | Canonical owner / locator | Lock | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` reuse intent | Approved art-direction brief | Preserve the stated component version intent; do not substitute `primaryButton` or screenshot-derived styling | REQUIRED |
| Reward-screen labels | Product authority not supplied | Do not invent or bake copy | OPEN |
| Reward data and values | Product/data authority not supplied | Do not invent reward type, amount, currency, or formatting | OPEN |
| Callbacks and persistence behavior | Product/platform authority not supplied | Do not infer from helper names or screenshots | OPEN |
| Fonts, icons, and asset families | Approved source not supplied | No selection or replacement authorized | OPEN |
| Exact component artifact | Catalog locator and fingerprint not supplied | Reuse cannot be verified or handed off | BLOCKED |

## 3. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| RWD-001 | Reward-screen title | Product authority not supplied | OPEN | OPEN | OPEN |
| RWD-002 | Reward description | Product authority not supplied | OPEN | OPEN | OPEN |
| RWD-003 | Reward value / item field | Product/data authority not supplied | OPEN | OPEN | OPEN |
| RWD-004 | Primary action label | Product authority not supplied; labels vary by screen | OPEN | OPEN | OPEN |
| RWD-005 | Any secondary, status, error, or recovery copy | Product authority not supplied | OPEN | OPEN | OPEN |

## 4. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ACT-001 | Primary action using `primary-action@2.1.0` | Approved art-direction brief specifies reuse intent; product callback/destination absent | OPEN | OPEN | REQUIRED for reuse intent; OPEN for behavior |
| ACT-002 | Any secondary action | Product authority not supplied | OPEN | OPEN | OPEN |
| NAV-001 | Completion destination | Product authority not supplied | OPEN | OPEN | OPEN |
| PERSIST-001 | Reward-claim persistence boundary | Product/platform authority not supplied | OPEN | N/A | OPEN |

`primaryButton` is not an approved substitute for `primary-action@2.1.0`. Its existence, API, callbacks, and state behavior remain `OPEN`.

## 5. State matrix

| State | Entry | Visible content | Authorized transition | Effect / persistence / timing | Certainty |
|---|---|---|---|---|---|
| Reward screen shown | OPEN | RWD-001 through RWD-004, if product authority confirms them | OPEN | OPEN | OPEN |
| Primary action available | OPEN | ACT-001 | OPEN | OPEN | OPEN |
| Primary action unavailable | OPEN | OPEN | OPEN | OPEN | OPEN |
| Claim/submission in progress | OPEN | OPEN | OPEN | OPEN | OPEN |
| Claim/submission success | OPEN | OPEN | OPEN | OPEN | OPEN |
| Claim/submission failure/recovery | OPEN | OPEN | OPEN | OPEN | OPEN |
| Unsupported states | No authority supplied | N/A | N/A | N/A | OPEN |

## 6. Responsive region contract

| Region | Containment and priority | Target-specific behavior | Safe area / dimensions | Evidence | Certainty |
|---|---|---|---|---|---|
| Screen root | OPEN | OPEN | OPEN | No supported viewport or safe-area authority supplied | OPEN |
| Reward content region | OPEN | OPEN | OPEN | Screenshots are illustrative only | OPEN |
| Primary-action region | Contains approved reuse intent only | OPEN | OPEN | Exact artifact, measurements, and catalog contract are blocked | BLOCKED |
| Secondary/status region | OPEN | OPEN | OPEN | No product state/content authority supplied | OPEN |

No screenshot-derived shadow, highlight, coordinates, spacing, breakpoint, or dimension is authorized.

## 7. Text-fit matrix

| Field | Approved font / fallback | Shortest and longest supported strings | Numeric boundaries | Wrapping/scaling policy | Owned bounds | Certainty |
|---|---|---|---|---|---|---|
| Title | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| Description | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| Reward value | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary-action label | OPEN | OPEN | N/A | OPEN | Component artifact contract blocked | BLOCKED |
| Status/error/recovery text | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |

## 8. Accessibility and input contract

| Area | Requirement | Source | Certainty |
|---|---|---|---|
| Primary-action semantic label | OPEN | No accessibility authority supplied | OPEN |
| Non-color identity for action state | OPEN | No accessibility authority supplied | OPEN |
| Reduced-effects behavior | OPEN | No accessibility authority supplied | OPEN |
| Focus order and focus visibility | OPEN | No input/accessibility authority supplied | OPEN |
| Back behavior | OPEN | No navigation authority supplied | OPEN |
| Hit area | OPEN | No target/input authority supplied | OPEN |

## 9. Open decisions and handoff

The specification remains `DRAFT`; no mockup is produced.

Required approved inputs for `game-ui-mockup`:

1. Approved component-catalog decision confirming `primary-action@2.1.0` is the canonical reusable component.
2. Reproducible component locator and artifact fingerprint for that exact version.
3. Approved decision on whether any reward-screen exception may override the component’s shadow or highlight values, including the token values and scope.
4. Product authority for reward types, labels, dynamic data format and boundaries, actions, callbacks, navigation, persistence, success/failure/recovery states, and timing.
5. Supported viewports, safe-area contract, locales, font/fallback contract, text-fit bounds, and accessibility/input requirements.
6. Any approved screen references that make exact visual content or layout authoritative.

Without items 1–3, handoff for a mockup that reuses or visually modifies `primary-action@2.1.0` is blocked.
