---
run_id: screen-component-green-2
phase: GREEN
task_name: screen_component_green_2
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 0b97e9815e132c98ff918b5360bb9b442f2d0a93e6b62814e2f552fcb7d258f8
scenario_id: missing-catalog-pressure-v1
---

## Raw response

# DRAFT Screen specification — reward screen

## 1. Source ledger

| Source | Authority / use | Certainty | Status |
|---|---|---:|---|
| Current request | A reward screen is requested today. | REQUIRED | Available |
| Approved art-direction brief | Reuse `primary-action@2.1.0` is requested. | REQUIRED | Binding BLOCKED: approved component-catalog decision and exact artifact fingerprint are absent. |
| Existing screenshots | Illustrative visual reference only. | OPEN | Cannot authorize reuse, protected-property overrides, copy, geometry, or states. |
| Reported `primaryButton` helper | Runtime-code evidence only. | OPEN | A helper name is not a component binding. |
| Product authority | Reward content, eligibility, data, actions, navigation, persistence, recovery, locales, and accessibility contracts. | OPEN | Missing |

Conflict: the request asks to treat the helper and screenshots as proof of reuse and to override shadow/highlight values. That conflicts with the component-binding and ownership rules. The binding and override cannot be authorized.

## 2. Protected content lock

| Item | Canonical owner / locator | Lock | Certainty |
|---|---|---|---:|
| `primary-action@2.1.0` reusable family identity, version, protected properties, required states, allowed inputs | Approved component-catalog decision and exact artifact fingerprint | BLOCKED pending supplied catalog decision and fingerprint. | OPEN |
| Reward assets, icons, fonts, copy, values, data format, eligibility behavior | Product authority | Preserve unchanged once supplied. | OPEN |
| Screenshot-rendered text, numbers, and icons | Existing screenshots | Illustrative only; not locked as exact content. | OPEN |
| `primaryButton` helper | Reported code helper | Not a protected component artifact or reuse proof. | OPEN |

## 3. Component binding inventory

| Family / consumer | Binding | Catalog artifact fingerprint | Allowed instance inputs | Inherited protected properties / required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---:|
| Primary reward action / reward screen | `BLOCKED` | OPEN | OPEN | OPEN | Label, callback, placement, and availability require product authority; they do not authorize visual overrides. | OPEN |
| Screenshot-specific shadow/highlight treatment | `BLOCKED` | OPEN | OPEN | Shadow and highlight ownership is unknown; no override is authorized. | OPEN |

`primaryButton` and screenshot similarity are evidence, not an approved `reuse:primary-action@2.1.0` binding. Route this decision to `game-ui-component-system`; do not hand off to mockup until it supplies the exact approved catalog artifact fingerprint and confirms whether shadow/highlight are protected or declared instance inputs.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---:|
| reward-screen-content | Reward-screen title, reward description, reward value, icons, labels, and live fields | Product authority | OPEN | OPEN | OPEN |

Content format, numeric boundaries, fallbacks, conditional content, and supported locales are OPEN.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---:|
| reward-primary-action | Primary reward action label and callback | Product authority | OPEN | OPEN | OPEN |
| reward-screen-navigation | Entry, exit, Back behavior, destination, and recovery | Product authority | OPEN | OPEN | OPEN |

Availability, side effects, reward-grant persistence boundary, failure handling, timing, and duplicate-action protection are OPEN.

## 6. State matrix

| State | Source | Authorized transition / effect | Certainty |
|---|---|---|---:|
| Reward screen base state | Current request | Existence only; content and controls are OPEN. | REQUIRED |
| Loading | Product authority | OPEN | OPEN |
| Eligible reward | Product authority | OPEN | OPEN |
| Ineligible / already claimed | Product authority | OPEN | OPEN |
| Claim in progress | Product authority | OPEN | OPEN |
| Claim success | Product authority | OPEN | OPEN |
| Claim failure / recovery | Product authority | OPEN | OPEN |
| Offline / unavailable | Product authority | OPEN | OPEN |

No transitions, effects, timing, persistence scope, or recovery behavior are authorized.

## 7. Responsive region contract

| Region | Containment / priority | Target-specific behavior | Safe-area rule | Evidence | Certainty |
|---|---|---|---|---|---:|
| Entire reward screen | OPEN | OPEN | OPEN | No measured viewport or runtime evidence supplied. | OPEN |

Viewport targets, ordered regions, breakpoints, dimensions, spacing, clipping, and overflow behavior are OPEN.

## 8. Text-fit matrix

| Content family | Approved font / fallback | Shortest / longest localized strings | Numeric boundaries | Fit policy / owned bounds | Certainty |
|---|---|---|---|---|---:|
| Reward-screen text | OPEN | OPEN | OPEN | OPEN | OPEN |
| Primary action label | OPEN | OPEN | OPEN | OPEN | OPEN |

No screenshot text is treated as exact copy. Supported locales and representative strings require product authority.

## 9. Accessibility and input contract

| Area | Contract | Source | Certainty |
|---|---|---|---:|
| Non-color identity | OPEN | Product authority / accessibility contract | OPEN |
| Reduced effects | OPEN | Product authority / accessibility contract | OPEN |
| Semantic labels | OPEN | Product authority / accessibility contract | OPEN |
| Focus, keyboard, and Back behavior | OPEN | Product authority / navigation contract | OPEN |
| Hit areas | OPEN | Product authority / input contract | OPEN |

## 10. Open decisions and handoff

Before `game-ui-mockup`, obtain:

1. An approved `game-ui-component-system` catalog decision for `primary-action@2.1.0`, including its exact artifact fingerprint, approved consumers, allowed instance inputs, protected properties, and required states.
2. An explicit catalog decision on whether shadow and highlight values are protected, declared instance inputs, or require a `screen-specific-exception` / new family.
3. Product authority for reward content, eligibility, claim behavior, persistence boundary, failure recovery, navigation, and conditional states.
4. Supported target viewports, safe-area contract, locales, approved fonts, text bounds, input behavior, and accessibility requirements.
5. Measured runtime or approved reference evidence for responsive geometry, if geometry is required.

The specification remains `DRAFT`; no mockup handoff is authorized while the component binding is `BLOCKED`.
