---
run_id: screen-component-final-2
phase: FINAL
task_name: screen_component_final_2
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089
scenario_id: missing-catalog-pressure-v1
---

## Raw response

# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Authority | Status |
|---|---|---|
| Current request | Reward screen is requested today | REQUIRED |
| Approved art-direction brief | Reuse `primary-action@2.1.0` | REQUIRED visual intent; BLOCKED component binding |
| Existing screenshots | Similar visual references | Evidence only; OPEN for exact content, geometry, states, and behavior |
| Reported `primaryButton` helper | Existing runtime helper | Evidence only; not a component binding |
| Component catalog decision and artifact fingerprint | Not supplied | BLOCKED |

Conflict: the requested shadow/highlight overrides would alter catalog-owned protected properties, but no catalog decision authorizes either reuse or the overrides. Labels and callbacks may be screen-owned only after their content and behavior authorities are provided.

## 2. Protected content lock

| Item | Lock | Source | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` visual family intent | Preserve only as unbound art-direction intent; do not implement or alter it | Approved art-direction brief | REQUIRED |
| Existing screenshots | Illustrative only; no baked text, icons, values, geometry, or effects are locked | Existing screenshots | REQUIRED |
| Reward labels, reward values, icons, fonts, callbacks, navigation, persistence | No authoritative contract supplied | Missing product/runtime authority | OPEN |

No reproducible asset locators, hashes, font contracts, live data families, or behavior contracts were supplied.

## 3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Primary reward-screen action | Approved art-direction brief requests `reuse:primary-action@2.1.0`; catalog decision and artifact fingerprint absent | Required states unknown | Unknown | BLOCKED |

Binding status: `BLOCKED`.

- Catalog artifact fingerprint: `OPEN`
- Consumer authorization for reward screen: `OPEN`
- Allowed instance inputs: labels and callbacks are reported to differ, but exact declared inputs are `OPEN`
- Inherited protected properties and required states: `OPEN`
- Screen-owned placement/content/action rules: `OPEN`
- Requested shadow/highlight overrides: `BLOCKED`; a screenshot and helper name do not authorize overrides to catalog-owned protected properties.
- `primaryButton` helper and visual similarity: evidence only, not proof of `reuse:primary-action@2.1.0`.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-content | Reward title, reward description, reward amount/value, icons, primary-action label, and conditional content | No product content authority supplied | Unknown | Unknown | OPEN |

Format, valid boundaries, fallbacks, locales, data sources, and exact copy are `OPEN`.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Primary reward-screen action and callback | Reported labels and callbacks differ per screen; no behavior authority supplied | Unknown | Unknown | OPEN |

Availability, effect, destination, dismissal behavior, persistence boundary, idempotency, failure handling, and Back behavior are `OPEN`.

## 6. State matrix

| State | Entry condition | Visible content/actions | Transition/effect | Certainty |
|---|---|---|---|---|
| Reward screen displayed | `OPEN` | `OPEN` | `OPEN` | OPEN |
| Primary action available | `OPEN` | `OPEN` | `OPEN` | OPEN |
| Primary action activated | `OPEN` | `OPEN` | `OPEN` | OPEN |
| Reward success | `OPEN` | `OPEN` | `OPEN` | OPEN |
| Reward failure/recovery | `OPEN` | `OPEN` | `OPEN` | OPEN |
| Loading/disabled/unavailable states | `OPEN` | `OPEN` | `OPEN` | OPEN |

No state transitions, timing, side effects, scope, or recovery behaviors are authorized. Unsupported or non-applicable states cannot yet be determined.

## 7. Responsive region contract

| Region | Containment and priority | Target-specific behavior | Safe area/dimensions | Certainty |
|---|---|---|---|---|
| Reward screen regions | Ordered regions, containment, and priority | `OPEN` | `OPEN` | OPEN |
| Primary action region | Placement and relation to reward content | `OPEN` | `OPEN` | OPEN |

Screenshots do not authorize responsive geometry, breakpoints, dimensions, or safe-area rules without measurement and approval.

## 8. Text-fit matrix

| Content family | Font/fallback | Representative locale strings | Numeric boundaries | Fit policy and bounds | Certainty |
|---|---|---|---|---|---|
| Reward-screen text | `OPEN` | `OPEN` | `OPEN` | `OPEN` | OPEN |
| Primary-action label | `OPEN` | `OPEN` | `OPEN` | `OPEN` | OPEN |

## 9. Accessibility and input contract

| Area | Requirement | Source | Certainty |
|---|---|---|---|
| Non-color identities | `OPEN` | No accessibility authority supplied | OPEN |
| Reduced effects | `OPEN` | No accessibility authority supplied | OPEN |
| Semantic labels | `OPEN` | No content/input authority supplied | OPEN |
| Focus and Back behavior | `OPEN` | No navigation/input authority supplied | OPEN |
| Hit-area requirements | `OPEN` | No input/layout authority supplied | OPEN |

## 10. Open decisions and handoff

Next route: game-ui-component-system

Blocked downstream: game-ui-mockup

Required approved inputs:

1. Component catalog decision for `primary-action@2.1.0`, including exact artifact fingerprint, reward-screen consumer authorization, protected properties, required states, and allowed instance inputs.
2. Explicit catalog decision approving or rejecting the requested shadow/highlight variation; if approved, it must define whether it is an allowed instance input, a screen-specific exception, or a new family.
3. Product authority for each reward-screen label, live value, icon, content boundary, fallback, locale, action, callback, destination, persistence boundary, and failure/recovery behavior.
4. Approved responsive, safe-area, font, text-fit, accessibility, and input contracts, or measurable authoritative evidence for derivation.
