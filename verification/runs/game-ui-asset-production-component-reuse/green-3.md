# game-ui-asset-production component reuse pressure run 3

Phase: `GREEN`
Source SHA-256: `5b854b02e8693b0ee77bf9eec0b25ffc843327b6fc0d2349b590efe7446b0a8d`

## Response

`reward-button-final.png`은 승인된 code-native 재사용 바인딩을 대체할 수 없습니다. 아틀라스화·동일 바인딩 기록·pressed 증거 생략은 모두 거절합니다.

Status: `DRAFT` — binding disposition complete; screen-wide art-family parity evidence is not supplied, so it remains `MISSING` and this is not `REVIEW_READY`.

Production mode: `no-new-raster` for this binding. No bitmap, export, placeholder, or atlas entry is produced.

```text
binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog-declared adapter: ui-components/PrimaryButton; evidence capability: runtime-landmark probes m-shadow, m-highlight, m-corner
```

Rejected proposal: `reward-button-final.png` changes the approved representation from `code-native` to raster, changes protected visual properties, and lacks the required `pressed` state evidence.

```text
Next route: game-ui-component-system
```

The valid canonical `ASSET_NOT_REQUIRED` path remains available. Catalog evidence must still verify `m-shadow`, `m-highlight`, `m-corner`, plus both `default` and `pressed` states.

Downstream status: this binding itself is not blocked by asset production; however, implementation must not begin because no screen-wide visible-art-family inventory, source-parity rows, target-size composed-screen evidence, rights/source hashes, or visual QA were provided. Those unknowns are separate from—and must not be fabricated from—the binding disposition.

## Score

Matrix and overall block passed; fixed binding-level and packet-level status labels were absent.
