---
run_id: screen-component-green-5
phase: GREEN
task_name: screen_component_green_5
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 0b97e9815e132c98ff918b5360bb9b442f2d0a93e6b62814e2f552fcb7d258f8
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Status | Certainty |
|---|---|---|
| Approved art-direction brief: reuse `primary-action@2.1.0` | Current visual direction | REQUIRED |
| Component catalog decision for `primary-action@2.1.0` | Not supplied | BLOCKED |
| Catalog artifact fingerprint | Not supplied | BLOCKED |
| Existing screenshots | Illustrative evidence only; no exact visual properties authorized | OPEN |
| Reported `primaryButton` helper | Runtime evidence only; not a component binding | OPEN |
| Labels and callbacks differ by screen | Product behavior/content authority not supplied | OPEN |

Conflict: the requested shadow and highlight overrides would alter catalog-owned protected properties unless the approved catalog explicitly declares them as instance inputs. The catalog decision and fingerprint are absent, so this cannot be authorized.

## 2. Protected content lock

| Item | Owner/source | Contract | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` family identity and version | Approved art-direction brief | Reuse requested, pending exact catalog binding | REQUIRED |
| Component artifact fingerprint | Component catalog | Required for reuse verification | BLOCKED |
| Shadow and highlight properties | Component catalog | Protected or configurable only as declared by catalog | OPEN |
| Reward-screen labels | Product authority | Exact copy, locales, and text format required | OPEN |
| Reward data fields | Product authority | Canonical source, format, bounds, fallback required | OPEN |
| Reward callbacks | Product authority | Effect, persistence, navigation, failure/recovery required | OPEN |
| Fonts, icons, and assets | Product/art-direction authority | Exact locators and licenses/fingerprints required | OPEN |

## 3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Primary reward action | Approved art-direction brief | Required component states not supplied | Placement and target behavior not supplied | BLOCKED |

Binding: `BLOCKED`.

Required before a binding can be recorded as `reuse:primary-action@2.1.0`:

- Approved component catalog decision.
- Exact approved artifact fingerprint.
- Declared consumers and allowed instance inputs.
- Inherited protected properties and required states.
- Explicit determination whether shadow and highlight are catalog-configurable instance inputs.

The `primaryButton` helper and screenshot similarity do not establish reuse. Screen-specific labels, callbacks, and placement may be screen-owned only after the component binding is approved; they do not authorize overrides to protected visual properties.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-title | Reward screen title | Product authority not supplied | OPEN | OPEN | OPEN |
| reward-value | Reward amount or item | Product authority not supplied | OPEN | OPEN | OPEN |
| reward-description | Reward explanatory copy | Product authority not supplied | OPEN | OPEN | OPEN |
| reward-primary-action-label | Primary action label | Product authority not supplied | OPEN | OPEN | OPEN |

No exact labels, live fields, data formats, valid boundaries, or fallbacks are authorized.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Claim/continue action | Product authority not supplied | Availability, effect, persistence, destination, failures, recovery OPEN | OPEN | OPEN |
| reward-back | Back behavior | Product authority not supplied | OPEN | OPEN | OPEN |

## 6. State matrix

| State | Source | Authorized transition/effect | Certainty |
|---|---|---|---|
| Initial reward presentation | Product authority not supplied | OPEN | OPEN |
| Primary action available | Product authority not supplied | OPEN | OPEN |
| Primary action unavailable | Product authority not supplied | OPEN | OPEN |
| Reward persistence pending | Product authority not supplied | OPEN | OPEN |
| Reward persistence succeeded | Product authority not supplied | OPEN | OPEN |
| Reward persistence failed | Product authority not supplied | OPEN | OPEN |
| Loading, retry, duplicate-claim, timeout, and recovery | Product authority not supplied | Unsupported or non-applicable status not authorized | OPEN |

## 7. Responsive region contract

| Region | Containment and priority | Target behavior | Safe area/dimensions | Certainty |
|---|---|---|---|---|
| Reward screen root | Ordered region ownership not supplied | OPEN | OPEN | OPEN |
| Reward content region | OPEN | OPEN | OPEN | OPEN |
| Primary action region | OPEN | OPEN | OPEN | OPEN |

No screenshots, coordinates, platform conventions, or assumed dimensions are treated as requirements.

## 8. Text-fit matrix

| Field | Font/fallback | Shortest/longest locale strings | Numeric bounds | Wrap/scale policy | Certainty |
|---|---|---|---|---|---|
| All reward-screen text | Not supplied | Not supplied | Not supplied | Not supplied | OPEN |

## 9. Accessibility and input contract

| Requirement | Source | Contract | Certainty |
|---|---|---|---|
| Non-color identity | Not supplied | OPEN | OPEN |
| Reduced-effects behavior | Not supplied | OPEN | OPEN |
| Semantic labels | Not supplied | OPEN | OPEN |
| Focus behavior | Not supplied | OPEN | OPEN |
| Back behavior | Not supplied | OPEN | OPEN |
| Hit-area requirements | Not supplied | OPEN | OPEN |

## 10. Open decisions and handoff

This specification remains `DRAFT` and is blocked from handoff to `game-ui-mockup`.

Route first to `game-ui-component-system` with:

1. The approved catalog decision for `primary-action@2.1.0`.
2. Its exact artifact fingerprint.
3. Protected properties, required states, permitted consumers, and allowed instance inputs.
4. An explicit ruling on whether shadow and highlight values are configurable; if they are not, either preserve them or approve a `screen-specific-exception`/new family.
5. Product authority for reward copy, data, callbacks, persistence boundary, navigation, recovery, locales, target environments, safe areas, text-fit bounds, and accessibility/input behavior.

After these inputs are approved and the binding can be verified, hand only the resolved contract to `game-ui-mockup`.
