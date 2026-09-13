# Detailed output and acceptance rules

Read the sections for the current production or verification stage before performing that stage. Exact headers, tables, approval and recovery rules below are normative.

## Authority order

Resolve conflicts in this order and record the result:

1. current user decisions that explicitly revise earlier direction
2. authoritative product and design requirements
3. current approved screen-specific direction
4. shared visual language from current canonical references
5. runtime implementation, used only to inventory the present state and defects

A reference screen can supply shared visual language without becoming a layout or content template. Exclude superseded sources.

## Output contract

Return one concise **Art-direction brief** with these slots, in order:

1. **Authority ledger** — current, supporting, superseded, `OPEN`, and `BLOCKED` sources.
2. **Visual thesis** — the intended player impression in one sentence, or `BLOCKED` when authority is insufficient.
3. **Shared visual language** — palette roles, materials, contour, lighting, typography, icons, and depth supported by current sources.
4. **Component-family decisions** — for every repeated visible family, record exactly `reuse:<componentId>@<version>`, `screen-specific-exception`, `new-family-required`, or `BLOCKED`, with its authority. Similarity alone never establishes reuse.
5. **Screen-specific expression** — qualitative hierarchy, mood, density, and distinction.
6. **Protected invariants** — supplied content, data, navigation, interaction, font, accessibility, and gameplay facts.
7. **Anti-goals** — concrete inconsistent or unreadable outcomes.
8. **Open decisions and handoff** — unresolved decisions and the exact inputs needed by `game-ui-component-system`, `game-ui-screen-spec`, and `game-ui-mockup`.

## Scope boundary

- Do not generate images or write image-generation prompts.
- Do not create or modify production assets, code, or runtime layout.
- Do not invent copy, data, controls, states, fonts, navigation, or accessibility requirements.
- Do not specify pixel geometry, asset manifests, test matrices, or runtime acceptance results.
- Do not create, revise, or approve a component catalog; classify the visual-family need and route it to `game-ui-component-system`.
- Do not continue into mockup, asset production, implementation, or runtime validation in the same response.

## Verification and approval

- Confirm every cited source exists or is explicitly marked `OPEN` or `BLOCKED`.
- Confirm every output slot is present and each factual statement traces to a listed authority.
- Confirm no downstream artifact was produced.
- Keep the brief `DRAFT` until the designated product owner explicitly approves it. The author cannot self-approve or inherit approval from a superseded reference.

Stop after the draft brief. If a component-family decision is `new-family-required` or `BLOCKED`, route it to `game-ui-component-system` before downstream reuse claims. If missing authority prevents a defensible visual thesis, request the smallest product decision or source needed to continue.
