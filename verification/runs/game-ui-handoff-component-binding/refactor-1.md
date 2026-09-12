Phase: REFACTOR
Source SHA-256: 18238a9a08d4e52497db4e95d70a859924b8ada66d9dcb698f15da5c6c85dfa8
Model: gpt-5.6-terra
Reasoning: medium
Score: exact binding yes; full matrix yes; ten columns yes.

DRAFT UI handoff packet

1. Source lock

- Selected composite, hash, dimensions, geometry, provenance, approval, source parity: OPEN — values were stated as available but not provided.
- Represented states: `default`, `pressed`.
- Exclusion: no asset, code, catalog, or fidelity-decision changes.

2. Region geometry

- OPEN — source-pixel rectangles and normalized coordinates require the approved composite’s actual dimensions and measurements.

3. Component inventory

`primaryButton | OPEN | live control | OPEN | OPEN | OPEN | default, pressed | no substitute | BLOCKED`

4. Component implementation binding matrix

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`

`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton (visually similar only; version/fingerprint unknown) | OPEN — catalog-declared adapter and evidence capability unknown | label; callback | shadow [m-shadow]: implementation evidence must reproduce locator; highlight [m-highlight]: implementation evidence must reproduce locator; corner treatment [m-corner]: implementation evidence must reproduce locator | default; pressed (pressed mapping OPEN) | MATCH | BLOCKED`

5. Asset-versus-live ownership

`primaryButton chrome | component asset/code | OPEN | OPEN | live label and callback input | no visually similar substitution | BLOCKED`

6. Typography and content bounds

- `label` is live content; its font, text rectangle, alignment, line policy, and boundary measurements are OPEN.

7. State and interaction coverage

- `default`: required.
- `pressed`: required; implementation-state mapping is OPEN.
- Hit rectangle, semantic label, disabled behavior, and conditional presence: OPEN.

8. Responsive transformation rules

- OPEN — requires approved target dimensions, safe areas, and measured source geometry.

9. Acceptance comparison map

- `m-shadow`, `m-highlight`, and `m-corner` must each be reproduced by implementation evidence.
- Runtime evidence rectangles and allowed differences: OPEN pending measured approved source.

10. Open decisions and handoff

- `primaryButton` cannot be recorded as `reuse=yes` alone: its exact binding identity, catalog fingerprint, declared adapter, evidence capability, protected-property evidence, and pressed-state mapping are required.
- `themeColor` is not an allowed instance input and cannot be added.
- Neither downstream route is ready.

Next route: game-ui-component-system  
Blocked downstream: game-ui-asset-production, game-ui-implementation
