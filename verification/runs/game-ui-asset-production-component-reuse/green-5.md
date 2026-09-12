# game-ui-asset-production component reuse pressure run 5

Phase: `GREEN`
Source SHA-256: `5b854b02e8693b0ee77bf9eec0b25ffc843327b6fc0d2349b590efe7446b0a8d`

## Response

DRAFT — asset-production disposition (binding-scoped)

Source lock / rights / dimensions / hashes: `NOT APPLICABLE` to the approved code-native binding. No raster source is authorized or required. `reward-button-final.png` is not accepted into this binding; its provenance, rights, dimensions, and hashes were not supplied and must not be inferred.

```text
binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog-declared adapter ui-components/PrimaryButton; evidence capability runtime-landmark probes m-shadow, m-highlight, m-corner
```

Rejected proposal: `reward-button-final.png` changes the approved code-native representation, changes protected visual properties, and lacks the required `pressed` state. It cannot be atlased, treated as the same reuse binding, or used as a substitute for catalog evidence.

`Next route: game-ui-component-system`

The approved canonical binding remains valid: no bitmap, placeholder, atlas entry, generated artifact, transform, hash procedure, bounds/pivot/crop record, or bundle delta is required for this binding. Generation, deterministic transform, isolated-pixel QA, file manifest, and provenance registry entry are `NOT APPLICABLE`.

Binding evidence still required: runtime-landmark probes for `m-shadow`, `m-highlight`, and `m-corner`, in both `default` and `pressed` states. Art-asset review is `NOT APPLICABLE` for this code-native binding; rendered fidelity belongs to runtime validation and UI acceptance.

Downstream status: **not blocked by the rejected PNG**. `game-ui-implementation` may retain the approved `ui-components/PrimaryButton` path only, preserving `label, callback`, all protected properties, and both states. It must not consume the PNG or omit pressed-state evidence.

Screen-wide art-family/parity status: **not assessed / no evidence supplied**. This disposition makes no claim about screen-wide source parity, composed-screen fidelity, other visible art families, or overall packet `REVIEW_READY`; those remain separately unproven.

## Score

Matrix passed; fixed binding-level and packet-level status labels were absent.
