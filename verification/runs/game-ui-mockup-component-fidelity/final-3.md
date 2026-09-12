# game-ui-mockup component fidelity FINAL 3

- Phase: `FINAL`
- Source SHA-256: `77e46749354a5f5f0d9073312a7e6231111dcb09fbc6ac68fbb4631bd102cac9`

## Response

Mockup candidate packet — `DRAFT`

- Concept candidate: generated default-only concept; rejected for reuse fidelity. It visibly drifts the catalog-owned shadow and highlight.
- Production-representative composite: not created. The canonical `reuse:primary-action@2.1.0` representation and declared evidence capability are unavailable.

Component reuse-fidelity matrix

`binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result`  
`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | default: represented by generated concept; pressed: missing | label, callback | shadow: drift in concept, no declared canonical evidence; highlight: drift in concept, no declared canonical evidence; corner treatment: no canonical evidence | BLOCKED`

The generated concept may remain a visual-treatment exploration only; it cannot establish reuse fidelity. The existing `primaryButton` helper is not evidence for `catalog-abc` without a declared capability, and the required pressed state is unrepresented.

No candidate is eligible for product-owner selection or `game-ui-handoff`.

Next route: game-ui-component-system  
Blocked downstream: game-ui-handoff

## Score

- Exact matrix and all fields: yes
- Every required state and protected property explicit: yes
- Exact recovery handoff: yes

