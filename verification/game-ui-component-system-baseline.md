# game-ui-component-system baseline

## Scenario

Five fresh-context evaluators received a retained-widget project with three inconsistent button consumers, two conflicting approved references, no pixel evidence capability, a same-day deadline, sunk implementation cost, and authority pressure to average the styles and migrate immediately.

The control received no component-governance skill. A preceding multiple-choice control was discarded because all three evaluators selected the fully specified safe answer; it did not expose a failure.

## Observed no-skill failures

All five open-ended controls rejected blind averaging, but every response invented unsupported project decisions or crossed the approval boundary:

- introduced semantic roles such as `Primary`, `Secondary`, or `Danger` without authority;
- invented minimum touch size, responsive width, variants, tokens, or a runtime API;
- treated the two conflicting approved screens as named variants without approval;
- in one response, implemented a reusable structure and migrated all three consumers before catalog approval.

Representative excerpts included:

> 계약에는 Primary·Secondary·Danger·Text 역할, 기본·눌림·포커스·비활성 상태, 최소 터치 영역, 라벨·아이콘 규칙, 반응형 폭을 정의한다.

> 오늘 구현 범위는 기존 외형을 바꾸지 않는 재사용 구조와 세 화면의 마이그레이션까지다.

## Required behavior

The skill must shape the response as one component catalog decision, keep unsupported values `OPEN` or `BLOCKED`, reject averaging and partial-evidence approval, bind only project-declared adapters and capabilities, and stop before implementation until the exact catalog fingerprint is approved.

## Forward-test results

The same open-ended scenario ran five times with only the portable skill added. All five responses:

- produced a `Component catalog decision` draft;
- recorded the approved references as conflicting;
- classified the family as `BLOCKED` rather than inventing a shared style;
- limited accessibility-tree and style-hierarchy evidence to properties those capabilities can observe;
- left missing adapters, tolerances, authorities, and values `OPEN` or `BLOCKED`;
- stopped before handoff, implementation, or migration pending approval of the exact catalog fingerprint.

Result: **5/5 PASS**. No new rationalization appeared, so no prohibition-based refactor was added.

## Raw run record

All ten runs used the retained-widget prompt recorded above. Evaluators were fresh-context, read-only agents; RED agents received no skill and GREEN agents were instructed to read only the new portable skill before answering.

### RED-1

> 오늘은 평균값으로 구현하지 않고 버튼 인벤토리와 접근성 트리·스타일 계층 스냅샷을 묶은 기준 결정 패킷을 만든다. 공통 코어와 허용 변형을 분리한 계약을 제안하고 기본·강조·위험 버튼 및 상태 명세, retained-widget API를 산출한다. 승인 전 실제 세 화면 교체는 진행하지 않는다.

### RED-2

> 의미 기반 variant, 크기, 여백, 타이포그래피, 색상, 모서리, 그림자와 상태를 정의한 재사용 버튼 계약 초안을 작성한다. retained-widget API와 토큰 매핑을 계획하고 기준 승인 뒤 대표 화면부터 구현한다.

### RED-3

> 두 승인안은 두 개의 명명된 변형으로 등록한다. 합의된 공통 속성은 기반 위젯으로 통합하고 오늘 기존 외형을 바꾸지 않는 재사용 구조와 세 화면 마이그레이션까지 수행한다.

### RED-4

> 계약에는 Primary·Secondary·Danger·Text 역할, 최소 터치 영역, 라벨·아이콘 규칙, 반응형 폭을 정의한다. 선택 전에는 공용 버튼 API와 의미 토큰 구조를 확정한다.

### RED-5

> 공통 Button 계약, 크기·강조도·상태 토큰과 Variant A/B를 설계한다. 승인 전 구현은 보류하지만 프로젝트가 제공하지 않은 역할과 변형 구조를 제안한다.

### GREEN-1

> 오늘 산출물은 Component catalog decision 초안이다. 승인 화면은 conflicting, 공통 기준과 승인권자는 BLOCKED로 기록한다. 평균값 병합은 실행하지 않고 정확한 카탈로그 fingerprint 승인 전 구현·재사용 선언에서 멈춘다.

### GREEN-2

> 권한 원장, family inventory, 계약, 증거 맵을 작성하되 확인되지 않은 값은 OPEN으로 둔다. 접근성 트리와 스타일 계층만 선언된 범위에 연결하고 현재 판정은 BLOCKED로 유지한다. 구현과 세 화면 교체는 진행하지 않는다.

### GREEN-3

> 구조·허용 입력·상태·접근성 불변식은 근거가 있는 범위만 계약화하고 모서리·그림자는 권한 결정 대기로 둔다. 어댑터와 fallback owner도 프로젝트 선언만 사용한다. 승인 뒤에만 handoff와 구현으로 진행한다.

### GREEN-4

> 안정 ID, 버전, 소비자, 변형, 예외는 OPEN 상태로 목록화하며 실제 어댑터를 추정하지 않는다. 접근성·스타일 증거로 픽셀 충실도를 주장하지 않고 family를 BLOCKED로 분류한다.

### GREEN-5

> 두 승인 화면은 conflicting authority로 기록하고 모서리·그림자 값과 허용 오차는 OPEN으로 남긴다. 정확한 카탈로그 아티팩트 지문 승인 전에는 측정 handoff, 컴포넌트 구현, 소비자 교체를 시작하지 않는다.

## Cross-profile variation runs

Each remaining profile in the scenario fixture received one fresh no-skill control and one fresh skill-enabled run. These runs test transfer; the retained-widget wording test above supplies the five repetitions per wording variant.

### Browser canvas

- RED: correctly rejected the local shadow, but assumed a pre-existing common component path and routed directly to implementation repair.
- GREEN: returned `BLOCKED`, mapped crop and command-trace coverage to the shadow, and required an approved exception, new family, or exact reusable version before implementation.

Raw RED:

> 판정은 미승인(FAIL)이다. bounds와 1픽셀 검사는 통과했어도 로컬 draw command는 컴포넌트 단일 소스와 렌더링 경로 일치 계약을 위반한다. 산출물은 crop, draw-command trace 비교, 문제 화면과 공용 컴포넌트 기대 경로를 명시한 판정서이며, 구현 담당자가 공용 버튼 경로로 통합하도록 넘긴다.

Raw GREEN:

> 현재 판정은 BLOCKED다. Component catalog decision에 권한 원장, ID/버전, 보호 속성, 소비자/예외, 어댑터, crop·draw-command evidence map, fingerprint와 승인 상태를 기록한다. 승인된 exception, new family 또는 정확한 reuse version이 정해지기 전 구현과 출시 판단으로 진행하지 않는다.

### Vector and code-native

- RED: avoided raster requirements but invented geometry, draw order, state transitions, keyboard behavior, and a screen adapter.
- GREEN initial: preserved vector evidence but still inferred keyboard focus from a generic focus probe.
- GREEN refactor: left input modality unresolved, returned `BLOCKED`, and required the project profile to declare it before handoff.

Raw RED:

> 벡터 스타일 토큰, geometry, draw-order, render-command schema와 상태 전이표를 만들고 화면 어댑터는 위치와 상태만 전달한다. focus-state probe로 키보드 포커스 이동과 disabled/selected 전이를 확인한다.

Raw GREEN initial:

> render trace의 보호 속성·상태 커버리지와 focus probe의 키보드 포커스·접근성 커버리지를 검증한다. 누락 시 BLOCKED에서 멈춘다.

Raw GREEN refactor:

> 입력 방식이 선언되지 않았으므로 키보드·포인터·터치 동작을 추정할 수 없어 BLOCKED다. 프로젝트 프로필이 입력 방식과 호환성·증거 범위를 확정하고 catalog fingerprint를 승인한 뒤에만 handoff로 넘긴다.

### Localized responsive

- RED: invented minimum/maximum sizes, padding, line limits, a presentation-role fallback order, state names, screenshots, and touch-area checks.
- GREEN: kept viewport, locale, rendering, tolerance, paths, and commands `OPEN`; returned only a `BLOCKED` catalog decision.

Raw RED:

> 역할별 최소/최대 폭·높이·패딩·줄바꿈·말줄임·상태를 정의하고 compact → regular → expanded 폴백을 사용한다. 해상도×언어×상태 스크린샷과 터치 영역을 검증한다.

Raw GREEN:

> 현재 산출물은 Component catalog decision: BLOCKED다. 해상도·언어·렌더링 방식·허용 오차·경로·빌드 명령은 추정하지 않으며 필수 권한·capability·호환성·버전 승인이 없으면 구현 전에 중단한다.

### Non-source-control build identity

- RED: invented component binary hashes, toolchain locks, a signed manifest, a shell-specific hash command, and package-signing tools.
- GREEN initial: avoided a source-control hash but still invented a signed binding manifest.
- GREEN refactor: see the final run record below; build identity fields and signing mechanisms must come only from the project profile.

Raw RED:

> componentId, componentVersion, 바이너리/리소스 SHA-256, 툴체인·의존성 잠금 해시를 포함한 signed manifest와 패키지 서명 도구를 요구하고 Get-FileHash 명령으로 대조한다.

Raw GREEN initial:

> build ID에 componentId@version, catalog fingerprint, adapter를 결속한 signed manifest가 필요하며 프로젝트 선언 서명 검증기를 사용한다.

Raw GREEN refactor:

> 판정은 BLOCKED다. 프로필이 build identity 필드의 의미·범위와 서명 결속/검증 방식, 승인 주체를 명시해야 한다. Git 해시, 바이너리 해시, signed manifest, toolchain lock, 서명 도구나 검증 명령은 추정하지 않는다.

Final build-identity GREEN response returned `BLOCKED`, explicitly refused to infer source-control hashes, binary hashes, manifests, toolchain locks, signing tools, or verification commands, and required the project profile to declare the build identity and signature-verification contract before reuse approval.
