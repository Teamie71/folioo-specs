# Folioo 기획 문서

**업데이트별 전체 계획과 기능별 상세 명세를 나누어 관리하는 레포.**

원문 작성은 Notion·Figma·Markdown, 검토·승인본과 변경 이력 관리는 GitHub에서 진행.

**현재 등록: v.3 PRD 1건** · [PRD 읽기](updates/UPD-003/PRD.md) · [v.3 개요](updates/UPD-003/update-overview.md) · [변경 범위](updates/UPD-003/changes.md)

## 관리 구조

업데이트마다 PRD·IA를 따로 보관하고, 같은 기능의 상세 문서는 업데이트가 바뀌어도 같은 기능 폴더에서 관리. 업데이트 문서에서 이번에 다루는 기능을 연결하는 구조.

| 관리 단위 | 경로 | 담는 내용 | 현재 상태 |
| --- | --- | --- | --- |
| 업데이트별 계획 | `updates/<UPD-ID>/` | 해당 업데이트의 PRD·IA·기능별 변경 목록·최종본 참조 | v.3 (`UPD-003`) 등록 |
| 기능별 상세 | `features/<FEAT-ID>/` | 기능명세·화면 설명·Figma 와이어프레임 연결·기능 전용 정책 | 기능 문서 등록 시 생성 |
| 공통 정책 | `policies/` | 여러 기능에 공통으로 적용되는 정책 | 정책서 등록 시 생성 |
| 결정 근거 | `decisions/` | Notion 의사결정 기록과 관련 기능·화면·문서 연결 | 결정 기록 등록 시 생성 |
| 문서 색인 | `registry/` | 업데이트·기능·화면·문서 ID와 실제 파일 위치 | 업데이트·PRD 등록, 기능·화면 목록은 비어 있음 |

```mermaid
flowchart TD
    U["updates/ · 업데이트 계획"] -->|대상 기능 참조| F["features/ · 기능별 상세"]
    P["policies/ · 공통 정책"] -->|적용| F
    D["decisions/ · 결정 근거"] -->|근거 연결| U
    D -->|근거 연결| F
    R["registry/ · ID와 위치"] -->|찾기| U
    R -->|찾기| F
```

위 도식은 문서 간 연결 관계. 아직 등록되지 않은 기능·정책·결정 문서는 실제 자료를 등록할 때 생성.

## 현재 폴더와 파일

현재 존재하는 경로만 표시. IA·기능명세·화면 설명·정책서는 아직 미등록.

- **[updates/](updates/)** — 업데이트별 계획
    - **[UPD-003/](updates/UPD-003/)** — 제품 업데이트 v.3
        - [update-overview.md](updates/UPD-003/update-overview.md) — v.3 개요·문서 등록 현황
        - [PRD.md](updates/UPD-003/PRD.md) — v.3 전체 기획 (`DOC-001`)
        - [changes.md](updates/UPD-003/changes.md) — 기능별 추가·개편·유지·제거 계획
        - [manifest.json](updates/UPD-003/manifest.json) — 원문 URL·수집 시점·내용 해시
- **[registry/](registry/)** — ID로 문서를 찾는 색인
    - [updates.json](registry/updates.json) — 현재 업데이트와 업데이트별 위치
    - [documents.json](registry/documents.json) — 문서 ID와 파일 위치
    - [features.json](registry/features.json) — 기능 ID와 위치, 현재 빈 목록
    - [screens.json](registry/screens.json) — 화면 ID와 위치, 현재 빈 목록
- **README.md** — 레포 관리 구조와 문서 탐색 안내, 현재 문서
- **[AGENTS.md](AGENTS.md)** — 조회·문서 관리·검토·커밋·PR의 공통 지침과 양식
- **[CLAUDE.md](CLAUDE.md)** — Claude Code에서 AGENTS.md를 읽는 연결 파일
- **[.coderabbit.yaml](.coderabbit.yaml)** — CodeRabbit 설정
- **[.gitignore](.gitignore)** — 로컬 임시파일·환경설정 파일 제외 설정

## 다음 업데이트와 과거 문서

- 새 업데이트: `updates/<새 UPD-ID>/`에 독립 PRD·IA·변경 목록 보관. 이미 등록된 이전 업데이트의 계획 문서도 같은 위치에 보존.
- 같은 기능의 유지·수정: `features/<같은 FEAT-ID>/`의 문서 계승·갱신. 업데이트의 변경 목록에서 신규·유지·일부 수정·전면 개편·폐기와 대상 문서 연결.
- 과거 최종본: 업데이트 완료 시 `release.json`에 확정한 참조와 고정 태그·승인 커밋으로 당시 기능·정책 조회.

등록·버전·계승·승인·PR 작성의 상세 기준은 [AGENTS.md](AGENTS.md) 참조.

<details>
<summary>문서를 추가할 때의 상세 파일 배치</summary>

아래는 등록 후 사용할 배치. `<UPD-ID>`·`<FEAT-ID>`·`<DEC-ID>`는 자리표시자이며 실제 등록된 ID로 대체.

### 업데이트 폴더: updates/&lt;UPD-ID&gt;/

| 파일 | 내용 |
| --- | --- |
| `update-overview.md` | 업데이트 개요와 관련 문서 진입점 |
| `PRD.md` | 업데이트 전체 기획 |
| `IA.md` | IA 텍스트 구조와 Figma 원문 연결, IA 등록 시 생성 |
| `changes.md` | 기능별 변경·계승 범위와 관련 문서·PR |
| `manifest.json` | 업데이트 문서의 원문·수집 정보 |
| `release.json` | 완료 시 확정한 문서·버전·계승 출처·고정 참조 |

### 기능 폴더: features/&lt;FEAT-ID&gt;/

| 파일 | 내용 |
| --- | --- |
| `feature-overview.md` | 기능 개요와 관련 명세·화면·정책 진입점 |
| `spec.md` | 기능명세서와 적용 요구사항 |
| `screen-description.md` | 화면 설명·정책·예외와 화면요소 ID 참조 |
| `wireframe.json` | 선택한 Figma 파일·페이지·기능 Section·화면 Frame과 버전 |
| `elements.json` | 화면 설명에서 참조하는 요소 ID와 Figma 요소 연결 |
| `manifest.json` | 원문 URL·내용 해시·마지막 변경 업데이트·관련 파일 위치 |
| `policies/<policy-name>.md` | 기능 전용 정책, 해당 정책 등록 시 생성 |
| `assets/` | 필요한 첨부자료가 있을 때 생성 |

### 공통 문서

| 경로 | 내용 |
| --- | --- |
| `policies/<policy-name>.md` | 여러 기능이 함께 참조하는 공통 정책 |
| `decisions/<DEC-ID>.md` | 결정 내용·이유·근거 자료·적용 대상·대체 관계 |

</details>
