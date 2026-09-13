# Detailed output and acceptance rules

Read the sections for the current production or verification stage before performing that stage. Exact headers, tables, approval and recovery rules below are normative.

## Component runtime integration contract

Emit one **Component runtime integration matrix**. Immediately before its header, emit this exact plain-text title once, without a Markdown heading marker or decoration:

`Component runtime integration matrix`

Use this exact plain-text header once, with no leading or trailing pipe:

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | implementation evidence | integration status`

Build every row by this ten-cell recipe. Copy the first eight cells verbatim from the approved handoff `Component implementation binding matrix`: binding, catalog artifact fingerprint, consumer, implementation target, declared adapter, allowed instance inputs, protected-property evidence, and required states. Do not normalize identifiers, remove a `reuse:` prefix, reorder lists, or append notes to copied cells. Put project-declared test, probe, or capability mappings in `implementation evidence`; put only `READY`, `OPEN`, or `BLOCKED` in `integration status`.

- `READY` means the consumer uses the exact declared adapter for the same catalog identity and fingerprint, passes only the allowed instance inputs, preserves every protected property, maps all required states one-to-one, and has passing current evidence from the focused tests or scoped observations selected under the Implementation contract. This is integration readiness, not rendered-fidelity acceptance.
- `OPEN` is only an optional internal implementation choice that cannot alter identity, adapter, inputs, protected properties, states, or behavior.
- `BLOCKED` covers an added or undeclared input, any protected-property override, a substituted or renamed helper, a missing state or probe, a stale fingerprint, or evidence that does not map to the declared catalog capability.

Only the allowed instance inputs may cross the screen-to-component boundary. A generic `style`, `theme`, `skin`, `tint`, `scale`, or similar escape prop is forbidden when it can alter a protected property unless that exact input is explicitly listed as allowed. Local pointer handlers cannot simulate a missing component state. Matching dimensions, passing unrelated tests, similar names, or visual resemblance do not prove that the declared adapter or catalog fingerprint is in use.

Implementation evidence maps protected properties and required states to project-declared tests, probes, or evidence capabilities. It proves integration wiring, not pixels: rendered fidelity remains owned by `game-ui-runtime-validation`.

If implementation would change a binding, representation, declared adapter, allowed input, protected property, required state, or catalog fingerprint, emit these lines exactly once:

`Next route: game-ui-component-system`

`Blocked downstream: game-ui-runtime-validation`

If the handoff matrix is missing, stale, conflicting, or not `READY`, use `Next route: game-ui-handoff`. If the production disposition, binding readiness, or packet readiness is missing or blocked, use `Next route: game-ui-asset-production`. In either case keep `Blocked downstream: game-ui-runtime-validation`.

## Implementation contract

Inspect repository impacts and preserve unrelated changes using project-provided tools. Match verification to the scoped regression risk:

1. Reuse an adequate focused test or observation; add a test only when a behavior, input, state or responsive boundary lacks meaningful regression coverage.
2. For a defect, observe the pre-change failure when reproducible. Record unavailable RED evidence honestly; never invent it or build a harness just to fill the packet.
3. Implement the smallest complete change. For a small static layout edit, existing target-size before/after captures and scoped runtime observation may suffice; do not duplicate coordinate literals in tests merely to obtain RED/GREEN.
4. Recheck affected criteria on the current candidate. Preserve valid unaffected evidence and existing mandatory project gates. Runtime fidelity still belongs to runtime validation; independent verification is not waived.

Keep component state valid through its public operations; do not expose mutable internals or hidden globals that bypass the approved ownership/input boundary. Separate layout, live-data binding and effects when it clarifies the changed responsibility. Reuse existing adapters; avoid speculative inheritance, interfaces and per-frame work unrelated to the requirement.

Map every component and state to its asset, layout owner, live text/data owner, input owner, states, and fallback. Keep dynamic values live. Use declared intrinsic/visible geometry, anchors, safe areas, and fit modes. A mockup or screenshot is never a runtime hit surface.

Do not change approved copy, content, currency, font, navigation, Back behavior, persistence, availability, or state rules to simplify implementation. Do not use runtime tint, outline, scale, glow, or spacing to conceal missing or mismatched production art.

## Output contract

Maintain an **implementation evidence packet** with:

1. input lock, hashes, approvals, parity records, supported targets, and exclusions
2. impact map, consumers, shared files, and preserved changes
3. Component integration map containing the Component runtime integration matrix, plus asset/frame, layout, live content, input rectangle, and fallback ownership
4. verification choice and regression boundary; pre-change failure/evidence when applicable, otherwise an explicit reason RED is unavailable or not applicable
5. implementation result: minimal code path and current focused test or scoped observation evidence; do not label an unexecuted test GREEN
6. contract preservation before/after for product-owned content and behavior
7. deviation ledger: zero deviations or exact source, reason, measured effect, owner decision, and approval
8. changed files, tests, purposes, and commands
9. open decisions and locked build inputs for `game-ui-runtime-validation`

## Scope and verification

- Do not generate, repair, or compensate for art; return art defects to `game-ui-asset-production`.
- Do not invent missing geometry, responsive behavior, states, or product facts.
- Execute the focused tests or scoped observations selected for affected layout, content binding, states, input geometry, navigation, persistence and approved boundaries; do not add unrelated checks. Use meaningful regression tests for changed behavior when required by the selected risk and project policy.
- Confirm every handoff row has a runtime consumer and no extra UI or behavior was introduced.
- Run project-required test/build/audit commands, but do not claim rendered fidelity before runtime validation.

Stop for missing approval, source parity, measurements, states, assets, or product authority. Stop if work would change an out-of-scope product contract. After the selected implementation checks pass with current evidence, route the unchanged build to runtime validation. Observation evidence is not an unexecuted test result or final visual acceptance.
