# Detailed output and acceptance rules

Read the sections for the current production or verification stage before performing that stage. Exact headers, tables, approval and recovery rules below are normative.

## Review contract

Recompute source parity. Reuse evidence must read the same runtime path and hash as production; new-production evidence must read the exact candidate destined for its declared runtime location. Packet, transform, mockup/QA inputs, consumers, and provenance must agree.

Technical validity is necessary but insufficient. Inspect original pixels, target-slot renders, and the full composed screen against the approved mockup.

For every visible family, record source, reference, target-size evidence, and verdict for:

- material and surface treatment
- contour and edge finish
- lighting and shadow logic
- perspective and volume
- detail density at actual display size
- color harmony and contrast hierarchy
- optical weight across combined families

Separately verify rights, transformations, dimensions, format, alpha bounds, halos, frame bleed, silhouette, color-plus-symbol distinction, aspect, padding, pivot, crop safety, target-slot fit, reproducibility, and production status.

## Output contract

Return one review containing:

1. reviewer identity, excluded roles, and independence statement
2. source/output hash lock and verified parity rows
3. technical quality matrix
4. composed-screen craft quality matrix
5. target-size comparison for every supported target
6. findings with severity, owner, and reopen condition
7. exactly `Decision: APPROVE ASSET QUALITY` or `Decision: REJECT ASSET QUALITY`

Approval requires complete family coverage, rights and technical evidence, verified parity, no missing or unproven reuse, and no open craft-quality finding. Product-owner fidelity approval remains separate; this verdict does not approve implementation or the complete UI.

## Stop conditions

- Reject missing rights, hashes, transforms when bytes changed, geometry, target slots, consumers, visible families, or target-size evidence.
- Reject substitute assets or evidence produced from bytes different from the declared runtime source.
- Reject mixed style or a composed-screen loss of approved material, lighting, perspective, detail density, color hierarchy, or optical weight even when isolated assets pass.
- Do not edit assets, manifests, code, or evidence. Route findings to `game-ui-asset-production`.
