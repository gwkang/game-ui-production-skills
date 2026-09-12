---
run_id: screen-component-green-4
phase: GREEN
task_name: screen_component_green_4
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 0b97e9815e132c98ff918b5360bb9b442f2d0a93e6b62814e2f552fcb7d258f8
scenario_id: missing-catalog-pressure-v1
---

## Raw response

DRAFT Screen specification — Reward screen

1. Source ledger

| Source | Status | Certainty | Use |
|---|---|---|---|
| Approved art-direction brief: reuse `primary-action@2.1.0` | Current visual authority | REQUIRED | Visual reuse intent only |
| Approved component-catalog decision | Not supplied | BLOCKED | Required to bind reusable component |
| Catalog artifact fingerprint for `primary-action@2.1.0` | Not supplied | BLOCKED | Required to verify binding |
| Existing screenshots | Reported visual evidence | OPEN | Not permission for requirements or reuse |
| `primaryButton` helper | Reported runtime evidence | OPEN | Not a component binding |
| Reward-screen labels and callbacks | Not supplied | BLOCKED | Product authority required |
| Reward-screen behavior, navigation, data, supported environments, locales, fonts, accessibility | Not supplied | BLOCKED | Product/runtime authority required |

Conflict: the requested shadow/highlight overrides would alter catalog-owned visual properties, but no approved catalog decision declares them allowed instance inputs. This cannot be authorized from screenshots or helper similarity.

2. Protected content lock

| ID | Protected content | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| LOCK-001 | Approved art-direction intent to reuse the `primary-action@2.1.0` family | Approved art-direction brief | All applicable component states | BLOCKED pending catalog contract | REQUIRED |
| LOCK-002 | Component-family protected properties, required states, and exact artifact identity | Component catalog and artifact fingerprint | BLOCKED | BLOCKED | BLOCKED |
| LOCK-003 | Reward labels, values, icons, fonts, and data formats | Product/content authority | BLOCKED | BLOCKED | BLOCKED |
| LOCK-004 | Reward completion and callback behavior | Product/behavior authority | BLOCKED | BLOCKED | BLOCKED |

3. Component binding inventory

| ID | Binding | Consumer | Allowed instance inputs | Inherited protected properties / required states | Screen-owned rules | Certainty |
|---|---|---|---|---|---|---|
| CMP-001 | BLOCKED | Reward screen primary action | BLOCKED | BLOCKED; catalog artifact fingerprint absent | Label, callback, and placement remain BLOCKED pending product and catalog authority | BLOCKED |

`primaryButton` and visual similarity in screenshots are evidence only, not a reusable-family binding. Shadow and highlight overrides are not authorized and must not be specified as screen-owned rules.

4. Content inventory

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| CNT-001 | Reward-screen title | Product/content authority | BLOCKED | BLOCKED | BLOCKED |
| CNT-002 | Reward value or reward description | Product/data authority | BLOCKED | BLOCKED | BLOCKED |
| CNT-003 | Primary-action label | Product/content authority | BLOCKED | BLOCKED | BLOCKED |
| CNT-004 | Reward-related icons or imagery | Approved asset/content authority | BLOCKED | BLOCKED | BLOCKED |

Formats, boundaries, fallbacks, and live-data ownership are OPEN.

5. Action and navigation inventory

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| ACT-001 | Primary reward-screen action | Product/behavior authority | BLOCKED | BLOCKED | BLOCKED |
| ACT-002 | Back or dismiss action, if any | Product/behavior authority | OPEN | BLOCKED | OPEN |

Availability, destination/effect, persistence boundary, callback timing, failure recovery, and duplicate-action behavior are OPEN.

6. State matrix

| State / transition | Source | Contract | Certainty |
|---|---|---|---|
| Initial reward-screen state | Product authority | OPEN | OPEN |
| Reward data loading / unavailable / error states | Product and runtime authority | OPEN | OPEN |
| Primary action enabled / disabled / pressed / completion states | Product authority plus approved component catalog | BLOCKED | BLOCKED |
| Primary action transition and side effects | Product/behavior authority | OPEN | OPEN |
| Return, dismiss, and Back behavior | Product/navigation authority | OPEN | OPEN |
| Unsupported states | No authority supplied | Explicitly non-applicable only after authority confirms scope | OPEN |

7. Responsive region contract

| ID | Region | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| RGN-001 | Safe-area root | Target-environment authority | All | BLOCKED | BLOCKED |
| RGN-002 | Reward content region | Approved screen reference or measured handoff | BLOCKED | BLOCKED | BLOCKED |
| RGN-003 | Primary-action region | Approved component catalog and screen reference | BLOCKED | BLOCKED | BLOCKED |

No viewport, safe-area, containment, priority, or dimension evidence was supplied.

8. Text-fit matrix

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| TXT-001 | Reward title | Font, locale, and copy authority | BLOCKED | BLOCKED | BLOCKED |
| TXT-002 | Reward value / description | Data format and locale authority | BLOCKED | BLOCKED | BLOCKED |
| TXT-003 | Primary-action label | Product copy and catalog contract | BLOCKED | BLOCKED | BLOCKED |

Approved fonts, locale set, shortest/longest strings, numeric bounds, owned text bounds, and wrapping/scaling policy are OPEN.

9. Accessibility and input contract

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| A11Y-001 | Primary-action semantic label and hit area | Product/accessibility authority and component catalog | BLOCKED | BLOCKED | BLOCKED |
| A11Y-002 | Focus and Back behavior | Product/navigation authority | OPEN | BLOCKED | OPEN |
| A11Y-003 | Non-color identity and reduced-effects behavior | Accessibility authority and component catalog | BLOCKED | BLOCKED | BLOCKED |

10. Open decisions and handoff

Stop before mockup. The reward screen cannot bind `reuse:primary-action@2.1.0` until `game-ui-component-system` provides:

- The approved catalog decision for `primary-action@2.1.0`.
- Its exact artifact fingerprint.
- Authorized consumers, declared instance inputs, protected shadow/highlight properties, and required states.
- An explicit decision on whether this reward screen is permitted to use the family and whether the requested visual overrides are allowed.

Product authority must additionally provide reward-screen copy, live-data format and bounds, actions/callbacks, navigation, persistence and recovery behavior, supported viewports/locales, and accessibility/input requirements.

Only resolved, approved bindings and product inputs may be handed to `game-ui-mockup`.
