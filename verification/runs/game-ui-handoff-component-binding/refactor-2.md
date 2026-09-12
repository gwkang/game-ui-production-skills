Phase: `REFACTOR`
Source SHA-256: `18238a9a08d4e52497db4e95d70a859924b8ada66d9dcb698f15da5c6c85dfa8`
Model: `gpt-5.6-terra`
Reasoning: `medium`
Score: exact binding yes; full matrix yes; ten columns NO because label | callback split the allowed-input cell.

DRAFT UI handoff packet

1. **Source lock** — Approved reward-screen composite; mockup fidelity: `MATCH`. Exact selected path, hash, dimensions, geometry, provenance, approval, protected-content, and source-parity records are not present in this handoff input: `OPEN`. States: `default`, `pressed`.

2. **Region geometry** — `OPEN`: no source-pixel rectangles, normalized coordinates, safe areas, anchors, or z-order were supplied.

3. **Component inventory**

`primary-action | OPEN | live control | OPEN | OPEN | OPEN | default; pressed | OPEN | BLOCKED`

4. **Component implementation binding matrix**

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`

`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton (matching bounds only; version and fingerprint unknown) | UNKNOWN; no catalog-declared adapter or evidence capability supplied | label | callback | shadow: m-shadow; highlight: m-highlight; corner treatment: m-corner; implementation evidence must reproduce each locator | default; pressed (pressed mapping UNKNOWN) | MATCH | BLOCKED`

5. **Asset-versus-live ownership** — `OPEN`; dynamic label and callback remain live. No raster/vector/code-chrome ownership or parity rows were supplied.

6. **Typography and content bounds** — `OPEN`; no measured text rectangle, font, fit policy, or boundary evidence was supplied.

7. **State and interaction coverage** — `default` and `pressed` required; pressed-state implementation mapping is `BLOCKED`. Hit rectangle, semantic label, disabled behavior, transition owner, and conditional presence are `OPEN`.

8. **Responsive transformation rules** — `OPEN`; no approved target, safe-area, fit, anchor, or crop rules were supplied.

9. **Acceptance comparison map** — `OPEN`; runtime evidence rectangles and permitted differences cannot be defined without the supplied source geometry and protected evidence.

10. **Open decisions and handoff** — Do not substitute `primaryButton`, add `themeColor`, omit `catalog-abc`, omit protected locators, or collapse the pressed-state requirement. The reusable binding is blocked pending the exact catalog-declared adapter for `reuse:primary-action@2.1.0`, matching version/fingerprint, evidence capability, protected-property evidence, and pressed-state mapping.

Next route: game-ui-component-system  
Blocked downstream: game-ui-asset-production, game-ui-implementation
