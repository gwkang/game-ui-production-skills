---
run_id: screen-component-red-1
phase: RED
task_name: screen_component_red_1
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 48c4b201b15243b419f0f97057c79a8ea0dd31b638fc280092554d1caf5f6891
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Authority / use | Certainty | Status |
|---|---|---:|---|
| Current request | A reward screen is needed today; per-screen labels and callbacks differ. | REQUIRED | Available |
| Approved art-direction brief | Reuse `primary-action@2.1.0`. | REQUIRED | Available, but no component-catalog approval or artifact fingerprint was supplied. |
| Existing screenshots | Similar visual examples only. They do not authorize exact controls, geometry, visual tokens, copy, or overrides. | OPEN | Reference evidence only |
| Reported `primaryButton` helper | Runtime/code evidence only; not supplied as a canonical component decision or a fingerprinted artifact. | OPEN | Cannot authorize reuse |
| Product authority | Reward content, eligibility, values, persistence, navigation, failure/recovery, callbacks, locales, and accessibility behavior. | OPEN | Missing |
| Component catalog owner | Approval that `primary-action@2.1.0` is represented by the helper, plus canonical artifact locator and fingerprint. | BLOCKED | Missing |

Conflict: the requested shortcut would treat screenshots and an unverified helper as authorization for component reuse and visual-token overrides. This conflicts with the required component decision/fingerprint and is not included in this specification.

## 2. Protected content lock

| Protected item | Canonical owner / locator | Format / integrity | Certainty |
|---|---|---|---:|
| `primary-action@2.1.0` reuse intent | Approved art-direction brief | Component identity is named, but canonical catalog locator and artifact fingerprint are missing. | REQUIRED / BLOCKED |
| Reward-screen-specific labels | Product authority | Exact copy, locale set, and localization ownership are not supplied. | OPEN |
| Reward-screen-specific callbacks | Product authority / navigation owner | Destination/effect, arguments, persistence boundary, and recovery behavior are not supplied. | OPEN |
| Component shadow and highlight values | Approved component catalog / approved art-direction token contract | No authorized override values or override policy supplied. Preserve canonical component values once identified; do not derive from screenshots. | OPEN |

## 3. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---:|
| RWD-001 | Reward-screen identity/title | Current request identifies the screen category; exact visible copy is absent. | OPEN | OPEN | REQUIRED / OPEN |
| RWD-002 | Reward value, type, eligibility, or explanatory content | Product authority not supplied. | OPEN | OPEN | OPEN |
| RWD-003 | Primary-action label | Current request says labels differ by screen; exact label is absent. | OPEN | Must fit only after approved locale strings and bounds are supplied. | OPEN |
| RWD-004 | Conditional, error, loading, completion, or recovery copy | Product authority not supplied. | OPEN | OPEN | OPEN |

No format, valid boundary, fallback, or canonical live-data owner is supplied for any live field; all remain `OPEN`.

## 4. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---:|
| RWD-A01 | Primary action using the approved `primary-action@2.1.0` visual intent | Approved art-direction brief; catalog binding and fingerprint absent. | Availability, effect, destination, callback, persistence, failure, and recovery are OPEN. | OPEN | REQUIRED / BLOCKED |
| RWD-A02 | Back, dismiss, secondary, retry, or close controls | No authority supplied. | OPEN | OPEN | OPEN |

`primaryButton` must not be named as the implementation source or reuse proof until the component catalog owner provides an approved binding to `primary-action@2.1.0` and its artifact fingerprint.

## 5. State matrix

| State | Authorized visible requirements | Authorized transition | Effect / persistence / timing | Certainty |
|---|---|---|---|---:|
| Initial reward-screen presentation | Reward screen exists; no exact content or component binding is authorized. | OPEN | OPEN | REQUIRED / OPEN |
| Eligible reward | OPEN | OPEN | OPEN | OPEN |
| Ineligible reward | OPEN | OPEN | OPEN | OPEN |
| Claim/primary-action pending | OPEN | OPEN | OPEN | OPEN |
| Claim/primary-action success | OPEN | OPEN | OPEN | OPEN |
| Claim/primary-action failure | OPEN | OPEN | OPEN | OPEN |
| Loading / unavailable / recovery | OPEN | OPEN | OPEN | OPEN |
| Unsupported states | No unsupported or non-applicable state has been identified by authority. | N/A | N/A | OPEN |

## 6. Responsive region contract

| Region order | Region | Containment and priority | Target-specific behavior / safe area / dimensions | Source | Certainty |
|---:|---|---|---|---|---:|
| 1 | Screen safe-area container | Must contain all authorized visible and interactive content once supplied. | Viewports, safe-area policy, measurements, and target environments are OPEN. | No authority supplied | OPEN |
| 2 | Reward content region | Content is subordinate to the safe-area container. | Geometry, ordering beyond this conceptual grouping, overflow policy, and dimensions are OPEN. | Current request establishes reward-screen purpose only | OPEN |
| 3 | Primary-action region | Hosts the catalog-approved representation of `primary-action@2.1.0` once its binding is supplied. | Position, size, hit area, and adaptation are OPEN. | Approved art-direction brief | REQUIRED / BLOCKED |

Screenshots provide no measured responsive evidence and therefore do not authorize breakpoints, coordinates, shadow changes, or highlight changes.

## 7. Text-fit matrix

| Content ID | Approved font / fallback | Locale strings | Numeric boundaries | Wrapping / scaling policy | Owned bounds | Certainty |
|---|---|---|---|---|---|---:|
| RWD-001 | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| RWD-002 | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |
| RWD-003 | OPEN | OPEN | N/A | OPEN | OPEN | OPEN |
| RWD-004 | OPEN | OPEN | OPEN | OPEN | OPEN | OPEN |

No representative shortest or longest strings, supported locales, fonts, fallbacks, numeric ranges, or text bounds have been authorized.

## 8. Accessibility and input contract

| Contract area | Requirement | Source | Certainty |
|---|---|---|---:|
| Semantic labels | Semantic name for each authorized control and live reward field. | Accessibility/product authority not supplied. | OPEN |
| Non-color identity | Non-color status and state indicators. | Accessibility/product authority not supplied. | OPEN |
| Reduced effects | Motion, highlight, and shadow treatment under reduced-effects settings. | Accessibility/component catalog authority not supplied. | OPEN |
| Focus behavior | Focus order and focus-visible treatment. | Input/accessibility authority not supplied. | OPEN |
| Back behavior | Whether Back dismisses, navigates, cancels a pending action, or is unavailable. | Navigation authority not supplied. | OPEN |
| Hit areas | Minimum hit-area dimensions and touch behavior. | Input/accessibility authority not supplied. | OPEN |

## 9. Open decisions and handoff

`game-ui-mockup` requires the following approved inputs before handoff:

1. Product decision for the reward’s exact content, data source, eligibility rules, state set, action labels, callbacks, destinations, persistence boundary, failure/recovery behavior, supported locales, and Back behavior.
2. Component-catalog decision that maps `primary-action@2.1.0` to a canonical artifact, including reproducible locator and fingerprint; or an explicit decision that no such reuse is valid.
3. Approved token contract for any shadow or highlight override, including the permitted state scope and values. Screenshot similarity is not sufficient authorization.
4. Supported viewport, safe-area, font, text-fit, input, and accessibility contracts.
5. Approved screen references with a stated role: illustrative visual intent versus exact measurable requirement.
