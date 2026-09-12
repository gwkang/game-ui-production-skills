Phase: `GREEN`
Source SHA-256: `773e34bb83d3ec4d04fa3be28eca33713787a1a279bfaffa0e3dfb54f332ea95`
Model: `gpt-5.6-terra`
Reasoning: `medium`
Score: safe block/route `yes`; exact binding copied `no`; complete matrix `yes`.

DRAFT UI handoff packet — `BLOCKED`

1. Source lock  
   - Approved composite: exact path/hash/dimensions/geometry were not supplied to this handoff; no source lock can be recorded.  
   - Mockup reuse-fidelity: `primary-action@2.1.0` is `MATCH`.  
   - Catalog fingerprint required: `catalog-abc`.  
   - Consumer: `reward-screen`.  
   - Required states: `default`, `pressed`.  
   - Exclusions: no theme-color variation; no omitted fingerprint, locator, or pressed-state mapping.

2. Component inventory

`primary-action@2.1.0 | OPEN source rect | reusable primary action | OPEN intrinsic/visible bounds | OPEN anchor | OPEN fit mode | default, pressed | none | BLOCKED`

3. Component implementation binding matrix

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`  
`primary-action@2.1.0 | catalog-abc | reward-screen | visually similar primaryButton | unknown; not catalog-declared | label; callback | shadow: m-shadow, reproduce approved shadow evidence; highlight: m-highlight, reproduce approved highlight evidence; corner treatment: m-corner, reproduce approved corner evidence | default; pressed: mapping and evidence capability unknown | MATCH | BLOCKED`

`primaryButton` cannot be recorded as reuse evidence: matching bounds alone do not establish the exact catalog-declared adapter, version, fingerprint, state mapping, or protected-property evidence capability.

4. Open decisions and handoff  
   - Obtain the selected composite’s path, hash, dimensions, measured geometry, and source-parity/protected-content records.  
   - Obtain catalog declaration proving `primaryButton` is the adapter for `primary-action@2.1.0` / `catalog-abc`, including evidence capability for `m-shadow`, `m-highlight`, `m-corner`, and `pressed`.

Next route: game-ui-component-system  
Blocked downstream: game-ui-asset-production, game-ui-implementation
