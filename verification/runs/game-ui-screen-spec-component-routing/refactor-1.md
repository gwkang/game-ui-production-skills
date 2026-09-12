---
run_id: screen-component-refactor-1
phase: REFACTOR
task_name: screen_component_refactor_1
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: f609c9f07719c2972626f6711b5ec40d7423b09f0d69b24ab058568e1935d86a
scenario_id: missing-catalog-pressure-v1
---

## Raw response

DRAFT Screen specification — reward screen

1. Source ledger

| Authority / evidence | Scope | Certainty | Status |
|---|---|---:|---|
| Approved art-direction brief | Reuse intent: `primary-action@2.1.0` | REQUIRED | Catalog decision and artifact fingerprint unavailable |
| Current request | Reward-screen purpose; labels and callbacks vary by screen | REQUIRED | Exact labels, callbacks, states, navigation, content, and layout are unspecified |
| Existing screenshots | Visual evidence only | OPEN | Cannot authorize reusable binding or protected-property overrides |
| Reported `primaryButton` helper | Runtime-code evidence only | OPEN | Not a reusable-family binding |

Conflict: the request asks to use the helper and screenshots as proof of reuse and to override shadow/highlight values. The component binding is unresolved, and catalog-owned protected properties may not be overridden without an approved catalog decision.

2. Protected content lock

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| LOCK-001 | `primary-action@2.1.0` reusable-family identity | Approved art-direction brief | All required states | OPEN pending catalog artifact | REQUIRED |
| LOCK-002 | Reward labels and callbacks vary per screen | Current request | Applicable screen states | Screen-owned values only after product authority supplies them | REQUIRED |
| LOCK-003 | Shadow and highlight properties | Component catalog authority | Applicable component states | Inherit unchanged unless catalog declares an allowed input | OPEN |

Assets, fonts, icons, exact copy, reward data fields, behavior, and canonical locators/hashes: OPEN.

3. Component binding inventory

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| CMP-001 | Primary action | Approved art-direction brief | Required states: OPEN | `BLOCKED`; requires approved `primary-action@2.1.0` catalog decision and exact artifact fingerprint, including allowed instance inputs and protected properties | BLOCKED |
| CMP-002 | Per-screen label and callback | Current request | OPEN | May be screen-owned only if the catalog declares them allowed instance inputs | OPEN |
| CMP-003 | Shadow/highlight override | Current request | OPEN | Not authorized; requires catalog decision declaring these inputs or a screen-specific exception | BLOCKED |

Consumer: reward screen. Inherited protected properties, required states, allowed instance inputs, and catalog artifact fingerprint: BLOCKED.

4. Content inventory

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| CNT-001 | Reward-screen labels | Current request | OPEN | Exact copy, locale, formatting, bounds, and fallback are OPEN | OPEN |
| CNT-002 | Reward data / values | No authority supplied | OPEN | Data family, format, valid boundaries, and fallback are OPEN | OPEN |

5. Action and navigation inventory

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| ACT-001 | Primary-action callback | Current request says callbacks differ | OPEN | Availability, destination/effect, persistence boundary, failure/recovery behavior, and timing are OPEN | OPEN |

6. State matrix

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| ST-001 | Reward screen | No state authority supplied | Initial, loading, success, unavailable, error, dismissed: OPEN | No responsive behavior authorized | OPEN |
| ST-002 | Primary action | No transition authority supplied | Enabled, disabled, pressed, loading, success, error: OPEN | Required states must come from the approved component catalog | OPEN |

All transitions, side effects, timing, recovery behavior, and state scope are OPEN.

7. Responsive region contract

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| RGN-001 | Reward-screen regions | No viewport, safe-area, or measurement authority supplied | All | Ordered regions, containment, priority, dimensions, targets, and safe-area handling are OPEN | OPEN |

8. Text-fit matrix

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| TXT-001 | Reward labels and primary-action label | No copy, locale, font, or bounds authority supplied | All applicable states | Fonts, fallbacks, shortest/longest strings, numeric boundaries, wrapping/scaling policy, and owned bounds are OPEN | OPEN |

9. Accessibility and input contract

| ID | Visible content or action | Source | States | Responsive rule | Certainty |
|---|---|---|---|---|---|
| A11Y-001 | Reward-screen input and accessibility | No accessibility/input authority supplied | All | Semantic labels, non-color identity, reduced-effects behavior, focus, Back behavior, and hit-area requirements are OPEN | OPEN |

10. Open decisions and handoff

Next route: game-ui-component-system

- Provide the approved `primary-action@2.1.0` catalog decision and exact artifact fingerprint.
- Specify its consumers, allowed instance inputs, protected shadow/highlight properties, and required states.
- Decide whether the reward screen needs a catalog-authorized shadow/highlight input or a documented screen-specific exception.
- Provide product authority for reward content, labels, reward-data format and boundaries, callbacks, action availability, navigation/effects, persistence, states, transitions, locales, target viewports, safe areas, fonts, and accessibility/input behavior.
- Do not hand off to `game-ui-mockup` until the component binding is resolved.
