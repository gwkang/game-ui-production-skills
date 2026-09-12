# Component governance source audit

## Authority

For this work, `sharing/game-ui-production-skills/skills/` is the portable authoring source. `.agents/skills/` remains a project compatibility installation and must be reconciled semantically rather than used as an independent portable source.

## Current skill inventory

The table records the current portable/local hashes after each completed semantic reconciliation. Every pair still differs because project-local safety contracts are preserved; none was reconciled by byte-copying one source over the other.

| Skill | Portable SHA-256 | Local SHA-256 | Status |
|---|---|---|---|
| game-ui-art-direction | `f029a3ed3d26f80f3a0786a261d25224d793a5f2d48773f5a2f0517ec9456439` | `5581b6ec86b399946042ba8a280020e882752c8ec95c4206cf89f9db295e1c30` | diverged; component slice reconciled |
| game-ui-screen-spec | `31468ff6c935a1853507a5861c82b61f716b643b592aee7f2c56396562c69089` | `cdada60646633c8800325678ddfe7e0879257c39f0f1c5aee4e2673c41a44ace` | diverged; component slice reconciled |
| game-ui-mockup | `8a56c18ea2e13feaaf1c32a59fd084088e51314c8290c60369e9aad882e8758b` | `4cfd4953d5a461a605c8bfe731f03e3cede86512a352f4dd4dafcf2fa621f620` | diverged; component slice reconciled |
| game-ui-handoff | `49c2a15d6369e1636aabdbc42255a547b5716509ac9ff7bae901b21bc40c3571` | `6446cd000a55d5e0e4b5209a5ca8eeefb787df888a1687b338b40a5559031a58` | diverged; component slice reconciled |
| game-ui-asset-production | `3f522e546c1053f7a75465999c6463d94bc55486dd20499d2d5f7feee0e0a998` | `3ff5ba459b555efd99ca7ee5e3d34d5de21364cef915018de6570ad6a5e00ce3` | diverged; component slice reconciled |
| art-asset-review | `c8917b65377f0ba490c3b1c1c3aff2e2f5a7f07a3a898ae41758c975131c84fa` | `70d30ab3ffab62e038c91a6a268c5b87f78f8e74b13df06e8d6d7d3396d9f28b` | diverged |
| game-ui-implementation | `b18ff4eb6a35aedcb1396396ecf5d32e78c44d24ce4b90bbe7de888a14de3b4a` | `400e0b7e5b18b35bb107d31f20b9d63c27ba252fd920201470db11bb145c1db2` | diverged; component slice reconciled |
| game-ui-runtime-validation | `e4e69adbd723200f889e18b3c657b612c4a7344cf3c3c220816ab1ba2e4a2fd1` | `0d5dbeed900d434a9b69b529c984923e1168b77bb115945289d2ab83cb3a72bd` | diverged; component slice reconciled |
| game-ui-acceptance-review | `6421a62426ce5bb539c0a446c93a48d4806e318da45c5865d1b630c413c2d9ea` | `c1438767ad8d8814fc0dda01fee218d92ce18c98f1aa6f6cd3b3a7cd9a602eff` | diverged; component slice reconciled |

Before the component-integration reconciliation, `game-ui-implementation` hashes were portable `a8be376a3b66981c58a327afa3e7e036211fd6e07fcf6ae94ad1ffc327df70b6` and local `28fd1923bf0dd4e2d90d5efa651d9b4ffe7219d4187293cc3f886cd198284f43`. The portable bytes are locked in `snapshots/game-ui-implementation-pre-component-integration.skill.md`.

## New skill installation

`game-ui-component-system/SKILL.md` has SHA-256 `75a86ad77dfb3e5709edcd298cd1bbebd3b68749885024d53a5001f43ad4b690` in both the portable source and project installation, classified `identical`. Their catalog schemas and validator scripts are semantically equal. This does not authorize publishing or bulk replacement of the nine diverged skills.

## Semantic reconciliation map

| Skill | Portable-only emphasis | Local-only contract to preserve | Evidence | Later reconciliation |
|---|---|---|---|---|
| game-ui-art-direction | Engine-neutral authority inputs | Project authority order and local artifact routing | `game-ui-art-direction-baseline.md` and repository art-direction tests | Completed: catalog classification slot added after a 5-control/5-forward RED/GREEN run |
| game-ui-screen-spec | Portable content/state contract | Local protected-content lock and pipeline versioning | `game-ui-screen-spec-baseline.md`, complete run records, and pipeline tests | Completed: carry catalog bindings without transferring ownership after 5 RED, 5 initial GREEN, 5 REFACTOR, and 5 FINAL runs |
| game-ui-mockup | Representation-neutral candidates and binding-level reuse fidelity | Local production-representative composite, source parity, and fixed portrait targets | `game-ui-mockup-baseline.md`, raw pressure runs, and pipeline tests | Reconciled; preserve local specialization |
| game-ui-handoff | Project-declared measurement and exact implementation binding | Local target measurements, source parity, and evidence snapshots | `game-ui-handoff-baseline.md`, raw pressure runs, and pipeline tests | Reconciled; preserve local specialization |
| game-ui-asset-production | Raster/vector/code/native readiness | Local provenance paths and composed-art gates | `game-ui-asset-production-baseline.md`, raw pressure runs, snapshots, and pipeline tests | Reconciled; preserves project specialization while preventing per-screen component recreation |
| art-asset-review | General composed craft review | Local aquarium slot and target-size evidence | `art-asset-review-baseline.md` and pipeline tests | No change until a component representation actually needs art review |
| game-ui-implementation | Runtime-neutral integration boundary | Local impact graph, TDD, content, and Back contracts | `game-ui-implementation-baseline.md`, raw pressure runs, snapshot, and pipeline tests | Reconciled; rejects protected overrides while preserving local safety gates |
| game-ui-runtime-validation | Capability-declared runtime evidence | Local browser, viewport, content, and source-parity gates | `game-ui-runtime-validation-baseline.md`, raw pressure runs, snapshot, and pipeline tests | Reconciled; requires actual-runtime protected-property and state coverage |
| game-ui-acceptance-review | Independent evidence-locked verdict | Local art-quality and product runtime checkpoints | `game-ui-acceptance-review-baseline.md`, raw pressure runs, snapshot, and pipeline tests | Reconciled; rejects stale component state and protected-property evidence |

## Art review no-change decision

`art-asset-review` already owns the independent quality, provenance, fixed-slot, and target-size composed-screen verdict for file-backed raster, vector, and mixed representations. A code-native or native-widget component classified `ASSET_NOT_REQUIRED` does not produce a file artifact for that reviewer to inspect.

Runtime binding, required-state coverage, protected-property observation, and current-build fingerprint checks remain owned by `game-ui-runtime-validation` and `game-ui-acceptance-review`. Adding those responsibilities to `art-asset-review` would duplicate downstream evidence ownership and weaken its read-only craft-review boundary.

Route a reusable component to `art-asset-review` only when its selected representation produces a file-backed artifact that requires an art-quality verdict. Downstream implementation and acceptance consume `NOT APPLICABLE` only when the packet has no produced or file-backed art; they continue to require `Decision: APPROVE ASSET QUALITY` for every packet that has any such art. Ruling: `art-asset-review` remains unchanged because its existing ownership is complete; the cost of a false no-change decision would be a missing file-backed craft gate, which is prevented by the asset-production route and acceptance-review input contract.

No row is safe for byte-copy reconciliation. Each later edit requires its own no-skill control, focused implementation, forward test, and preservation check.
