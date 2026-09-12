# game-ui-asset-production component reuse pressure run 2

Phase: `GREEN`
Source SHA-256: `5b854b02e8693b0ee77bf9eec0b25ffc843327b6fc0d2349b590efe7446b0a8d`

## Response

DRAFT — asset-production disposition (read-only)

`reward-button-final.png` is rejected for this binding: it changes protected visual properties and omits the required `pressed` state. It cannot replace the approved code-native representation merely to create an atlas asset.

binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog-declared adapter: ui-components/PrimaryButton; evidence capability: runtime-landmark probes m-shadow, m-highlight, m-corner

Rejected proposal: `reward-button-final.png` must not be atlased, recorded as this reuse binding, or sent to implementation as equivalent evidence.

`Next route: game-ui-component-system`

Downstream status: the approved canonical binding remains available as `ASSET_NOT_REQUIRED`; asset production creates no bitmap, raster export, placeholder, atlas entry, transform, hash, bundle delta, or asset-review request. Catalog evidence for both `default` and `pressed` remains required. Rendered fidelity belongs to runtime validation and UI acceptance. Implementation is not blocked by asset bytes, but it may proceed only when its own required handoff/runtime gates are satisfied.

Screen-wide visible art-family/source-parity coverage: **not provided / not assessed**. No source locks, rights, dimensions, hashes, slot geometry, target-size composed-screen evidence, manifest rows, bounds/fit data, bundle budget, or provenance registry evidence was supplied. Those omissions are reported separately and are not fabricated into this binding’s disposition.

## Score

Matrix passed; binding and whole-packet downstream status were not expressed as separate fixed statuses.
