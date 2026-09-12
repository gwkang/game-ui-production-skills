# game-ui-asset-production component reuse pressure run 1

Phase: `GREEN`
Source SHA-256: `5b854b02e8693b0ee77bf9eec0b25ffc843327b6fc0d2349b590efe7446b0a8d`

## Response

DRAFT — asset-readiness packet (reusable binding only)

- Production mode: `no-new-raster`.
- Approved source lock: `catalog-abc`, `code-native`, adapter/source `ui-components/PrimaryButton`.
- Rights, dimensions, hashes, bundle budget, runtime asset locations, provenance registry entry, and screen-wide art-family inputs: not supplied; no bytes are produced or changed for this binding.
- Generation record: `NOT APPLICABLE`.
- Deterministic transform/hash procedure: `NOT APPLICABLE`.
- Asset manifest, intrinsic/visible bounds, padding, pivot, crop safety, stretch region, fit mode, isolated-pixel QA, bundle impact, and art provenance: `NOT APPLICABLE` for this code-native binding.
- Required catalog evidence remains: runtime-landmark probes `m-shadow`, `m-highlight`, `m-corner`.
- Required rendered states remain: `default, pressed`.
- Independent `art-asset-review`: `NOT APPLICABLE` for this binding. Runtime validation and UI acceptance must verify rendered fidelity and both states.

Component production disposition matrix:

```text
binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog-declared adapter ui-components/PrimaryButton; runtime-landmark probes m-shadow, m-highlight, m-corner
```

Rejected proposal: `reward-button-final.png` is not eligible for this binding. It changes the approved code-native representation through a raster export and supplies only `default`, leaving required `pressed` uncovered. It must not be atlased, recorded as the same reuse binding, or passed to implementation.

```text
Next route: game-ui-component-system
```

Downstream status:

- The approved canonical binding remains `ASSET_NOT_REQUIRED`; it is not blocked by rejecting the PNG proposal.
- `game-ui-implementation` may consume only the unchanged approved binding after catalog evidence and runtime validation cover `default` and `pressed`.
- This packet is not `REVIEW_READY`: no screen-wide visible-art-family inventory, source-parity rows, composed-screen evidence, or art-family QA was supplied. Those screen-wide families are `NOT ASSESSED / evidence not supplied`, not invented or inferred from this reusable binding.

## Score

Matrix passed; downstream sequencing was ambiguous because runtime validation was stated as preceding implementation.
