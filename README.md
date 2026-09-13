# Game UI Production Skills

Ten portable agent skills for taking an existing game's UI from visual direction through independent runtime acceptance. Each skill has one owner and can be installed independently; a project should use only the stages its request actually needs.

## Current contract layout

Each SKILL.md contains the role, inputs and handoff. Read its references/output-contract.md for exact output, approval, coverage and recovery rules. Validation uses a separate subagent, frozen criteria and bounded author-repair/verifier-recheck; out-of-scope observations do not create tasks or gates. Historical verification snapshots remain tied to their original source hashes.

## Role chain

| Stage | Skill | Input | Output |
|---|---|---|---|
| Direction | `game-ui-art-direction` | Product and visual authority | Approved visual-direction brief |
| Component governance | `game-ui-component-system` | Approved project profile and repeated-family authority | Versioned catalog decision |
| Specification | `game-ui-screen-spec` | Approved direction and product contracts | Exact content/state/input/responsive specification |
| Candidate | `game-ui-mockup` | Approved direction and specification | Selectable production-representative composites |
| Handoff | `game-ui-handoff` | Selected composite and source locks | Measured ownership and geometry contract |
| Asset readiness | `game-ui-asset-production` | Approved handoff and asset authority | Reproducible asset-readiness packet |
| Asset review | `art-asset-review` | Asset packet and target-size evidence | Independent asset-quality verdict |
| Implementation | `game-ui-implementation` | Approved specifications and reviewed assets | Test-first implementation evidence |
| Runtime validation | `game-ui-runtime-validation` | Locked build and upstream approvals | Actual-runtime evidence packet |
| UI acceptance | `game-ui-acceptance-review` | Complete current evidence | Independent UI-only verdict |

The full chain is:

`art-direction → [component-system when reuse/new family/drift is in scope] → screen-spec → mockup → handoff → asset-production → art-asset-review → implementation → runtime-validation → acceptance-review`

Do not treat the chain as mandatory ceremony for every UI request. Start at the stage that owns the requested outcome, but satisfy that skill's required inputs. Read-only reviews do not authorize fixes, and approval at one stage does not approve later stages.

## Installation

Copy each desired folder from `skills/` into a skill directory recognized by your agent runtime. Common user-level locations include `~/.agents/skills/`; project-local installations commonly use `.agents/skills/`. Keep the folder name and `SKILL.md` together.

Example:

```text
.agents/skills/
  game-ui-art-direction/
    SKILL.md
  game-ui-screen-spec/
    SKILL.md
```

Install only the roles you need. Cross-skill names in the documents describe handoff ownership; they do not install dependencies automatically.

## Project inputs

These skills do not include a project profile or assume an engine, genre, repository layout, viewport, locale, currency, build command, evidence tool, or asset pipeline. Each skill obtains applicable values from the current project's approved authority. Missing values remain `OPEN` or `BLOCKED` rather than being guessed.

Image generation is optional and belongs only to approved bitmap concept or production work. Code-native and verified-reuse workflows explicitly support skipping generation.

## Verification evidence

The `verification/` directory records the baseline failure and isolated forward-test result for each skill. These records test role boundaries and decision behavior; they do not certify a particular game's assets, implementation, or release.

## Rights

The skill text and repository documentation are licensed under the MIT License. Third-party tools, fonts, references, generated media, and project assets retain their own terms and are not included here.
