---
name: game-ui-asset-production
description: Use when an approved game UI handoff has visible art families that need production readiness or reuse verification before implementation.
---

# Game UI Asset Production

## Overview

Turn an approved handoff into a reproducible, independently reviewable asset-readiness packet while keeping live content and input in code.

## Required inputs

- Approved art direction, screen specification, mockup, and handoff.
- The handoff's current `Component implementation binding matrix` and the exact approved component catalog artifact or project-declared resolver for its fingerprint.
- Locked sources, hashes, geometry, states, fit rules, target slots, and consumers.
- Rights, license, bundle budget, runtime asset conventions, and migration authority.

## Production mode

Choose exactly one handoff-authorized mode:

- `new-production` — create or change raster/vector bytes and record reproducible transforms.
- `verified-reuse-only` — change no asset bytes; every visible family uses an existing runtime asset.
- `no-new-raster` — change no asset bytes; at least one visible family is code-native. Generation, transform, migration, and bundle delta are `NOT APPLICABLE`.

Use image generation only for approved new bitmap work and follow the available tool's rights rules. Produce text-free components, never a full-screen runtime texture. Store editable sources and optimized outputs in project-declared locations.

Every crop, resize, cleanup, pack, and compression operation must be reproducible by a checked-in script or exact command/config. Record input and output hashes. Never crop a mockup at runtime, bake live content or semantic labels, or overwrite shared assets without approved consumer migration.

## Component production disposition

Carry every reusable handoff row into a `Component production disposition matrix`. Copy the upstream binding, catalog artifact fingerprint, consumer, allowed instance inputs, protected-property names and evidence locators, and required states verbatim. Resolve the representation only from the approved catalog artifact with the same fingerprint; a screenshot, similar export, or convenient runtime helper cannot replace it.

Emit this header exactly, followed by one plain pipe-delimited row per reusable binding. Each line has exactly nine `|` separators and no leading or trailing pipe:

`binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence`

Use exactly one production disposition per row:

- `REUSE_CANONICAL` — reuse the exact approved raster, vector, mixed, or other file-backed representation; any deterministic packaging stays source-linked to that representation and does not create a new component identity or version.
- `ASSET_NOT_REQUIRED` — the approved representation is code-native or a native widget and needs no produced asset bytes. Emit `production-asset-not-required`, name the catalog-declared adapter and evidence capability, and do not create a bitmap, raster export, placeholder, or atlas entry merely to produce an asset.
- `NEW_PRODUCTION` — create bytes only when the current catalog identity, handoff, and approval authorize that representation and every protected property and required state remains covered.
- `BLOCKED` — identity, fingerprint, representation kind, source representation, adapter, evidence capability, protected-property coverage, or required state is missing, stale, conflicting, or broadened.

A derived atlas slice, optimized export, or package is an adapter artifact, not a new component version. Record its exact source representation, deterministic transform, output hash, consumers, and state mapping. Do not change the component's identity, version, allowed inputs, protected properties, or required states during production.

If a proposed asset changes the approved representation, component identity/version, allowed inputs, protected properties, or required states, reject it from the current binding and use:

`Next route: game-ui-component-system`

When the approved canonical representation remains valid, keep that row's `REUSE_CANONICAL` or `ASSET_NOT_REQUIRED` path available and route only the rejected proposal upstream. When no valid canonical path remains, mark the row `BLOCKED` and emit:

`Blocked downstream: game-ui-implementation`

If the handoff row is absent, not `READY`, or bound to a different catalog fingerprint, use `Next route: game-ui-handoff` and block implementation. Asset production does not repair catalog or handoff decisions.

## Fidelity and source parity

Inventory every visible art family as `new production`, `verified reuse`, or `missing`. Reuse requires target-size composed-screen evidence against the approved mockup; technical validity or zero byte cost is insufficient. Compare material, contour, lighting, perspective, detail density, color harmony, and optical weight across combined families.

Maintain a source-parity manifest for each family: classification, runtime destination, current source hash, mockup/QA input and hash, candidate output, consumer, and provenance status. Reuse evidence reads the exact production runtime bytes. New-production evidence reads the exact candidate destined for the declared runtime location. Any disagreement is blocking.

## Output contract

Return a `DRAFT` **asset-readiness packet** with:

1. source lock, rights, dimensions, hashes, and exclusions
2. asset manifest: stable ID, file, consumer, slot, state, format, and fallback
3. component production disposition matrix plus fidelity coverage for every visible family and its parity row
4. generation record, or `NOT APPLICABLE`
5. deterministic transform and hash procedure, or `NOT APPLICABLE`
6. intrinsic/visible bounds, padding, pivot, crop safety, stretch region, and fit mode
7. isolated-pixel and composed-screen visual QA
8. per-file and total bundle impact against the approved budget
9. provenance record in the project-owned registry
10. open defects and reviewed inputs for `game-ui-implementation`

Mark the packet `REVIEW_READY` only after reproducibility and visual QA pass. Independent `art-asset-review` owns the quality verdict for produced or file-backed art. A binding marked `ASSET_NOT_REQUIRED` records art review as `NOT APPLICABLE`; its catalog evidence remains required and its rendered fidelity is verified by runtime validation and UI acceptance.

## Scope and verification

- Do not change content, live typography, input, layout, or scene code.
- Do not redesign the approved mockup or delete superseded assets; migration owns cleanup.
- Regenerate changed outputs and compare hashes; in reuse modes recompute runtime hashes without inventing production work.
- Inspect original pixels and target-size composites over relevant backgrounds at every supported target.
- Verify alpha/edge artifacts, aspect, padding, pivot, state distinction, text clearance, frame isolation, and source parity.
- Require independent asset review before implementation.

Stop for unknown rights, source, measurement, slot, or consumer. Stop while any family is missing, reuse is unproven, evidence differs from production bytes, or a style mismatch remains. Do not begin implementation.
