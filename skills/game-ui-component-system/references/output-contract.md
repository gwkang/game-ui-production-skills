# Detailed output and acceptance rules

Read the sections for the current production or verification stage before performing that stage. Exact headers, tables, approval and recovery rules below are normative.

## Decision rule

Classify every repeated family as exactly one of:

| Decision | Use when |
|---|---|
| `reuse:<componentId>@<version>` | An approved entry covers the consumer, state, adapter, and evidence capability. |
| `screen-specific-exception` | Current authority requires a deliberate non-shared expression and records its scope. |
| `new-family-required` | No approved entry covers the requested structure or protected appearance. |
| `BLOCKED` | Authority, capability, compatibility, or approval evidence is missing or conflicting. |

Similarity, majority usage, averaged values, a common primitive, or passing partial evidence cannot establish reuse.

## Output contract

Produce one concise **Component catalog decision** containing:

1. **Authority ledger** — current, supporting, superseded, conflicting, `OPEN`, and `BLOCKED` sources.
2. **Family inventory** — proposed stable ID, semantic version, representation kind, variants, consumers, and exceptions.
3. **Contract** — structure, allowed instance inputs, protected properties, states, and accessibility invariants.
4. **Adapter binding** — the project-declared implementation adapter and fallback owner.
5. **Evidence map** — declared capabilities, protected-property coverage, landmarks or probes, and project-owned tolerances.
6. **Compatibility** — covered presentation roles, consumers, and explicit incompatibilities.
7. **Decision and approval** — one classification per family plus the exact artifact fingerprint and approval status.
8. **Next route** — the smallest upstream decision or downstream owner allowed to proceed.

Use [references/component-catalog.schema.json](component-catalog.schema.json) when creating a machine-readable catalog. Run `scripts/validate_component_catalog.py CATALOG.json PROFILE.json` to enforce cross-field profile, evidence-coverage, identity, and approval invariants.

## Scope boundary

- Do not design screen composition, invent product content, measure an unapproved reference, produce assets, or implement runtime components.
- Do not convert a conflicting family into a new standard by averaging values.
- Do not approve the catalog you authored or treat approval of one version as approval of another.
- Do not claim visual fidelity from evidence that fails to cover every protected property and required state.

## Verification and stop conditions

Confirm that each value traces to the authority ledger, every protected property has a declared evidence capability, and the approval fingerprint matches the exact catalog artifact. Stop before implementation when any required authority, capability, compatibility decision, or approval is missing. After approval, route measurements to handoff, representation readiness to asset production when applicable, runtime integration to implementation, and observed drift to runtime validation and independent acceptance.

## Common mistakes

- A shared low-level helper is not an approved component family.
- A new label or callback may be an allowed input; a new material treatment is a protected-property change.
- Lack of raster evidence does not block a project whose declared hierarchy, vector, command-trace, or native evidence covers the contract.
