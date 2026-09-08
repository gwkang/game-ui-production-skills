---
name: game-ui-handoff
description: Use when an approved game UI mockup needs a measurable implementation contract before asset or code work.
---

# Game UI Handoff

## Overview

Translate approved visual evidence into measurable geometry, ownership, scaling, and state rules without producing assets or code.

## Required inputs

- Approved `game-ui-art-direction`, `game-ui-screen-spec`, and `game-ui-mockup` artifacts.
- Exact selected composite paths, dimensions, hashes, represented states, provenance, and product-owner decision.
- Protected-content and source-parity records.
- Supported targets, safe areas, reusable components, and current implementation evidence when available.

Stop when an input is missing, stale, conflicting, or bound to a different hash.

## Measurement rule

Measure at original resolution. Express each rectangle in source pixels and normalized coordinates `(x/W, y/H, width/W, height/H)`. Label every value `MEASURED`, `DERIVED`, or `OPEN` and cite its source. A derived runtime value includes its formula and assumptions.

Do not invent coordinates, tolerances, font sizes, copy, breakpoints, states, or fit behavior. Visual plausibility is not measurement.

## Output contract

Return one `DRAFT` **UI handoff packet** with:

1. **Source lock** — selected files, hashes, dimensions, states, approvals, exclusions, and source parity.
2. **Region geometry** — hierarchy, rectangles, normalized coordinates, anchors, alignment, spacing, safe areas, and z-order.
3. **Component inventory** — ID, role, source region, intrinsic and visible bounds, pivot, padding, and reuse status.
4. **Asset-versus-live ownership** — raster/vector/code chrome, live text/data, input owner, fallback, and parity row for every element.
5. **Typography and content bounds** — font, text rectangle, alignment, line policy, representative boundaries, and unresolved minimums.
6. **State and interaction coverage** — visual state, transition owner, hit rectangle, semantic label, disabled behavior, and conditional presence.
7. **Responsive transformation rules** — anchors, constraints, fit mode, crop-safe area, and behavior for every approved target.
8. **Acceptance comparison map** — approved landmark, runtime evidence rectangle, allowed difference, and rejection condition.
9. **Open decisions and handoff** — unresolved measurements and separate inputs for `game-ui-asset-production` and `game-ui-implementation`.

Use component rows shaped as `ID | source rect | owner | intrinsic/visible bounds | anchor | fit mode | states | fallback | certainty`.

## Scope and verification

- Keep dynamic content and controls live; never bake them into component art or invisible image hit regions.
- Do not create assets, code, atlases, manifests, or layout modules.
- Do not declare a stretchable region without measured border and corner evidence; distinguish frame bounds from visible bounds.
- Recompute normalized values and require pixel round-trip within an explicitly sourced tolerance.
- Overlay measured rectangles on a copy and inspect at original detail.
- Confirm every screen-spec row has visual, content, input, and state ownership and every protected source retains its approved hash.

The product owner approves visual fidelity; implementation owners may reject infeasible or ambiguous measurements. Stop after the packet and do not begin asset production or implementation.
