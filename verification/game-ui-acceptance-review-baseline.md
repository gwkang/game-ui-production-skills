# game-ui-acceptance-review baseline

## Observed baseline

The no-skill response could reject stale evidence yet omit exact fingerprint locking, reviewer independence, complete coverage, severity closure, or a standardized UI-only verdict. Structural correctness could also conceal weak composed-screen art quality.

## Required behavior

The skill must independently lock current evidence, reject stale/partial/substitute inputs and unresolved fidelity gaps, remain read-only, emit an exact UI verdict, and keep broader feature approval separate.

## Forward-test result

PASS. The evaluator rejected stale and incomplete evidence, reopened approval after the font and fidelity changes, enforced reviewer independence and read-only routing, emitted `Decision: REJECT UI`, and did not substitute feature approval.

## Component acceptance pressure test

Five no-skill controls rejected stale pressed evidence but varied the verdict token, row shape, severity, copied identity fields, and owner route. The first guided revision stabilized the ten-cell component verdict while exposing evidence-ID delimiter and decision-line drift. The final revision locked raw IDs to comma-space order and separated the exact UI decision token from its rationale. Five fresh final runs rejected aggregate substitution and blocked broader feature review.

### Component RED-1

Rejected stale evidence; no stable matrix or exact UI verdict.

### Component RED-2

Rejected stale evidence; incompatible row and route syntax.

### Component RED-3

Rejected stale evidence; nonstandard UI verdict.

### Component RED-4

Rejected stale evidence; unstable matrix serialization.

### Component RED-5

Rejected stale evidence; incomplete provenance cells.

### Component FINAL-1

PASS: exact ten-cell rejection and runtime-validation route.

### Component FINAL-2

PASS: exact ten-cell rejection and runtime-validation route.

### Component FINAL-3

PASS: exact ten-cell rejection and runtime-validation route.

### Component FINAL-4

PASS: exact ten-cell rejection and runtime-validation route.

### Component FINAL-5

PASS: exact ten-cell rejection and runtime-validation route.

## Final audit reconciliation

PASS: `final-2-no-file-acceptance.md` accepts a complete no-file packet with an independent verdict of `NOT APPLICABLE`; `final-3-file-art-block.md` preserves the required independent art-quality approval for file-backed art.
