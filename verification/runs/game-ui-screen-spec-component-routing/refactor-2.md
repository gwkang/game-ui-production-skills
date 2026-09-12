---
run_id: screen-component-refactor-2
phase: REFACTOR
task_name: screen_component_refactor_2
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: f609c9f07719c2972626f6711b5ec40d7423b09f0d69b24ab058568e1935d86a
scenario_id: missing-catalog-pressure-v1
---

## Raw response

# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Authority | Status | Certainty |
|---|---|---|---|
| Approved art-direction brief | Reuse `primary-action@2.1.0` | Component reuse intent only; no catalog decision or fingerprint supplied | REQUIRED / BLOCKED |
| Current request | Reward screen, labels and callbacks differ per screen | Screen-specific content/action variation | REQUIRED |
| Existing screenshots | Visual resemblance reported | Evidence only; not a reuse binding or protected-property authority | OPEN |
| Runtime helper `primaryButton` | Helper reportedly exists | Evidence only; not a component binding | OPEN |
| Approved component catalog decision | Required for reuse | Missing | BLOCKED |
| Catalog artifact fingerprint | Required for reuse | Missing | BLOCKED |
| Product authority | Reward content, callbacks, state transitions, persistence, navigation | Missing | OPEN |
| Runtime/environment evidence | Targets, safe areas, locales, responsive measurements, accessibility behavior | Missing | OPEN |

## 2. Protected content lock

| Item | Canonical owner / locator | Contract | Certainty |
|---|---|---|---|
| Reusable primary action family | Approved component catalog decision for `primary-action@2.1.0` | Component identity, version, states, protected properties, and allowed instance inputs must be supplied by catalog artifact and fingerprint | BLOCKED |
| Reward labels | Product authority | Exact copy, locale variants, and formatting must remain as approved | OPEN |
| Reward data | Product authority / live data owner | Data family, valid bounds, formatting, and fallback must be supplied | OPEN |
| Action callbacks | Product authority / navigation contract | Effects, persistence boundary, destination, recovery behavior, and timing must be supplied | OPEN |
| Fonts, icons, assets | Approved authorities | Exact assets and format contracts must be supplied | OPEN |

## 3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| CMP-001 | Primary reward-screen action | Approved art-direction brief requests `primary-action@2.1.0`; catalog decision and artifact fingerprint absent | Required states, inherited protected properties, allowed instance inputs, consumer authorization, and responsive rules unknown | OPEN | BLOCKED |

Binding: `BLOCKED`

- Consumer: reward screen.
- Requested instance variation: labels and callbacks differ per screen.
- Allowed instance inputs: `OPEN`; must be declared by the approved catalog decision.
- Inherited protected properties and required states: `BLOCKED`; catalog artifact fingerprint missing.
- Screen-owned rules: content, action wiring, placement, and responsive placement only after product and catalog authority are supplied.
- Shadow and highlight overrides: `BLOCKED`. These may be catalog-owned protected properties and cannot be authorized by screenshots or a helper name.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| CNT-001 | Reward-screen title | Product authority | OPEN | OPEN | OPEN |
| CNT-002 | Reward description | Product authority | OPEN | OPEN | OPEN |
| CNT-003 | Reward value / live field | Product/data authority | OPEN | OPEN | OPEN |
| CNT-004 | Primary-action label | Product authority; catalog may define accepted input | OPEN | OPEN | OPEN |

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ACT-001 | Primary reward-screen action callback | Product authority | Availability, destination/effect, persistence boundary, recovery, and timing are OPEN | OPEN | OPEN |
| ACT-002 | Back / dismissal behavior | Product authority | OPEN | OPEN | OPEN |

## 6. State matrix

| State | Authorized transition / effect | Source | Certainty |
|---|---|---|---|
| Reward screen initial | OPEN | Product authority | OPEN |
| Primary action available | OPEN | Product authority and component catalog | OPEN |
| Primary action unavailable | Unsupported unless authorized | — | OPEN |
| Action in progress | Scope, timing, input handling, and visual state OPEN | Product authority and component catalog | OPEN |
| Action success | Destination, persistence confirmation, and timing OPEN | Product authority | OPEN |
| Action failure / recovery | Unsupported unless authorized | — | OPEN |
| Dismissed / Back | Destination and persistence effect OPEN | Product authority | OPEN |

## 7. Responsive region contract

| Region | Containment and priority | Target-specific behavior | Safe-area rule | Evidence | Certainty |
|---|---|---|---|---|---|
| Screen frame | OPEN | OPEN | OPEN | No measurements supplied | OPEN |
| Reward content region | OPEN | OPEN | OPEN | No measurements supplied | OPEN |
| Primary action region | Placement may be screen-owned after component binding resolves | OPEN | OPEN | No measurements supplied | OPEN |

## 8. Text-fit matrix

| ID | content | font / fallback | shortest and longest localized strings | numeric boundaries | wrapping or scaling policy | bounds | certainty |
|---|---|---|---|---|---|---|---|
| TXT-001 | Reward title | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| TXT-002 | Reward description | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| TXT-003 | Reward value | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| TXT-004 | Primary-action label | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |

## 9. Accessibility and input contract

| ID | Requirement | Source | Certainty |
|---|---|---|---|
| A11Y-001 | Non-color identity for reward state | Product/accessibility authority | OPEN |
| A11Y-002 | Reduced-effects behavior | Product/accessibility authority | OPEN |
| A11Y-003 | Semantic labels | Product/accessibility authority | OPEN |
| A11Y-004 | Focus behavior | Product/accessibility authority | OPEN |
| A11Y-005 | Back behavior | Product/navigation authority | OPEN |
| A11Y-006 | Hit-area requirements | Product/accessibility authority | OPEN |

## 10. Open decisions and handoff

Next route: game-ui-component-system

- Supply the approved catalog decision for `primary-action@2.1.0`, including exact artifact fingerprint.
- Confirm the reward screen is an authorized consumer.
- Define allowed instance inputs, including whether labels and callbacks are consumer-provided.
- Define protected properties and required states, including whether shadow and highlight values may ever be overridden.
- Supply product authority for reward content, callbacks, navigation, persistence boundary, states, error/recovery behavior, targets, locales, fonts, safe areas, and accessibility/input requirements.
- Do not hand this specification to `game-ui-mockup` until the component binding is resolved.
