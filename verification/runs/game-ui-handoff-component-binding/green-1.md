Phase: GREEN
source SHA-256: 773e34bb83d3ec4d04fa3be28eca33713787a1a279bfaffa0e3dfb54f332ea95
model: gpt-5.6-terra
reasoning: medium
score: safe block/route yes; exact binding copied no; complete matrix yes

DRAFT UI handoff packet — reward-screen composite

1. Source lock  
Selected composite: approved reward-screen composite.  
Hash: OPEN — exact value not supplied. Dimensions/geometry: OPEN — exact values not supplied. States: `default`, `pressed`. Mockup reuse-fidelity: `MATCH`. Source parity/protected-content record: OPEN. Exclusion: `themeColor` is not an allowed instance input.

2. Region geometry  
Reward-screen hierarchy and all source-pixel/normalized rectangles: OPEN pending the supplied exact composite geometry; no coordinates may be inferred from matching bounds.

3. Component inventory  

`primary-action@2.1.0 | OPEN | live control | intrinsic/visible bounds OPEN | OPEN | OPEN | default, pressed | none | BLOCKED`

4. Component implementation binding matrix  

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`  
`primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton (version/fingerprint unknown) | OPEN — catalog declaration absent | label; callback | shadow: m-shadow, runtime evidence must reproduce approved shadow; highlight: m-highlight, runtime evidence must reproduce approved highlight; corner treatment: m-corner, runtime evidence must reproduce approved corner treatment | default; pressed (pressed mapping OPEN) | MATCH | BLOCKED`

`themeColor` is excluded. A visually similar `primaryButton` with matching bounds is neither the exact binding nor reuse evidence without a catalog-declared adapter and bound-fingerprint evidence capability.

5. Asset-versus-live ownership  
Primary-action chrome/protected treatment: catalog-bound component art/code, BLOCKED. Label: live text, allowed input. Callback: live input owner, allowed input. All remaining reward-screen ownership/parity rows: OPEN.

6. Typography and content bounds  
Label font, text rectangle, alignment, line policy, and boundaries: OPEN; do not infer.

7. State and interaction coverage  
`default`: required. `pressed`: required, mapping/evidence OPEN. Hit rectangle, semantic label, disabled behavior, and conditional presence: OPEN.

8. Responsive transformation rules  
Anchors, constraints, fit mode, crop-safe area, and target behavior: OPEN pending exact geometry and approved-target evidence.

9. Acceptance comparison map  
Approved landmarks and runtime evidence rectangles: OPEN. Protected comparison requirements are `m-shadow`, `m-highlight`, and `m-corner`; rejection condition: any failure to reproduce the protected treatment, or absence of required pressed-state mapping.

10. Open decisions and handoff  
Do not record a shortened `primaryButton/reuse=yes` substitution, omit `catalog-abc`, omit locators, collapse the pressed state, or add `themeColor`. The current implementation target’s version/fingerprint, catalog-declared adapter, evidence capability, protected-property evidence, pressed mapping, source hash, and geometry must be resolved.

`Next route: game-ui-component-system`  
`Blocked downstream: game-ui-asset-production, game-ui-implementation`
