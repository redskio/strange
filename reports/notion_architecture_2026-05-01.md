# 🔮 Notion 워크스페이스 신규 아키텍처 설계 보고서

**기준: 2026-05-01** | 설계자: Doctor Strange | 요청: NICKFURY 분석 기반 구조 재편

---

## 📐 전체 구조 (생성 완료)

```
강의자료 데이터 (Root)
ID: 34895a6a-9ebc-8029-8edb-f479dc541720
│
├── 📁 01. 콘텐츠 허브 — AI 업무자동화 & 데이터분석
│   ID: 35395a6a-9ebc-8160-990e-ef10665181e8
│   URL: https://app.notion.com/p/01-AI-35395a6a9ebc8160990eef10665181e8
│   └── 🗃️ AI 자동화 콘텐츠 아카이브 (DB)
│       DB ID: 35395a6a-9ebc-81d2-82c7-f51f762fbcf1
│       URL: https://app.notion.com/p/35395a6a9ebc81d282c7f51f762fbcf1
│
├── 📁 02. 강의 제작 — AI 유튜브 시리즈
│   ID: 35395a6a-9ebc-8124-aebf-c1da36a4a530
│   URL: https://app.notion.com/p/02-AI-35395a6a9ebc8124aebfc1da36a4a530
│   ├── 📚 완성 강의자료 (01~20강)
│   │   ID: 35395a6a-9ebc-819a-a4f2-d7c4ee804281
│   └── ✏️ 기획 & 초안
│       ID: 35395a6a-9ebc-81fe-9b7d-e0955f88959e
│
├── 📁 03. 프로젝트 — AdMix AI
│   ID: 35395a6a-9ebc-814f-b17e-f58f269610ef
│   URL: https://app.notion.com/p/03-AdMix-AI-35395a6a9ebc814fb17ef58f269610ef
│
├── 📁 04. 운영 — J.A.R.B.I.S. & 시스템
│   ID: 35395a6a-9ebc-81c3-b862-da6b375bff47
│   URL: https://app.notion.com/p/04-J-A-R-B-I-S-35395a6a9ebc81c3b862da6b375bff47
│   ├── 🤖 에이전트 테스트 기록
│   │   ID: 35395a6a-9ebc-81fd-9e08-c8cb80c24a19
│   └── 🗒️ 회의록
│       ID: 35395a6a-9ebc-813a-a5db-e45b6fc6f35d
│
└── 📁 05. 아카이브
    ID: 35395a6a-9ebc-81b4-941a-f41cfe30b3a1
    URL: https://app.notion.com/p/05-35395a6a9ebc81b4941af41cfe30b3a1
    ├── 📊 완료된 리서치
    │   ID: 35395a6a-9ebc-81ec-b6c2-f604a4c76a78
    └── 🗄️ 구버전 자료
        ID: 35395a6a-9ebc-816e-be20-ffb068998855
```

---

## 🗃️ AI 자동화 콘텐츠 아카이브 DB 스펙

| 속성명 | 타입 | 옵션 |
|--------|------|------|
| Title | title | — |
| Platform | select | YouTube / Google / LinkedIn |
| Category | multi_select | 업무자동화 / 데이터분석 / AI툴 / 에이전트 / n8n / LLM / 노코드 |
| Tags | multi_select | 자유 입력 |
| PublishDate | date | — |
| Summary | rich_text | — |
| URL | url | — |
| CollectedAt | date | — |
| Status | select | 신규 / 검토완료 / 강의연계 / 아카이브 |

**워크플로**: 신규 → 검토완료 → 강의연계 → 아카이브

---

## 📋 기존 폴더 → 신규 구조 매핑 가이드

| 기존 폴더 | 이동 위치 | 액션 |
|----------|---------|------|
| 강의 — AI 유튜브 시리즈 | 02. 강의 제작 | 콘텐츠 이관 후 삭제 권장 |
| 리서치 — AI 업무자동화 아카이브 | 05. 아카이브 > 완료된 리서치 | 이관 후 삭제 권장 |
| 회의록 | 04. 운영 > 회의록 | 이관 후 삭제 권장 |
| 에이전트 — J.A.R.B.I.S. 테스트 기록 | 04. 운영 > 에이전트 테스트 기록 | 이관 후 삭제 권장 |
| 프로젝트 — AdMix AI | 03. 프로젝트 | 이관 후 삭제 권장 |

> ⚠️ 기존 폴더 삭제는 재우씨 직접 확인 후 진행 권장 (데이터 손실 방지)

---

## 🔑 PEPPER에게 전달할 DB 접속 정보

```
DB명: AI 자동화 콘텐츠 아카이브
DB ID: 35395a6a-9ebc-81d2-82c7-f51f762fbcf1
부모 페이지: 01. 콘텐츠 허브 (35395a6a-9ebc-8160-990e-ef10665181e8)
Status 초기값: 신규
```

*기준: 2026-05-01 | Doctor Strange Architecture Report*
