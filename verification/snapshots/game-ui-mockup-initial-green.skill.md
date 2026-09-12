---
name: game-ui-mockup
description: Use when an approved game UI art direction and screen specification need a full-screen visual candidate for product-owner selection.
---

# Game UI Mockup

## Overview

Create full-screen visual candidates from approved direction and screen truth. A mockup is immutable design evidence, not a runtime screen, component sheet, or implementation shortcut.

## Required inputs

- Approved `game-ui-art-direction` and `game-ui-screen-spec` artifacts.
- The screen specification's approved component binding inventory. For every `reuse:<componentId>@<version>` entry, require its catalog artifact fingerprint, consumer, allowed instance inputs, protected properties, required states, canonical representation, and declared evidence capability.
- Current and superseded references, each labeled by role.
- Representative content, states, target viewports, safe areas, and text-fit cases named by the screen specification.
- The protected content lock, including reproducible locators and hashes for content that must remain exact.
- Provenance requirements, output destination, and requested candidate count. A user-supplied generation-attempt budget is optional.

If an approved input is missing or conflicting, stop and mark it `OPEN` or `BLOCKED`. Do not replace it with placeholders, common layouts, remembered platform conventions, or implementation details.

## Tool routing

Use an available image-generation tool only when the approved direction requires a generated or edited bitmap concept. Inspect every referenced image before tool use and follow that tool's rights and editing rules.

When existing assets and code-native primitives fully express the approved direction, record `concept-not-required` and create only deterministic production-representative composites. Do not generate an image merely to fill a packet slot.

## Candidate contract

Produce two distinct artifact types when generation is required:

- **Concept candidate** — retained output bytes used to evaluate visual treatment. Generated text, data, icons, or protected content are illustrative and never source-parity evidence.
- **Production-representative composite** — deterministic composition of approved visual treatment, exact protected bytes, and exact rendered live content. Record the compositor or reproducible procedure, inputs, output dimensions, and hash.

Only a production-representative composite can receive mockup approval or enter downstream evidence.

### Component reuse fidelity

For every bound reusable component, preserve the catalog identity and version. Apply only the screen-owned instance inputs and placement permitted by the approved binding; catalog-owned protected properties and required states remain exact.

A generated component appearance is never reuse-fidelity evidence. It may explore surrounding visual treatment, but it cannot replace, retouch, average, or approximate the approved canonical representation. A similar helper, screenshot, or visual match is also insufficient unless the catalog declares it as an evidence capability for that exact fingerprint.

Record one **Component reuse-fidelity matrix** with these columns:

`binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result`

Use only these results:

- `MATCH` — the exact bound identity and fingerprint are current, every required represented state is visible, all protected properties have declared reproducible evidence, and only allowed instance inputs vary.
- `DRIFT` — evidence exists but a protected property, state, identity, fingerprint, or allowed-input boundary differs. Reject that composite.
- `BLOCKED` — required binding, fingerprint, canonical representation, state, or evidence capability is absent, stale, or conflicting. Do not claim fidelity or select the composite.

- Build prompts and compositions only from approved inputs; label each reference as composition, style, subject, or edit target.
- Produce exactly the requested candidate count and every target viewport named by the screen specification. Do not infer one target from another.
- Show one identified representative state per image. A candidate does not prove states it does not show.
- Use exact approved copy, symbols, data formats, controls, and protected content. Reject corrupt or substituted content instead of calling it illustrative.
- Preserve approved hierarchy, safe-area intent, responsive regions, and live-content space; record every departure.
- Keep retained concept bytes unchanged. Save deterministic composites separately with stable versioned names; never overwrite an approved reference.
- Record prompt, tool and mode, reference roles, generation identifier when available, dimensions, hashes, transformations, target screen and state, rights, and current/superseded status.
- Follow the supplied attempt budget. If none exists, stop after three failed attempts for one requested candidate and target, recording rejected hashes and the unresolved visual region.

## Output contract

Return one **Mockup candidate packet** containing:

1. concept path or `concept-not-required`, plus production-representative composite paths and previews
2. exact prompt or deterministic composition procedure, with reference roles
3. screen-spec compliance matrix mapping each required region, content family, and represented state to visible evidence
4. component reuse-fidelity matrix for every reusable binding
5. observed defects, rejected candidates, and intentional differences
6. provenance, hashes, and current/superseded status
7. one product-owner selection question

## Scope boundary

- Do not load a full-screen mockup as a runtime texture or production atlas.
- Do not create production assets, manifests, scene code, layout code, or invisible input regions.
- Do not continue into handoff, asset production, implementation, runtime validation, or approval review.
- Do not create, revise, approve, or version a component catalog from mockup work.
- Do not treat visual similarity, generation success, or the author's preference as approval.

## Verification and approval

- Inspect every retained image at original detail; verify dimensions, hashes, crop safety, text, data, controls, and protected-content parity.
- Reproduce deterministic composites and require identical output hashes.
- Trace every visible requirement to the approved screen specification; there must be no orphan content or controls.
- Keep every candidate `DRAFT` until the designated product owner explicitly selects its exact composite hashes.

Stop when a component binding, fingerprint, canonical representation, required state, or declared evidence capability is missing, stale, or conflicting. Mark the matrix row `BLOCKED` and return to `game-ui-component-system` before `game-ui-handoff`.

Use this exact recovery handoff:

`Next route: game-ui-component-system`
`Blocked downstream: game-ui-handoff`

Stop after presenting the candidate packet. Send only explicitly selected production-representative composites to `game-ui-handoff`.
