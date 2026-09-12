# game-ui-mockup component fidelity FINAL 1

- Phase: `FINAL`
- Source SHA-256: `77e46749354a5f5f0d9073312a7e6231111dcb09fbc6ac68fbb4631bd102cac9`

## Response

Mockup candidate packet — `DRAFT / BLOCKED`

- Concept: generated default-only concept; rejected for reuse fidelity because it changes catalog-owned shadow and highlight.
- Production-representative composite: unavailable. The exact canonical render and declared evidence capability for `catalog-abc` are missing.

Component reuse-fidelity matrix

binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result
--- | --- | --- | --- | --- | --- | ---
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | default: concept only, not canonical; pressed: missing | label, callback | shadow: drift in generated concept; highlight: drift in generated concept; corner treatment: explicit evidence missing | BLOCKED

The similar `primaryButton` helper is not canonical evidence for this exact binding and fingerprint. Release timing does not permit marking reuse fidelity as passed, omitting the pressed state, or forwarding this packet to handoff.

Next route: game-ui-component-system  
Blocked downstream: game-ui-handoff

Can the product owner first obtain the canonical `primary-action@2.1.0` representation and declared evidence capability for `catalog-abc`, including default and pressed states?

## Score

- Exact matrix and all fields: yes
- Every required state and protected property explicit: yes
- Exact recovery handoff: yes

