---
name: game-ui-handoff
description: Use when an approved game UI mockup needs a measurable implementation contract before asset or code work.
---

# Game UI Handoff

## Overview

Translate approved visual evidence into measurable geometry, ownership, scaling, and state rules without producing assets or code.

## Required inputs

- Approved `game-ui-art-direction`, `game-ui-screen-spec`, and `game-ui-mockup` artifacts.
- The approved mockup's `Component reuse-fidelity matrix`, with a current `MATCH` row for every reusable binding.
- Exact selected composite paths, dimensions, hashes, represented states, provenance, and product-owner decision.
- Protected-content and source-parity records.
- Supported targets, safe areas, reusable components, and current implementation evidence when available.

Stop when an input is missing, stale, conflicting, or bound to a different hash.

## Measurement rule

Measure at original resolution. Express each rectangle in source pixels and normalized coordinates `(x/W, y/H, width/W, height/H)`. Label every value `MEASURED`, `DERIVED`, or `OPEN` and cite its source. A derived runtime value includes its formula and assumptions.

Do not invent coordinates, tolerances, font sizes, copy, breakpoints, states, or fit behavior. Visual plausibility is not measurement.

## Component implementation binding

Carry every reusable binding into implementation without shortening its ID, dropping its version or catalog artifact fingerprint, widening its allowed instance inputs, or collapsing its required states and protected-property evidence. A visually similar helper or matching bounds are not binding or reuse evidence unless the current catalog declares that exact implementation target as an adapter and provides its evidence capability for the bound fingerprint.

Emit this block in order:

`Component implementation binding matrix`

`binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status`

Then emit one row per reusable binding. Name every allowed input, required state, and protected property separately. Carry each mockup evidence locator into the relevant protected-property or state entry and state what implementation evidence must reproduce it.

Copy the upstream `binding`, catalog artifact fingerprint, consumer, allowed instance inputs, protected-property names and locators, required states, and mockup fidelity cells verbatim. Do not remove the `reuse:` prefix, normalize identifiers, or substitute an implementation helper name for the binding. A `BLOCKED` packet still emits the heading, header, and every complete binding row before the recovery handoff; a route-only response is incomplete.

Emit the header and each row as plain pipe-delimited lines with no leading or trailing pipe. Each line has exactly nine `|` separators and therefore ten cells. Inside a cell, separate multiple values with commas or semicolons, never another pipe. Count the cells before returning the packet.

Use only these handoff statuses:

- `READY` — upstream mockup fidelity is current `MATCH`; the implementation target is the exact catalog-declared adapter for the same identity and fingerprint; every allowed input, protected property, required state, and required implementation-evidence method is explicit.
- `OPEN` — an optional measurement or implementation choice remains unresolved but does not weaken identity, fingerprint, allowed-input, protected-property, or state requirements. Keep the affected downstream input open.
- `BLOCKED` — required identity, fingerprint, implementation target, declared adapter, evidence capability, protected-property evidence, state mapping, or upstream fidelity is missing, stale, conflicting, or broadened. Do not hand off the affected component.

## Output contract

Return one `DRAFT` **UI handoff packet** with:

1. **Source lock** — selected files, hashes, dimensions, states, approvals, exclusions, and source parity.
2. **Region geometry** — hierarchy, rectangles, normalized coordinates, anchors, alignment, spacing, safe areas, and z-order.
3. **Component inventory** — ID, role, source region, intrinsic and visible bounds, pivot, padding, and reuse status.
4. **Component implementation binding matrix** — exact catalog identity, implementation target, allowed variation, protected evidence, state coverage, and readiness.
5. **Asset-versus-live ownership** — raster/vector/code chrome, live text/data, input owner, fallback, and parity row for every element.
6. **Typography and content bounds** — font, text rectangle, alignment, line policy, representative boundaries, and unresolved minimums.
7. **State and interaction coverage** — visual state, transition owner, hit rectangle, semantic label, disabled behavior, and conditional presence.
8. **Responsive transformation rules** — anchors, constraints, fit mode, crop-safe area, and behavior for every approved target.
9. **Acceptance comparison map** — approved landmark, runtime evidence rectangle, allowed difference, and rejection condition.
10. **Open decisions and handoff** — unresolved measurements and separate readiness for `game-ui-asset-production` and `game-ui-implementation`.

Use component rows shaped as `ID | source rect | owner | intrinsic/visible bounds | anchor | fit mode | states | fallback | certainty`.

## Scope and verification

- Keep dynamic content and controls live; never bake them into component art or invisible image hit regions.
- Do not create assets, code, atlases, manifests, or layout modules.
- Do not create, revise, approve, or version a component catalog or mockup fidelity decision from handoff work.
- Do not declare a stretchable region without measured border and corner evidence; distinguish frame bounds from visible bounds.
- Recompute normalized values and require pixel round-trip within an explicitly sourced tolerance.
- Overlay measured rectangles on a copy and inspect at original detail.
- Confirm every screen-spec row has visual, content, input, and state ownership and every protected source retains its approved hash.

Stop when the implementation target, its version or fingerprint, declared adapter, evidence capability, or protected-property evidence is missing, stale, or conflicting. Mark the row `BLOCKED` and return to `game-ui-component-system` before `game-ui-asset-production` or `game-ui-implementation`.

Use this exact recovery handoff:

`Next route: game-ui-component-system`
`Blocked downstream: game-ui-asset-production, game-ui-implementation`

If the upstream reuse-fidelity row is absent or not `MATCH`, stop and return to `game-ui-mockup`; do not repair or reinterpret it in the handoff packet.

The product owner approves visual fidelity; implementation owners may reject infeasible or ambiguous measurements. Stop after the packet and do not begin asset production or implementation.
