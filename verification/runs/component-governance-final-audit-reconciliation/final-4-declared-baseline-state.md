# Final audit reconciliation 4

Phase: `FINAL_AUDIT_RECONCILIATION`
Skill: `game-ui-runtime-validation`
Source SHA-256: `e4e69adbd723200f889e18b3c657b612c4a7344cf3c3c220816ab1ba2e4a2fd1`
Scenario: required states `idle, unavailable`; screen-spec baseline `idle`; exact current-build evidence supplied.

## Response

Component runtime evidence matrix
binding | catalog artifact fingerprint | build fingerprint | consumer | declared adapter | viewport | required state | protected-property evidence | runtime evidence IDs | coverage status
reuse:status-chip@1.0.0 | catalog-idle-1 | build-900 | profile-screen | native/StatusChip | 390x844 | idle | tone:m-tone; spacing:m-spacing | cap-idle-390 | VERIFIED
reuse:status-chip@1.0.0 | catalog-idle-1 | build-900 | profile-screen | native/StatusChip | 320x568 | idle | tone:m-tone; spacing:m-spacing | cap-idle-320 | VERIFIED
reuse:status-chip@1.0.0 | catalog-idle-1 | build-900 | profile-screen | native/StatusChip | 390x844 | unavailable | tone:m-tone; spacing:m-spacing | cap-unavailable-390 | VERIFIED

Next route: game-ui-acceptance-review

## Score

PASS: covers the declared baseline at both targets and never invents `default`.
