# game-ui-asset-production component reuse pressure run 4

Phase: `GREEN`
Source SHA-256: `5b854b02e8693b0ee77bf9eec0b25ffc843327b6fc0d2349b590efe7446b0a8d`

## Response

`DRAFT — Component production disposition`

`binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence`  
`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; adapter ui-components/PrimaryButton; catalog evidence capability runtime-landmark probes m-shadow, m-highlight, m-corner`

Disposition: no image, atlas entry, transform, hash, or bundle delta is produced for this binding. Generation record, deterministic transform/hash procedure, intrinsic bounds, pixel QA, source parity manifest, provenance entry, and asset-review verdict are `NOT APPLICABLE` to this code-native component.

Rejected proposal: `reward-button-final.png` cannot be recorded as this reuse binding: it replaces the approved code-native representation and lacks the required `pressed` state. The time spent exporting it and release timing do not alter the catalog contract.

`Next route: game-ui-component-system`

The approved canonical `ASSET_NOT_REQUIRED` path remains valid. Downstream: `game-ui-implementation` may proceed only with `ui-components/PrimaryButton` under the approved binding; it must retain both required states and validate the catalog landmark probes at runtime. The rejected PNG is excluded.

Screen-wide art-family fidelity/source-parity status: `NOT ASSESSED` — no screen-wide family inventory, approved mockup comparison, target-size composed-screen evidence, source hashes, or runtime-byte parity evidence was provided. This is separate from, and does not convert, the reusable code-native binding into asset production.

## Score

Matrix passed; whole-packet implementation block remained implicit.
