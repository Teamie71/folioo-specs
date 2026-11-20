# Folioo-specs

기획 원문은 Notion·Figma·Markdown에서 작성하고, 이 레포는 검토·승인·변경 이력과 원문 연결을 관리합니다.

## 먼저 읽기

1. [공통 조회·작업 지침](AGENTS.md)
2. [현재 업데이트와 과거 참조](registry/updates.json)
3. 해당 업데이트 README·PRD·IA와 기능 README·명세·화면 설명
4. 필요한 공통 정책·결정 기록

## 현재 기획 문서

현재 업데이트: **v.3 (`UPD-003`)** · 등록된 기획 문서: **PRD 1건 (`DOC-001`)**

v.3 기획의 대상은 대학생·취준생이며, 준비 단계별 직무 찾기·경험 정리·포트폴리오 첨삭을 중심으로 구성.

| 바로가기 | 확인할 내용 |
| --- | --- |
| [v.3 개요](updates/UPD-003/README.md) | 대상 사용자·기획 방향·문서 등록 현황 |
| [v.3 PRD](updates/UPD-003/PRD.md) | 문제 정의·개편 전략·타겟·릴리즈 계획·성공 지표 |
| [v.3 변경 범위](updates/UPD-003/changes.md) | 기능별 추가·개편·유지·제거 계획 |
| [원문·수집 정보](updates/UPD-003/manifest.json) | Notion 원문 위치·수집 시점·내용 해시 |

IA·기능별 명세·화면·정책은 미등록 상태이며, 미등록을 폐기로 해석하지 않습니다.

## 위치

### 전체 폴더

아래는 문서 등록 후 사용할 대표 구조입니다. `<UPD-ID>`·`<FEAT-ID>`·`<DEC-ID>`는 실제로 등록할 ID의 자리표시자이며, 예시를 위해 새 ID나 기획 문서를 만들지 않습니다. **등록 시 생성**으로 표시한 경로는 아직 없는 문서의 배치를 안내합니다.

| 경로 | 역할 | 생성 시점 |
| --- | --- | --- |
| `updates/<UPD-ID>/` | 업데이트별 독립 PRD·IA·변경 목록·최종본 목록 | 해당 업데이트 최초 등록 시 |
| `features/<FEAT-ID>/` | 기능별 최신 승인 명세·화면 설명·전용 정책·Figma 연결 | 해당 기능 최초 등록 시 |
| `policies/` | 여러 기능에 적용되는 공통 정책 | 공통 정책 등록 시 |
| `decisions/` | Notion 의사결정 DB의 결정·근거 기록 | 관련 결정 기록 수집 시 |
| `registry/` | 업데이트·기능·화면·문서의 ID와 위치 색인 | 초기 설정에 포함 |

### 업데이트별 문서

기준 경로: `updates/<UPD-ID>/`. 아래 파일은 실제 원문 등록 시 생성하며, `release.json`은 업데이트 최종화 시 준비합니다.

| 하위 경로 | 내용 |
| --- | --- |
| `README.md` | 업데이트 개요와 PRD·IA·대상 기능·정책의 진입점 |
| `PRD.md` | 해당 업데이트의 Notion PRD 수집본 |
| `IA.md` | 해당 업데이트 IA의 텍스트 구조와 Figma 원문 연결 |
| `changes.md` | 기능별 신규·유지·일부 수정·전면 개편·폐기와 관련 문서·PR 목록 |
| `release.json` | 종료 시 확정한 문서·버전·계승 출처와 고정 참조 목록 |
| `manifest.json` | 업데이트 문서의 원문·수집 시점·내용 해시·이전 출처 |

업데이트별 PRD·IA·변경 목록은 해당 폴더에서, 완료 시점의 참조 정보는 `release.json`에서 확인.

### 기능별 문서

기준 경로: `features/<FEAT-ID>/`. 같은 기능은 업데이트가 바뀌어도 ID·경로를 유지합니다.

| 하위 경로 | 내용 |
| --- | --- |
| `README.md` | 기능 개요·상태·관련 명세·화면·정책을 찾는 진입점 |
| `spec.md` | Notion 기능명세서 수집본과 적용 요구사항 |
| `screen-description.md` | 화면 설명·정책·예외와 와이어프레임 요소 ID 참조 |
| `wireframe.json` | 선택한 Figma 파일·페이지·기능 Section·화면 Frame의 위치와 와이어프레임 버전 |
| `elements.json` | 화면 설명에서 참조하는 논리 요소 ID와 Figma 요소의 연결 |
| `manifest.json` | 현재·이전 원문 URL, 내용 해시, 마지막 변경 업데이트, 관련 파일 위치 |
| `policies/<policy-name>.md` | 기능 전용 정책과 명시·승인된 공통 정책 예외. 해당할 때 생성 |
| `assets/` | 필요한 첨부자료. 해당할 때 생성 |

기능별 문서의 버전·계승·원문 연결 기준은 [AGENTS.md](AGENTS.md) 참조.

### 공통 정책과 결정 근거

| 경로 | 내용 | 생성 조건 |
| --- | --- | --- |
| `policies/<policy-name>.md` | 공통 정책의 적용 범위·기준과 관련 기능 연결 | 실제 공통 정책 원문이 있을 때 |
| `decisions/<DEC-ID>.md` | Notion 결정 기록의 결정 내용·이유·실제 자료·적용 대상·대체 관계 | 확인 가능한 결정 기록을 수집할 때 |

공통 정책과 결정 기록의 적용·연결 기준은 [AGENTS.md](AGENTS.md) 참조.

### 색인과 운영 파일

현재 업데이트 색인에 `UPD-003`, 문서 색인에 PRD `DOC-001` 등록 완료. 기능·화면 색인은 해당 상세 문서 미등록으로 빈 목록 유지.

| 경로 | 역할 |
| --- | --- |
| `registry/updates.json` | 현재 업데이트와 업데이트별 문서 위치 색인 |
| `registry/features.json` | 기능 ID·상태·문서 위치 색인 |
| `registry/screens.json` | 화면 ID와 관련 기능·문서 위치 색인 |
| `registry/documents.json` | 논리 문서 ID와 파일 위치 색인 |
| `README.md` | 문서 탐색 순서와 대표 구조 안내 |
| `AGENTS.md` | 조회·기획 검토·문서 관리·버전·커밋·PR·병합의 공통 지침과 PR 양식 |
| `CLAUDE.md` | Claude Code에서 공통 지침을 읽는 진입점 |
| `.coderabbit.yaml` | CodeRabbit 실행 옵션과 AGENTS.md 검토 기준 연결 |
| `.gitignore` | 로컬 임시파일·환경설정 파일 제외 규칙 |

실제 등록된 항목과 문서 위치는 `registry/` 및 해당 업데이트·기능의 README에서 확인.

## 공통 지침

조회·기획 검토·문서 관리·버전·커밋·PR·병합 기준과 PR 양식은 [AGENTS.md](AGENTS.md)에서 관리.
