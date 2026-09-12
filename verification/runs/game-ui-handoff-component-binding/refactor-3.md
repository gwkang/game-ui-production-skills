Phase: REFACTOR
Source SHA-256: 18238a9a08d4e52497db4e95d70a859924b8ada66d9dcb698f15da5c6c85dfa8
Model: gpt-5.6-terra
Reasoning: medium
Score: exact binding yes; full matrix yes; ten columns yes.

DRAFT — UI handoff packet

1. Source lock

- Selected composite: reward-screen composite — `OPEN` (path, hash, dimensions, represented-state source, approval reference, provenance, and source-parity record were not supplied).
- Approved state: default; pressed.
- Exclusions: no asset, code, catalog, or fidelity-decision changes.
- Source parity: `OPEN`; protected source hash cannot be confirmed.

2. Region geometry

- Reward screen hierarchy, source-pixel rectangles, normalized coordinates, anchors, spacing, safe areas, and z-order: `OPEN`. Exact geometry is required; it must be copied from the approved composite measurement record, not inferred.

3. Component inventory

`primary action | OPEN | live control | OPEN/OPEN | OPEN | OPEN | default, pressed | none | OPEN`

4. Component implementation binding matrix

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`

`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton (visually similar; matching bounds only) | OPEN — catalog declaration for this target and fingerprint not provided | label; callback | shadow (m-shadow; runtime evidence must reproduce locator); highlight (m-highlight; runtime evidence must reproduce locator); corner treatment (m-corner; runtime evidence must reproduce locator) | default; pressed (pressed-state mapping and evidence OPEN) | MATCH | BLOCKED`

5. Asset-versus-live ownership

- Primary action label and callback: live; input owner `OPEN`.
- Primary-action visual chrome: protected reusable component; raster/vector/code ownership `OPEN`.
- Fallback and per-element source-parity rows: `OPEN`.

6. Typography and content bounds

- Font, text rectangle, alignment, line policy, representative boundary, and minimums: `OPEN`; do not add `themeColor`, which is outside the allowed inputs.

7. State and interaction coverage

- `default`: visual transition owner, hit rectangle, semantic label, disabled behavior, and conditional presence: `OPEN`.
- `pressed`: mapping and implementation evidence: `OPEN`; it may not be omitted.

8. Responsive transformation rules

- Supported targets, anchors, constraints, fit mode, crop-safe area, and target-specific behavior: `OPEN`.

9. Acceptance comparison map

- Approved landmarks, runtime evidence rectangles, allowed differences, and rejection conditions: `OPEN`.
- Required protected landmarks: `m-shadow`, `m-highlight`, `m-corner`.

10. Open decisions and handoff

The `reuse:primary-action@2.1.0` row is `BLOCKED`: the current `primaryButton` is not proven to be the exact catalog-declared adapter for `catalog-abc`, and it lacks declared evidence capability, protected-property evidence, and pressed-state mapping. Matching bounds and visual similarity are insufficient.

`Next route: game-ui-component-system`  
`Blocked downstream: game-ui-asset-production, game-ui-implementation`
