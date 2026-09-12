---
name: game-ui-asset-production
description: Use when an approved game UI handoff has visible art families that need production readiness or reuse verification before implementation.
---

# Game UI Asset Production

## Overview

Turn an approved handoff into a reproducible, independently reviewable asset-readiness packet while keeping live content and input in code.

## Required inputs

- Approved art direction, screen specification, mockup, and handoff.
- Locked sources, hashes, geometry, states, fit rules, target slots, and consumers.
- Rights, license, bundle budget, runtime asset conventions, and migration authority.

## Production mode

Choose exactly one handoff-authorized mode:

- `new-production` — create or change raster/vector bytes and record reproducible transforms.
- `verified-reuse-only` — change no asset bytes; every visible family uses an existing runtime asset.
- `no-new-raster` — change no asset bytes; at least one visible family is code-native. Generation, transform, migration, and bundle delta are `NOT APPLICABLE`.

Use image generation only for approved new bitmap work and follow the available tool's rights rules. Produce text-free components, never a full-screen runtime texture. Store editable sources and optimized outputs in project-declared locations.

Every crop, resize, cleanup, pack, and compression operation must be reproducible by a checked-in script or exact command/config. Record input and output hashes. Never crop a mockup at runtime, bake live content or semantic labels, or overwrite shared assets without approved consumer migration.

## Fidelity and source parity

Inventory every visible art family as `new production`, `verified reuse`, or `missing`. Reuse requires target-size composed-screen evidence against the approved mockup; technical validity or zero byte cost is insufficient. Compare material, contour, lighting, perspective, detail density, color harmony, and optical weight across combined families.

Maintain a source-parity manifest for each family: classification, runtime destination, current source hash, mockup/QA input and hash, candidate output, consumer, and provenance status. Reuse evidence reads the exact production runtime bytes. New-production evidence reads the exact candidate destined for the declared runtime location. Any disagreement is blocking.

## Output contract

Return a `DRAFT` **asset-readiness packet** with:

1. source lock, rights, dimensions, hashes, and exclusions
2. asset manifest: stable ID, file, consumer, slot, state, format, and fallback
3. fidelity coverage for every visible family and its parity row
4. generation record, or `NOT APPLICABLE`
5. deterministic transform and hash procedure, or `NOT APPLICABLE`
6. intrinsic/visible bounds, padding, pivot, crop safety, stretch region, and fit mode
7. isolated-pixel and composed-screen visual QA
8. per-file and total bundle impact against the approved budget
9. provenance record in the project-owned registry
10. open defects and reviewed inputs for `game-ui-implementation`

Mark the packet `REVIEW_READY` only after reproducibility and visual QA pass; independent `art-asset-review` owns the quality verdict.

## Scope and verification

- Do not change content, live typography, input, layout, or scene code.
- Do not redesign the approved mockup or delete superseded assets; migration owns cleanup.
- Regenerate changed outputs and compare hashes; in reuse modes recompute runtime hashes without inventing production work.
- Inspect original pixels and target-size composites over relevant backgrounds at every supported target.
- Verify alpha/edge artifacts, aspect, padding, pivot, state distinction, text clearance, frame isolation, and source parity.
- Require independent asset review before implementation.

Stop for unknown rights, source, measurement, slot, or consumer. Stop while any family is missing, reuse is unproven, evidence differs from production bytes, or a style mismatch remains. Do not begin implementation.
