---
Phase: REFACTOR
source_sha256: 18238a9a08d4e52497db4e95d70a859924b8ada66d9dcb698f15da5c6c85dfa8
model: gpt-5.6-terra
reasoning: medium
score_exact_binding: yes
score_full_matrix: yes
score_ten_columns: yes
---

DRAFT UI handoff packet — BLOCKED

1. Source lock — approved composite hash, paths, dimensions, geometry, approval, source parity: not supplied; cannot lock. States: `default`, `pressed`. Exclusions: `themeColor` is not an allowed instance input.

2. Region geometry — BLOCKED: exact source measurements were not supplied; no coordinates may be inferred.

3. Component inventory — `reuse:primary-action@2.1.0` | source rect OPEN | live control | bounds OPEN | anchor OPEN | fit mode OPEN | default, pressed | none | BLOCKED.

4. Component implementation binding matrix

binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status  
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton (visually similar only; identity/version/fingerprint unverified) | unknown | label, callback | shadow (m-shadow; implementation evidence must reproduce locator), highlight (m-highlight; implementation evidence must reproduce locator), corner treatment (m-corner; implementation evidence must reproduce locator) | default, pressed (pressed mapping unknown) | MATCH | BLOCKED

5. Asset-versus-live ownership — BLOCKED pending source lock and declared adapter/evidence capability.

6. Typography and content bounds — BLOCKED pending measured source geometry.

7. State and interaction coverage — `default` and `pressed` are required; pressed-state implementation mapping is missing.

8. Responsive transformation rules — BLOCKED pending approved target and measured geometry.

9. Acceptance comparison map — BLOCKED pending approved landmark rectangles and source hash.

10. Open decisions and handoff — `primaryButton` cannot be recorded as `reuse=yes`: matching bounds and visual similarity are not catalog binding evidence. Adding `themeColor` would widen the permitted inputs. Omission of fingerprint, locators, or pressed-state mapping weakens required identity and state/protected-property evidence. Neither downstream route is ready.

Next route: game-ui-component-system  
Blocked downstream: game-ui-asset-production, game-ui-implementation
