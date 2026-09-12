---
phase: REFACTOR
source_sha256: 18238a9a08d4e52497db4e95d70a859924b8ada66d9dcb698f15da5c6c85dfa8
model: gpt-5.6-terra
reasoning: medium
score:
  exact_binding: yes
  full_matrix: yes
  ten_columns: yes
---

DRAFT UI handoff packet

1. Source lock

- Selected composite: approved reward-screen composite; exact selected path, hash, dimensions, represented-state source, provenance, protected-content record, and source-parity record: `OPEN` (not supplied).
- Approval: approved reward-screen composite.
- Mockup reuse-fidelity: `MATCH`.
- Covered states: `default`, `pressed`.
- Exclusions: no asset production or implementation is authorized by this packet.

2. Region geometry

- Reward-screen hierarchy, source-pixel rectangles, normalized coordinates, anchors, alignment, spacing, safe areas, and z-order: `OPEN` pending the exact approved composite geometry. No coordinates are inferred.

3. Component inventory

`primary-action | OPEN | live control | intrinsic/visible bounds OPEN | OPEN | OPEN | default, pressed | no substitute helper | OPEN`

4. Component implementation binding matrix

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`

`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | OPEN: current primaryButton is visually similar with matching bounds only; its version and fingerprint are unknown | OPEN: no catalog-declared adapter or evidence capability supplied for catalog-abc | label; callback | shadow [m-shadow: implementation evidence must reproduce the approved locator]; highlight [m-highlight: implementation evidence must reproduce the approved locator]; corner treatment [m-corner: implementation evidence must reproduce the approved locator] | default; pressed [pressed mapping OPEN: implementation evidence must reproduce it] | MATCH | BLOCKED`

5. Asset-versus-live ownership

`primary-action chrome | OPEN | live label | callback input owner OPEN | no helper fallback permitted | source parity OPEN`

6. Typography and content bounds

- Label font, text rectangle, alignment, line policy, and representative boundaries: `OPEN`; only `label` is an allowed instance input.

7. State and interaction coverage

- `default`: visual transition owner, hit rectangle, semantic label, disabled behavior, and conditional presence: `OPEN`.
- `pressed`: state mapping and implementation evidence: `OPEN`; it must not be omitted.

8. Responsive transformation rules

- Approved targets, anchors, constraints, fit mode, and crop-safe behavior: `OPEN` pending measured source geometry and target records.

9. Acceptance comparison map

- Approved landmarks and runtime evidence rectangles: `OPEN`.
- Required rejection conditions: any identity/fingerprint mismatch; absent catalog-declared adapter or evidence capability; widened inputs; missing `default` or `pressed` coverage; missing reproduction evidence for `m-shadow`, `m-highlight`, or `m-corner`.

10. Open decisions and handoff

- `game-ui-asset-production`: `BLOCKED`.
- `game-ui-implementation`: `BLOCKED`.
- Do not record `primaryButton/reuse=yes`, add `themeColor`, omit `catalog-abc` or the locators, or drop the `pressed` mapping: each would weaken the approved binding contract.

Next route: game-ui-component-system  
Blocked downstream: game-ui-asset-production, game-ui-implementation
