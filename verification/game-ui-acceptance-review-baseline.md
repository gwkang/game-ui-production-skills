# game-ui-acceptance-review baseline

## Observed baseline

The no-skill response could reject stale evidence yet omit exact fingerprint locking, reviewer independence, complete coverage, severity closure, or a standardized UI-only verdict. Structural correctness could also conceal weak composed-screen art quality.

## Required behavior

The skill must independently lock current evidence, reject stale/partial/substitute inputs and unresolved fidelity gaps, remain read-only, emit an exact UI verdict, and keep broader feature approval separate.

## Forward-test result

PASS. The evaluator rejected stale and incomplete evidence, reopened approval after the font and fidelity changes, enforced reviewer independence and read-only routing, emitted `Decision: REJECT UI`, and did not substitute feature approval.
