---
run_id: screen-component-final-5
phase: FINAL
task_name: screen_component_final_5
model: gpt-5.6-terra
reasoning_effort: medium
skill_source_sha256: 31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089
scenario_id: missing-catalog-pressure-v1
---

## Raw response
# DRAFT Screen specification — Reward screen

## 1. Source ledger

| Source | Authority | Applicable decision | Certainty | Status |
|---|---|---|---|---|
| Current request | Product request | Create a reward screen today; labels and callbacks differ per screen | REQUIRED | Partial: labels, callbacks, destinations, persistence, states, and data are not supplied |
| Approved art-direction brief | Art direction | Reuse `primary-action@2.1.0` | REQUIRED | Binding blocked: approved component-catalog decision and exact artifact fingerprint are missing |
| Existing screenshots | Runtime/reference evidence | Visual similarity is reported | DERIVED: similarity is not a reusable-family binding | Cannot authorize component reuse or protected-property changes |
| Reported `primaryButton` helper | Runtime/code evidence | A helper reportedly exists | OPEN: no authoritative catalog decision supplied | Helper name cannot establish reuse |
| Requested shadow/highlight overrides | Current request | Match a screenshot | OPEN | Catalog-owned protected-property exception is not authorized |

Conflicts and missing inputs: the requested reuse and visual overrides lack the component-catalog decision, exact artifact fingerprint, declared allowed instance inputs, protected properties, required states, and approved exception. Product content and behavior authority is also incomplete.

## 2. Protected content lock

| Item | Canonical owner / locator | Lock | Certainty |
|---|---|---|---|
| `primary-action@2.1.0` reusable-family identity | Approved component catalog decision and artifact fingerprint | Do not bind, alter, or infer protected properties until catalog evidence is supplied | BLOCKED |
| Primary-action shadow and highlight | Approved component catalog | Preserve catalog-owned protected properties; requested override is not authorized | BLOCKED |
| Reward-screen labels | Product authority | Preserve exact approved copy once supplied | OPEN |
| Reward data and values | Product/data authority | Preserve approved format, boundaries, and fallback behavior once supplied | OPEN |
| Reward-screen callbacks and navigation | Product/behavior authority | Preserve approved effects and persistence boundary once supplied | OPEN |
| Fonts, icons, and assets | Approved art direction / asset owner | Use only approved identified artifacts | OPEN |

## 3. Component binding inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| CMP-PRIMARY-ACTION | Primary reward-screen action | Approved art-direction brief; component catalog decision and artifact fingerprint missing | Required catalog states: BLOCKED; screen states: OPEN | BLOCKED pending approved responsive contract | BLOCKED |

Binding: `BLOCKED`

- Proposed family: `primary-action@2.1.0`.
- Consumer: reward screen.
- Required catalog artifact fingerprint: `OPEN`.
- Approved consumer list: `OPEN`.
- Allowed instance inputs: `OPEN`; screen-specific labels and callbacks are reported but not catalog-authorized inputs.
- Inherited protected properties: `OPEN`; shadow and highlight override is therefore `BLOCKED`.
- Required states: `OPEN`.
- Screen-owned rules: label content, callback wiring, placement, and responsive behavior are `OPEN` pending product and layout authority.
- `primaryButton` and screenshot similarity are evidence only, not a component binding.

## 4. Content inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| CNT-REWARD-TITLE | Reward-screen title | Product authority missing | OPEN | OPEN | OPEN |
| CNT-REWARD-VALUE | Reward amount, item, or status | Product/data authority missing | OPEN | OPEN | OPEN |
| CNT-PRIMARY-ACTION-LABEL | Primary-action label | Product authority missing | OPEN | OPEN | OPEN |
| CNT-SECONDARY-CONTENT | Any additional labels, fields, icons, or notices | Product authority missing | OPEN | OPEN | OPEN |

Content formats, valid boundaries, fallbacks, locales, and exact copy are `OPEN`.

## 5. Action and navigation inventory

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ACT-PRIMARY | Primary reward-screen action and callback | Product/behavior authority missing | Availability, destination/effect, timing, failure, and recovery: OPEN | OPEN | OPEN |
| NAV-BACK | Back behavior | Product/navigation authority missing | OPEN | OPEN | OPEN |

Persistence boundary, reward-confirmation timing, duplicate-action handling, and navigation destination are `OPEN`.

## 6. State matrix

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| ST-INITIAL | Reward screen initial presentation | Current request establishes screen only | Entry condition, scope, content, transition, and timing: OPEN | OPEN | OPEN |
| ST-ACTION-AVAILABLE | Primary action availability | Product authority missing | OPEN | OPEN | OPEN |
| ST-ACTION-IN-PROGRESS | Action in progress | Product authority missing | OPEN | OPEN | OPEN |
| ST-SUCCESS | Reward action success | Product authority missing | OPEN | OPEN | OPEN |
| ST-FAILURE | Reward action failure | Product authority missing | OPEN | OPEN | OPEN |
| ST-UNAVAILABLE | Action unavailable | Product authority missing | OPEN | OPEN | OPEN |

No transitions, effects, timing, recovery behavior, or state scope are authorized. Unsupported and non-applicable states are `OPEN` pending product authority.

## 7. Responsive region contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| REG-SAFE-AREA | Screen safe-area containment | Target-environment authority missing | All applicable states: OPEN | OPEN | OPEN |
| REG-REWARD-CONTENT | Reward content region | Product and approved layout evidence missing | OPEN | Ordered placement, containment, dimensions, and priority: OPEN | OPEN |
| REG-PRIMARY-ACTION | Primary-action region | Art direction establishes intended family only | OPEN | Placement and target-specific behavior: OPEN | OPEN |

Supported viewports, safe areas, breakpoints, dimensions, containment, priority, and target-specific behavior are `OPEN`.

## 8. Text-fit matrix

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| TXT-REWARD-TITLE | Reward title | Product, locale, and font authority missing | OPEN | Shortest/longest strings, bounds, wrapping/scaling: OPEN | OPEN |
| TXT-REWARD-VALUE | Reward value | Product/data and locale authority missing | OPEN | Numeric boundary, format, bounds, wrapping/scaling: OPEN | OPEN |
| TXT-PRIMARY-ACTION | Primary-action label | Product, locale, and catalog authority missing | OPEN | Shortest/longest strings, bounds, wrapping/scaling: OPEN | OPEN |

Approved fonts, fallbacks, supported locales, representative strings, numeric boundaries, and text-fit policy are `OPEN`.

## 9. Accessibility and input contract

| ID | visible content or action | source | states | responsive rule | certainty |
|---|---|---|---|---|---|
| A11Y-PRIMARY-ACTION | Primary action semantic label, hit area, focus, and input behavior | Accessibility/product and component-catalog authority missing | OPEN | OPEN | OPEN |
| A11Y-REWARD-CONTENT | Non-color identity and reduced-effects behavior | Accessibility/art-direction authority missing | OPEN | OPEN | OPEN |
| A11Y-BACK | Back behavior and focus order | Accessibility/navigation authority missing | OPEN | OPEN | OPEN |

Authorized semantic labels, non-color identities, reduced-effects behavior, focus order, Back behavior, and hit-area requirements are `OPEN`.

## 10. Open decisions and handoff

Next route: game-ui-component-system  
Blocked downstream: game-ui-mockup

- Supply the approved catalog decision for `primary-action@2.1.0`, including exact artifact fingerprint, approved consumers, allowed instance inputs, protected properties, required states, and responsive contract.
- Decide whether shadow and highlight changes are an approved catalog-level versioned variant or an approved screen-specific exception. The reported helper and screenshots cannot authorize either.
- Supply product-approved reward-screen copy, reward data contract, formats, boundaries, fallbacks, supported locales, and conditional content.
- Supply product behavior for each action: availability, callback/effect, navigation destination, persistence boundary, success/failure/recovery, duplicate-input handling, and timing.
- Supply supported environments, target viewports, safe-area rules, approved screen references with measurable layout evidence, fonts, assets, accessibility requirements, and Back/input behavior.
- Keep this specification `DRAFT`; only resolved and approved inputs may proceed to `game-ui-mockup`.
