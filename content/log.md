---
title: 작업 기록
tags: [로그, 작업기록]
created: 2026-04-11
updated: 2026-04-27 (오후)
---

# 작업 기록

## 2026-04-11 — 초기 구축

### 배경

초등 교사이자 SW·AI 교육 연구 분과 연구자의 디지털 시민교육 연구 세션(Claude Code + Discord 채널)의 결과물을 Obsidian vault로 정리한다. Plan→Work→Review 하네스 스킬과 Read→Integrate→Verify 위키 스킬을 조합하여, 6개 태스크(T1~T6)를 병렬/순차로 실행했다.

### 생성된 파일 목록 (22개)

**루트 (5개)**
- `CLAUDE.md` — Claude 작업 스키마 (스킬/규칙 정의)
- `README.md` — 사람이 읽는 소개
- `index.md` — 전체 목차·교차 참조 지도 (T6에서 실제 파일에 맞게 재작성)
- `overview.md` — 한 페이지 요약 (T6 신규)
- `log.md` — 작업 기록 (T6 신규)

**concepts/ (3개)**
- `concepts/digital-citizenship.md` — 디지털 시민성 정의·배경·국내외 논의
- `concepts/6-competencies.md` — 디지털윤리.kr 6대 역량 상세
- `concepts/frameworks-comparison.md` — 디지털윤리.kr·Common Sense·S.T.A.R 비교

**papers/ (4개)**
- `papers/index.md` — 논문 목록·비교·연구 흐름
- `papers/2023-papers.md` — 2022~2023년 주요 논문 4편 (이수진·김하연·이상희·척도·카카오임팩트)
- `papers/2024-curriculum-analysis.md` — 도지민·최진영(2024) 교육과정 분석
- `papers/2025-star-project.md` — 김윤하·김미량(2025) S.T.A.R 프로젝트

**resources/ (3개)**
- `resources/digital-ethics-kr.md` — 방통위·KISA 디지털윤리.kr 공식 자료
- `resources/it-supporters.md` — IT서포터즈×디지털시민 저학년 스토리형 자료
- `resources/keris.md` — KERIS 초등 디지털 역량 교육자료

**policy/ (3개)**
- `policy/2022-curriculum.md` — 2022 개정 교육과정과 디지털 소양
- `policy/gyeonggi-edu.md` — 경기도교육청 디지털 시민교육 정책
- `policy/5min-practice.md` — 5분+ 실천 프로그램

**training/ (3개)**
- `training/2hr-overview.md` — 2시간 입문 연수 개요
- `training/15hr-overview.md` — 15시간 직무연수 개요
- `training/lesson-design-tips.md` — 수업 설계 7원칙·차시 구성 템플릿

**synthesis/ (1개)**
- `synthesis/key-insights.md` — 디지털 시민교육 종합 인사이트 7개 (T6 신규)

카테고리별 파일 수: 루트 5 + concepts 3 + papers 4 + resources 3 + policy 3 + training 3 + synthesis 1 = **총 22개 .md 파일**

### 교차 참조 검증 결과

T6 Step 5에서 vault 전체의 `[[wikilink]]`를 추출하여 각 대상 파일의 실존 여부를 확인했다.

**검증 방법**
1. `find ~/디지털시민교육-wiki -name "*.md" | sort`로 실제 파일 목록 확보
2. Grep으로 모든 `[[...]]` 패턴 추출
3. 각 링크 대상을 실제 파일과 대조
4. CLAUDE.md 안의 wikilink 예시는 코드 블록·문법 설명 용도이므로 검증 대상에서 제외

**발견된 Dead Link (수정 전 2건)**

| 위치 | 원본 링크 | 대상 파일 존재? | 조치 |
|------|----------|--------------|------|
| README.md:30 | `[[concepts/digital-citizenship-overview]]` | ✗ 없음 | `[[concepts/digital-citizenship]]`으로 수정 |
| README.md:35 | `[[resources/teaching-materials]]` | ✗ 없음 | `[[resources/digital-ethics-kr]]`으로 수정 |

**수정 후 Dead Link: 0건**

**Orphan Page 검증**

각 파일이 다른 파일에서 최소 1회 이상 링크되는지 확인:

| 파일 | 피링크 출처 |
|------|----------|
| README.md | index.md (T6에서 추가) |
| overview.md | index.md, synthesis/key-insights.md, README.md |
| index.md | README.md, papers/index.md, synthesis/key-insights.md, overview.md |
| CLAUDE.md | README.md, index.md (T6에서 추가) |
| log.md | index.md (T6에서 추가) |
| concepts/digital-citizenship.md | 6-competencies, frameworks-comparison, resources/keris, index, synthesis, README |
| concepts/6-competencies.md | digital-citizenship, frameworks-comparison, policy/2022-curriculum, policy/5min-practice, policy/gyeonggi-edu, papers/2023-papers, resources/digital-ethics-kr, resources/it-supporters, training/2hr-overview, training/lesson-design-tips, index, synthesis, overview, README |
| concepts/frameworks-comparison.md | digital-citizenship, 6-competencies, papers/2025-star-project, index, synthesis, README |
| papers/index.md | index, synthesis |
| papers/2023-papers.md | 2024-curriculum-analysis, policy/2022-curriculum, index, synthesis |
| papers/2024-curriculum-analysis.md | 2023-papers, 2025-star-project, policy/2022-curriculum, papers/index, index, synthesis |
| papers/2025-star-project.md | 6-competencies, frameworks-comparison, 2024-curriculum-analysis, policy/gyeonggi-edu, training/2hr-overview, training/15hr-overview, training/lesson-design-tips, papers/index, index, synthesis, overview, README |
| policy/2022-curriculum.md | digital-citizenship, papers/2023-papers, papers/2024-curriculum-analysis, resources/keris, index, synthesis, overview, README |
| policy/gyeonggi-edu.md | policy/2022-curriculum, policy/5min-practice, index, synthesis, overview, README |
| policy/5min-practice.md | policy/gyeonggi-edu, index, synthesis, README |
| resources/digital-ethics-kr.md | frameworks-comparison, resources/it-supporters, resources/keris, training/2hr-overview, training/15hr-overview, training/lesson-design-tips, index, synthesis, README |
| resources/it-supporters.md | index, synthesis |
| resources/keris.md | policy/2022-curriculum, index, synthesis |
| training/2hr-overview.md | training/15hr-overview, training/lesson-design-tips, resources/digital-ethics-kr, resources/it-supporters, papers/2025-star-project, index, synthesis, overview, README |
| training/15hr-overview.md | training/2hr-overview, training/lesson-design-tips, index, synthesis, overview |
| training/lesson-design-tips.md | training/2hr-overview, training/15hr-overview, resources/digital-ethics-kr, policy/5min-practice, papers/2025-star-project, index, synthesis |
| synthesis/key-insights.md | index, overview |

**Orphan Page: 0건**

### 최종 검증 결과

- 총 .md 파일 수: **22개** (목표 22+ 달성)
- Dead links: **0건** (수정 전 2 → 수정 후 0)
- Orphan pages: **0건**
- synthesis/key-insights.md: 7개 인사이트 + 남은 질문 6개 + 19개 근거 페이지 교차 인용
- overview.md: 6개 섹션 한 페이지 요약 + 주요 페이지 링크
- 모든 링크가 실제 존재 파일을 가리키고, 모든 파일이 최소 1개 이상의 다른 파일에서 참조됨

### 향후 추가 예정

synthesis/key-insights.md의 "남은 질문" 섹션에서 식별된 추가 조사 주제:

1. **장기 추적 연구** — S.T.A.R 20차시 이후 6개월·1년 추적 연구
2. **중학년(3~4학년) 전용 자료 보완** — 저학년 스토리형과 고학년 프로젝트형 사이의 공백
3. **타 시도교육청 정책 비교** — 서울·부산·인천·세종 등 2025년 기준 비교
4. **학부모·가정 연계 프로그램** — 학교 밖 디지털 시민교육 소스 수집
5. **AI 리터러시와의 접점** — 2026년 생성형 AI 맥락에서 6역량/S.T.A.R 재해석
6. **교사 연수 효과성 실증 연구** — 국내 연수 참여 후 교사 역량 변화 실증 자료

위 주제 중 하나라도 새 소스가 확보되면 Read→Integrate→Verify 위키 스킬로 vault에 재통합한다.

---

## 관련 문서

- [[index]] — 전체 목차
- [[overview]] — 한 페이지 요약
- [[synthesis/key-insights]] — 종합 인사이트

---

## 2026-04-27 — 2025 디지털 시민교육 기본 계획 통합

### 소스

- 파일: `~/Downloads/2025 디지털 시민교육 기본 계획.pdf` (38쪽, A4, 1.4MB)
- 발행: 경기도교육청 미래교육담당관 (2025.1.)
- 부제: "디지털 시민역량과 디지털 창의역량 신장"

### 작업 내용

1. **신규 페이지**: `policy/2025-gyeonggi-plan.md` 생성
   - 38쪽 전체를 5개 섹션(I.근거~V.기대효과)+참고1~5로 구조화
   - 2024 → 2025 변화표, 인성 기반 6대 역량 영역, 3대 추진 전략(교육과정/맞춤형/현장확산), 실천학교 4종 사업, 신설사항 표 포함
2. **기존 페이지 갱신**:
   - `policy/gyeonggi-edu.md`: 후속 계획 안내 callout + 관련 문서 링크 추가
   - `policy/5min-practice.md`: 2025 확장 callout(생성형 AI 윤리교육 5분+ 실천자료 신설) + 관련 문서 링크 추가
   - `index.md`: 정책 목록·교차 참조 지도·최근 업데이트 갱신

### 주요 인사이트 (Verify 단계 발견)

1. **6대 역량 분류 갱신** — 기존 `concepts/6-competencies.md`(정체성·웰빙·권리책임·소통·정보리터러시·사회참여)와
   2025년판의 "인성 기반 6대 영역(기기SW활용·정보활용생성·의사소통문제해결·윤리안전·사회참여·가치창출)"이 다름.
   경기도교육연구원 2024 연구로 재구조화된 것이며, 두 분류 체계의 매핑이 필요함.
   → 향후 작업: `concepts/6-competencies.md` 보강 또는 신규 `concepts/gyeonggi-6-domains.md` 작성 검토.
2. **디지털 창의역량의 별도 트랙화** — 2024년판에는 없던 신설 트랙. [[papers/2025-star-project|S.T.A.R]]이 강조한
   시민성+리터러시 통합을 정책화한 것으로 해석 가능.
3. **인정도서 2종 + 교과서 26.3 예정** — 초4 「미래를 여는 디지털 시민」(29차시), 중1~3 「슬기로운 인공지능 윤리생활」(32차시).
   초6/고 디지털 시민교육 교과서 + 초6/고 인공지능 윤리교육 교과서 26.3 보급 예정.

### 후속 검토 과제

- [ ] `concepts/6-competencies.md`에 경기형 6대 영역 매핑 표 추가
- [ ] `synthesis/key-insights.md`에 2025년 신설 트랙(창의역량) 시사점 반영
- [ ] 인정도서 2종 실물·실 사용 사례 확보 시 `resources/`에 별도 페이지 추가

---

## 2026-04-27 (오후) — 사우초 2학년 15차시 통합 패키지 통합

### 소스

- 폴더: `~/Downloads/____2___________________/` (한글 폴더명, 시스템에서 언더스코어 표시)
- 자료: 사우초등학교 디지털 시민창의역량교육 2학년 15차시
- 구성: PPTX 9개 + hwpx 활동지 7개 + pdf 활동지 1개 + 통합 zip + 글꼴 폴더(강원교육·경기천년체)
- 자료 작성일: 2025.11.10

### 작업 내용

1. **신규 페이지**: `resources/sauwoo-grade2-package.md` 생성
   - PPT 9블록 = **총 15차시** 분량 (1·4·7차시는 1차시, 나머지는 2차시 블록)
   - 9개 단원 모두 [[policy/2025-gyeonggi-plan|2025 경기형 6대 영역]]에 1:1 매핑됨을 확인하고 표로 정리
   - 차시별 상세(학습 목표·활동 흐름·도구·운영 옵션) 작성
   - 저학년 수업 설계 7패턴 추출 (영상동기·초성퀴즈·놀이·만들기도안·체험도구·블록옵션·점진확장)
   - 활용 시나리오 3종(자율시간 통째 / 창체+교과 분산 / 동학년 공동), 운영 유의사항 5가지 정리
2. **기존 페이지 갱신**:
   - `index.md`: resources 표·교차참조 지도·최근 업데이트 갱신
   - `resources/it-supporters.md`: 관련 문서에 사우초 패키지 링크 추가, updated 갱신
   - `synthesis/key-insights.md` #6: 2026-04-27 업데이트 callout 추가

### 인사이트 (Verify 단계)

1. **저학년 학기 단위 통합 모델 첫 확보** — vault `synthesis/key-insights.md` #6에서 지적한
   "저학년 스토리형(2차시) ↔ 고학년 프로젝트형(20차시) 사이의 자료 공백"이 일부 메워졌다.
2. **6대 영역 1:1 매핑 검증** — 1차시(영역1) → 2-3(영역1) → 4(영역2) → 5-6(영역2) → 7(영역3) →
   8-9(영역3+4) → 10-11(영역4) → 12-13(영역5) → 14-15(영역6) 순으로 진행되어 학기 흐름과 역량 누적이 일치한다.
3. **4-7차시의 중요한 사전 단계 의미** — 4차시 「소리없는 협동화」는 3-4학년의 자료 활용·생성으로,
   7차시 「규칙 찾기」는 3-4학년의 규칙성 설명/코딩 학습으로 이어지는 명확한 사전 단계로 설계됨.
4. **저학년 디지털 도구**: AR 색칠놀이(5-6차시), 오토드로우(14-15차시) 등 진입 장벽이 낮은 도구만 선별 사용.

### 후속 검토 과제

- [ ] 사우초 외 다른 저학년 학기 단위 통합 패키지 추가 수집 (1학년·3학년 분량)
- [ ] 본 패키지의 14-15차시 오토드로우 활용을 [[concepts/6-competencies]]의 "디지털 가치 창출" 항목 사례로 보강
- [ ] 영상 외부 링크 누락 여부 점검 (장기적으로 깨질 가능성)

---

## 2026-04-27 (저녁) — 2학년 담임 한정 2시간 연수 강의안 작성

### 배경

사용자(초등 교사)가 2학년 담임 10명 이내 대상 2시간 연수를 준비. 사용자 요구사항 단계별 협의:
1. 강의 + 휴대폰 개별 실습 (모둠·시연·발표 없음)
2. 자료 배포는 연수 후 이메일 발송 (당일 다운로드 부담 최소화)
3. 도입은 강사 자기소개·일화로, 마무리 단계 없이 자연 종료
4. 휴대폰 실습은 AI 윤리 트랙으로 — 사우초 자료 안의 외부 자원 전수 조사 결과 적합한 웹사이트 부재(와그작 앱은 설치 부담)
5. 활동 3개로 확장 — Quick,Draw! (5') + Crayon (7') + Which Face Is Real? (10') + 토론 (9')

### 작업 내용

1. **신규 페이지**: `training/2hr-grade2-sauwoo.md` (약 380줄)
   - 10단계 시간표 (도입·필요성·개념·정책·자료·실습3종·토론·마무리)
   - 단계별 상세 강의안 — 슬라이드 32장 권장 구성, 강사 멘트 예시, 발문, 데이터 출처 명시
   - 사용자 요구로 **AI 기술 발전 타임라인(2022 ChatGPT → 2024 Sora·딥페이크 사건 → 2026 현재)** 포함
   - 부록 A: 강사 진행 체크리스트 / 부록 B: 슬라이드 32장 빠른 목록 / 부록 C: vault 내 참조 페이지
   - QnA 예상 질문 5개 + 답변 가이드
2. **기존 페이지 갱신**:
   - `training/2hr-overview.md`: 플랜 E로 등록
   - `index.md`: training 표·최근 업데이트 갱신

### 사우초 자료 외부 자원 전수조사 (작업 부산물)

PPTX 9개에서 모든 외부 URL/앱 추출 결과:
- YouTube 영상: 14편 (각 차시 동기유발용)
- AR 색칠놀이 앱: 「와그작(Wazgak)」 — 5-6차시 (Google Play 설치 필요)
- 웹 도구: 「오토드로우(autodraw.com)」 — 14-15차시
- 즉, **사우초 자료 안에서 휴대폰 즉석 체험 가능한 웹사이트는 오토드로우가 유일**.
- 따라서 본 연수의 실습 3개는 사우초 외 외부 자원으로 구성 (Quick,Draw! / Crayon / Which Face Is Real?).

### 인사이트

1. **사우초 자료의 4.2 AI 윤리 공백** — 2-3차시 슬라이드 45에 딥페이크 영상 링크가 들어있긴 하지만 윤리적 학습으로 이어지지 않음. 본 연수가 이 공백을 보강하는 형태로 설계됨.
2. **AI 인식 → 생성 → 윤리 3단계 스토리** — 실습 3개가 단계별로 메시지를 누적해 강의 후반부의 일관된 흐름 형성.
3. **저학년 담임에게 직접 적용 가능한 자료 vs 교사 인지용 자료를 구분** — Quick,Draw!는 학생 직접 사용 가능, Crayon·Which Face Is Real?은 강사 시연용으로 운영 권장.

### 후속 검토 과제

- [ ] 연수 운영 후 청중 피드백 수집해 `training/2hr-grade2-sauwoo.md` 보강
- [ ] 슬라이드 32장 실제 PPT/Keynote 파일 작성 (vault에는 강의안만 보관)
- [ ] 다른 학년(1·3·4·5·6) 담임 대상 연수 변형 작성 가능성 검토
- [ ] Crayon이 craiyon.com에서 도메인 또는 정책 변경 시 대체 도구 (예: Bing Image Creator, Pollinations 등) 후보 확보
