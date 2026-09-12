# game-ui-mockup component fidelity FINAL 4

- Phase: `FINAL`
- Source SHA-256: `77e46749354a5f5f0d9073312a7e6231111dcb09fbc6ac68fbb4631bd102cac9`

## Response

Mockup candidate packet — `DRAFT`

1. Concept: generated default-state concept available, but rejected for downstream evidence: it changes catalog-owned shadow and highlight.  
   Production-representative composite: unavailable.

2. Reference roles: generated concept = style exploration only. No canonical `reuse:primary-action@2.1.0` representation or declared evidence capability is available.

3. Screen-spec compliance: consumer `reward-screen` cannot represent the required `pressed` state. Default-only concept does not prove pressed.

4. Component reuse-fidelity matrix

`binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result`  
`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | default: concept only; pressed: missing | label, callback | shadow: drifted in concept; highlight: drifted in concept; corner treatment: missing canonical evidence | BLOCKED`

5. Rejected candidate: generated default concept; visually preferable, but it modifies protected properties and cannot establish reuse fidelity.

6. Provenance/status: generated concept is `DRAFT` style-only material. No production-representative composite, reproducible composition procedure, canonical render, or evidence hash exists.

7. Product-owner selection question: Can the component owner provide the current canonical render and declared evidence capability for `catalog-abc`, including default and pressed states, before this screen proceeds?

Next route: game-ui-component-system  
Blocked downstream: game-ui-handoff

## Score

- Exact matrix and all fields: yes
- Every required state and protected property explicit: yes
- Exact recovery handoff: yes

