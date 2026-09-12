# Publication verification — 2026-09-12

This update publishes the current portable skill source, including component governance and its downstream contracts. Historical pressure-test responses and snapshots are preserved as historical evidence, not rerun results.

## Checks performed for this publication

- All 10 installed skill folders passed the skill frontmatter/scaffold validator.
- All 181 source-package files matched the publication checkout byte for byte before this note was added.
- Markdown relative links resolved within the publication package.
- Project identifiers, personal absolute paths, and common credential markers had no matches in the source-package scan.
- The source workspace's documentation check and 36 UI pipeline tests passed.
- The source workspace's portability suite passed 29 of 30 tests, including component catalog validator coverage. One historical-evidence freshness assertion failed as described below.
- Git whitespace validation passed for skill files and package documentation. The full staged check reports trailing spaces (including Markdown hard breaks) and blank lines at EOF in historical raw responses under `verification/runs/`; those original responses are preserved byte for byte.

## Historical evidence limitation

The current `skills/game-ui-runtime-validation/SKILL.md` SHA-256 is `9728a3f9551bce427ebb2b9ee9a7472b0d3d37889f9433975b5bb712db2d234b`. The final audit reconciliation records cite the earlier `e4e69adbd723200f889e18b3c657b612c4a7344cf3c3c220816ab1ba2e4a2fd1` source. Therefore `test_final_audit_reconciliation_pressure_runs_cover_both_counterexamples` fails its current-source hash assertion.

Those records, including the source audit and baseline reports, do not establish forward-test coverage of the current runtime-validation bytes. No historical source hash or response was rewritten to claim otherwise, and no new independent behavioral run was performed for this publication. Refreshing that evidence remains outstanding; this update does not claim an entirely passing portability suite or certify any game's runtime or release.
