---
run_id: screen-component-refactor-4
phase: REFACTOR
task_name: screen_component_refactor_4
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: f609c9f07719c2972626f6711b5ec40d7423b09f0d69b24ab058568e1935d86a
scenario_id: missing-catalog-pressure-v1
---

## Raw response

DRAFT Screen specification

1. Source ledger

| Authority / input | Status | Certainty |
|---|---|---|
| Approved art-direction brief: reuse `primary-action@2.1.0` | Reuse intent supplied; catalog decision and artifact fingerprint absent | REQUIRED / BLOCKED |
| Current request: reward screen today | Screen target only; content, behavior, states, layout, and supported environments absent | REQUIRED / OPEN |
| Existing screenshots | Illustrative visual evidence only; not authority for reusable binding or protected-property overrides | REQUIRED |
| Reported `primaryButton` helper | Runtime-code evidence only; not a reusable-family binding | REQUIRED |
| Per-screen label and callback differences | Instance variation reported, but allowed instance-input contract absent | REQUIRED / OPEN |
| Requested shadow and highlight overrides | Not authorized; catalog-owned protected-property contract absent | BLOCKED |

2. Protected content lock

| Item | Canonical owner / locator | Lock | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` reusable family | Approved component catalog decision and exact artifact fingerprint | Identity, version, protected properties, required states, allowed instance inputs | BLOCKED |
| Reward-screen labels | Product authority | Exact copy, locale coverage, formatting, fallback | OPEN |
| Reward values / data | Product/data authority | Data family, valid bounds, formatting, fallback | OPEN |
| Reward-screen actions and callbacks | Product/navigation authority | Effects, persistence boundary, destination, recovery | OPEN |
| Fonts, icons, assets | Approved visual/product authority | Exact artifact, license/provenance, fallback, format | OPEN |
| Screenshot shadow/highlight appearance | Screenshot only | Illustrative; not a protected or overridable requirement | REQUIRED |

No reproducible approved artifact locators or hashes were supplied.

3. Component binding inventory

| Family / consumer | Binding | Catalog artifact fingerprint | Allowed instance inputs | Inherited protected properties and required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---|
| Primary action / reward screen | BLOCKED | BLOCKED | OPEN | BLOCKED | Label, callback, and placement may be screen-owned only if the catalog explicitly declares them as allowed inputs | BLOCKED |

`primaryButton` and screenshot similarity do not establish `reuse:primary-action@2.1.0`. Shadow and highlight values must not be overridden unless the approved component catalog explicitly permits those inputs or approves a screen-specific exception.

4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-content | Reward-screen visible content | Current request identifies only the screen; product content authority absent | OPEN | OPEN | OPEN |
| primary-action-label | Primary-action label | Reported per-screen variation; exact text and allowed input contract absent | OPEN | OPEN | OPEN |
| reward-value | Reward value / value presentation | Product/data authority absent | OPEN | OPEN | OPEN |

5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| primary-action | Primary action callback | Reported per-screen callback variation; action effect, availability, persistence boundary, destination, and recovery absent | OPEN | OPEN | OPEN |
| reward-screen-navigation | Screen navigation / Back behavior | Product/navigation authority absent | OPEN | OPEN | OPEN |

6. State matrix

| State | Source | Authorized transition / effect | Certainty |
|---|---|---|---|
| Default reward screen | Current request identifies a reward screen only | Entry condition, visible content, and exit behavior are OPEN | OPEN |
| Primary-action available | No authority supplied | Availability rule, action effect, persistence boundary, timing, and recovery are OPEN | OPEN |
| Primary-action unavailable / loading / failure / success | No authority supplied | Explicitly unsupported until product authority authorizes the state and transition | OPEN |
| Reward-claim / reward-grant state | No authority supplied | Scope, side effects, persistence, timing, and recovery are OPEN | OPEN |

7. Responsive region contract

| Region | Containment and priority | Target-specific behavior / safe area | Evidence | Certainty |
|---|---|---|---|---|
| Reward-screen regions | OPEN | Supported targets, viewports, safe areas, geometry, ordering, and overflow rules are OPEN | Screenshots are illustrative only | OPEN |
| Primary-action region | OPEN | Placement and size rules are OPEN; must use catalog-authorized component constraints after binding resolves | No measured or approved dimensions supplied | OPEN |

8. Text-fit matrix

| Content | Approved font / fallback | Representative locale strings and numeric bounds | Wrap / scale policy | Owned bounds | Certainty |
|---|---|---|---|---|---|
| Reward-screen labels | OPEN | Supported locales, shortest/longest strings, and fallback absent | OPEN | OPEN | OPEN |
| Primary-action label | OPEN | Exact label and supported locale variants absent | OPEN | OPEN | OPEN |
| Reward value | OPEN | Data format and numeric boundaries absent | OPEN | OPEN | OPEN |

9. Accessibility and input contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| Reward-screen accessibility | Product/accessibility authority absent | OPEN | OPEN | OPEN |
| Primary-action semantic label, focus, hit area, non-color identity, reduced-effects behavior | Product/accessibility authority and component catalog absent | OPEN | OPEN | OPEN |
| Back behavior | Product/navigation authority absent | OPEN | OPEN | OPEN |

10. Open decisions and handoff

Next route: game-ui-component-system

- Provide the approved component-catalog decision for `primary-action@2.1.0`.
- Provide the exact approved catalog artifact fingerprint.
- Confirm whether the reward screen is an authorized consumer.
- Define allowed instance inputs, including whether label and callback variations are permitted.
- Define inherited protected properties and required states.
- Decide whether shadow and highlight are protected properties, declared instance inputs, or require a screen-specific exception; screenshots and the `primaryButton` helper cannot authorize the override.
- After binding resolves, provide product authority for reward content, reward data/format boundaries, actions, navigation, persistence, authorized states/transitions, supported viewports/safe areas/locales, fonts/assets, and accessibility/input behavior.
