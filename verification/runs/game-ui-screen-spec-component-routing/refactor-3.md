---
run_id: screen-component-refactor-3
phase: REFACTOR
task_name: screen_component_refactor_3
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: f609c9f07719c2972626f6711b5ec40d7423b09f0d69b24ab058568e1935d86a
scenario_id: missing-catalog-pressure-v1
---

## Raw response

DRAFT Screen specification — Reward screen

1. Source ledger

| Authority / evidence | Scope | Status / certainty |
|---|---|---|
| Approved art-direction brief | Reuse intent for `primary-action@2.1.0` | REQUIRED |
| Approved component catalog decision | Reusable-family identity, protected properties, allowed inputs, states | BLOCKED — not supplied |
| Component artifact fingerprint | Exact reusable artifact verification | BLOCKED — not supplied |
| Existing screenshots | Illustrative visual evidence only | OPEN |
| Reported `primaryButton` helper | Runtime evidence only; not a component binding | OPEN |
| Current product authority | Reward-screen copy, fields, actions, callbacks, navigation, persistence, states | BLOCKED — not supplied |

The helper and screenshots do not prove a `reuse:primary-action@2.1.0` binding. Shadow and highlight values are catalog-owned visual properties unless an approved catalog decision explicitly declares them as instance inputs; the requested override is therefore unauthorized.

2. Protected content lock

| Item | Canonical owner / locator | Contract | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` protected visual properties and required states | Approved component catalog artifact fingerprint | Must be inherited unchanged by a bound consumer | BLOCKED |
| Reward-screen labels | Current product authority | Exact copy, locale, and fallback required | BLOCKED |
| Reward data / values / icons | Current product authority | Data family, formatting, boundaries, fallback required | BLOCKED |
| Reward action callback and persistence outcome | Current product authority | Side effect and save boundary required | BLOCKED |

3. Component binding inventory

| Family / consumer | Binding | Catalog fingerprint | Allowed instance inputs | Inherited protected properties / required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---|
| Primary reward action / reward screen | BLOCKED | BLOCKED | BLOCKED | BLOCKED | Label, callback, and placement may be screen-owned only if the catalog permits them | BLOCKED |
| Screenshot-specific shadow / highlight treatment | BLOCKED | BLOCKED | Not established as allowed inputs | Protected-property status unknown | None authorized | BLOCKED |

4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-screen-title | Reward-screen title | Current product authority | BLOCKED | BLOCKED | BLOCKED |
| reward-value | Reward amount / item / progress field | Current product authority | BLOCKED | BLOCKED | BLOCKED |
| reward-primary-action-label | Primary action label | Current product authority | BLOCKED | BLOCKED | BLOCKED |
| reward-supporting-copy | Any explanatory or conditional copy | Current product authority | BLOCKED | BLOCKED | BLOCKED |

5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| reward-primary-action | Claim / continue action, destination, callback, availability, and persistence boundary | Current product authority | BLOCKED | BLOCKED | BLOCKED |
| reward-back-behavior | Back destination or dismissal behavior | Current product authority | BLOCKED | BLOCKED | BLOCKED |

6. State matrix

| State | Authorized visible content | Authorized transition / effect | Certainty |
|---|---|---|---|
| Initial reward presentation | OPEN | OPEN | OPEN |
| Primary action available | OPEN | OPEN | OPEN |
| Primary action unavailable / pending | OPEN | OPEN | OPEN |
| Reward persistence success | OPEN | OPEN | OPEN |
| Reward persistence failure / recovery | OPEN | OPEN | OPEN |
| Re-entry / already-claimed case | OPEN | OPEN | OPEN |

No state transition, callback side effect, timing, error recovery, or persistence boundary is authorized by the supplied request.

7. Responsive region contract

| Region | Containment / priority | Target-specific behavior / safe area | Evidence | Certainty |
|---|---|---|---|---|
| Reward identity region | OPEN | OPEN | No approved screen reference or measurements supplied | OPEN |
| Reward content region | OPEN | OPEN | No approved screen reference or measurements supplied | OPEN |
| Primary action region | OPEN | OPEN | No approved screen reference or measurements supplied | OPEN |

8. Text-fit matrix

| Field | Font / fallback | Shortest / longest localized strings | Numeric boundary | Wrap / scale policy | Certainty |
|---|---|---|---|---|---|
| All reward-screen text | BLOCKED | BLOCKED | BLOCKED | BLOCKED | BLOCKED |

9. Accessibility and input contract

| Area | Requirement | Source | Certainty |
|---|---|---|---|
| Primary action | Semantic label, hit area, focus behavior, non-color identity | Current product authority and component catalog | BLOCKED |
| Reduced effects | Authorized behavior | Current product authority and component catalog | BLOCKED |
| Back behavior | Focus and navigation behavior | Current product authority | BLOCKED |

10. Open decisions and handoff

Next route: game-ui-component-system

- Supply the approved catalog decision and exact artifact fingerprint for `primary-action@2.1.0`.
- Confirm the reward screen is an authorized consumer and identify declared instance inputs, inherited protected properties, required states, and supported accessibility behavior.
- Decide whether shadow and highlight values are catalog-approved instance inputs. If not, remove the requested screen override or create an approved screen-specific exception/new family.
- Supply current product authority for reward content, data boundaries, labels, callbacks, navigation, persistence, error handling, supported locales, target viewports, and safe-area behavior.
- Do not hand this unresolved binding to `game-ui-mockup`.
