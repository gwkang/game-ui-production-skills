# game-ui-mockup component fidelity FINAL 5

- Phase: `FINAL`
- Source SHA-256: `77e46749354a5f5f0d9073312a7e6231111dcb09fbc6ac68fbb4631bd102cac9`

## Response

Mockup candidate packet — `DRAFT / BLOCKED`

- Concept: generated default-state concept only; rejected for downstream evidence because shadow and highlight drift.
- Production-representative composite: none. The exact canonical render and declared evidence capability for `reuse:primary-action@2.1.0` are unavailable.
- Pressed state: missing.

Component reuse-fidelity matrix

`binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result`  
`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | default: represented but drifted; pressed: missing | label, callback | shadow: drifted in generated concept; highlight: drifted in generated concept; corner treatment: no canonical evidence available | BLOCKED`

Observed defects: the concept alters catalog-owned shadow and highlight; it does not represent the required pressed state. The similar `primaryButton` helper is not canonical evidence for fingerprint `catalog-abc`, and no declared evidence capability exists.

No reuse-fidelity pass can be recorded, no state may be omitted, and nothing may proceed to handoff.

Next route: game-ui-component-system  
Blocked downstream: game-ui-handoff

Product-owner question: Please provide or restore the canonical `reuse:primary-action@2.1.0` representation and declared reproducible evidence capability for `catalog-abc`, including default and pressed states, before selecting a production-representative composite.

## Score

- Exact matrix and all fields: yes
- Every required state and protected property explicit: yes
- Exact recovery handoff: yes

