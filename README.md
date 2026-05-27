# 5·18 공식 기념 연설의 담론 구조 비교: 이행기정의 담론의 정권별 분화

**Discourse Structure Comparison of Official May 18 Commemorative Addresses: Regime-Based Divergence in Transitional Justice Discourse**

---

## 개요 / Overview

이 리포지토리는 《기억과 전망》 55호 게재 확정 논문 "5·18 공식 기념 연설의 담론 구조 비교: 이행기정의 담론의 정권별 분화"의 분석에 사용된 코퍼스 데이터와 분석 결과 파일을 공개합니다.

This repository provides the corpus data and analysis outputs accompanying the paper "Discourse Structure Comparison of Official May 18 Commemorative Addresses: Regime-Based Divergence in Transitional Justice Discourse," accepted for publication in *Memory and Vision* (기억과 전망), No. 55.

1997년부터 2025년까지 5·18 광주민주화운동 기념식에서 발화된 공식 기념연설 코퍼스(28편, 1,179문장)를 분석 대상으로 하며, 사죄(T1)·용서(T2)·화해(T3)·정의/진상규명(T4)·치유/회복(T5)·기억/계승(T6)·역사의식(T7)의 7개 주제 범주로 코딩하여, 한국 공식 기념 담론에서 사죄-용서-화해의 규범적 연쇄가 구조적으로 단절되어 있음을 실증합니다.

The corpus comprises 28 official commemorative addresses delivered at the May 18 Gwangju Uprising commemorations (1997–2025), totaling 1,179 sentences. Sentences are coded into seven thematic categories (T1–T7) covering apology, forgiveness, reconciliation, justice/truth-seeking, healing/recovery, memory/commemoration, and historical consciousness. The analysis demonstrates that the normative apology-forgiveness-reconciliation chain has been structurally severed in South Korea's official commemorative discourse, with asymmetric patterns across conservative and progressive administrations.

---

## 논문 정보 / Paper Information

- **국문 제목**: 5·18 공식 기념 연설의 담론 구조 비교: 이행기정의 담론의 정권별 분화
- **영문 제목**: Discourse Structure Comparison of Official May 18 Commemorative Addresses: Regime-Based Divergence in Transitional Justice Discourse
- **게재지**: 《기억과 전망》 55호 (Korea Democracy Foundation)
- **게재 상태**: 게재 확정
- **저자**: 정성윤 (전남대학교 5·18연구소) / Sungyoun Chung (The May 18 Institute, Chonnam National University)

---

## 리포지토리 구조 / Repository Structure

```
orilan/may18-official-speeches/
│
├── data/
│   ├── raw/
│   │   └── speeches_full.csv                    수집 원문 전체 (32편)
│   │
│   ├── processed/
│   │   ├── full_coding_results_final_v2.csv      메인 코딩 데이터 (1,293문장, 실 분석 28편 1,179문장)
│   │   ├── speeches_preprocessed_v2.csv           연설 단위 메타데이터 (32편)
│   │   ├── sentences_preprocessed_v2.csv          문장 단위 전처리 (1,293문장)
│   │   ├── tense_analysis_all_speeches.csv        시제 분석 (693문장)
│   │   └── 2026_coding_final.csv                  2026년 이재명 연설 별도 코딩 (49문장)
│   │                                               ※ 전체 코퍼스 분석 대상에 미포함
│   └── analysis/
│       ├── an_3_1_theme_distribution.csv          주제 분포
│       ├── an_3_1_type_distribution.csv           유형 분포
│       ├── an_3_1_cooccurrence_top.csv            공기어 상위 목록
│       ├── an_3_2_t4_timeline.csv                 T4 연도별 추이
│       ├── an_3_3_adjacency_by_theme.csv          주제별 인접성
│       ├── an_3_3_cooccurrence_by_theme.csv       주제별 공기어
│       ├── an_3_3_t1t2t4_freq.csv                 T1·T2·T4 빈도
│       ├── an_3_3_t3_focus.csv                    T3 집중 분석
│       ├── an_3_4_t6t7_cooccurrence.csv           T6·T7 공기어
│       └── an_3_5_tense_distribution.csv          시제 분포
│
├── codebook/
│   └── coding_scheme.md                      코딩 기준 및 판별 지침
│
├── dashboard/
│   └── index.html                            인터랙티브 분석 대시보드
│
└── README.md
```

---

## 데이터 설명 / Data Description

### `data/raw/`

| 파일 | 설명 |
|------|------|
| `speeches_full.csv` | 1993–2025년 5·18 기념식 공식 기념연설 원문 전체 (32편) |

원문 출처: 대통령기록관, 국무총리비서실 총리연설문집, 언론보도 자료.

### `data/processed/`

| 파일 | 설명 |
|------|------|
| `full_coding_results_final_v2.csv` | 7개 주제 범주 코딩 결과 전체 (1,293문장, 실 분석 28편 1,179문장) |
| `speeches_preprocessed_v2.csv` | 연설 단위 메타데이터 (연도, 대통령, 정권 유형 등, 32편) |
| `sentences_preprocessed_v2.csv` | 문장 단위 전처리 결과 (1,293문장) |
| `tense_analysis_all_speeches.csv` | THEME 유형 문장의 시제 분석 결과 (693문장) |
| `2026_coding_final.csv` | 2026년 이재명 연설 별도 코딩 (49문장, 전체 코퍼스 분석 대상에 미포함) |

#### 주요 변수 (`full_coding_results_final_v2.csv` 기준)

| 변수 | 설명 | 값 |
|------|------|----|
| `analysis_scope` | 분석 포함 여부 | `included` (28편) / `excluded` (4편) |
| `type` | 문장 유형 | THEME / CONTEXT / RITUAL / POLICY |
| `primary_theme` | 1차 주제 | T1–T7 |
| `secondary_theme` | 2차 주제 (복수) | `["T2", "T5"]` 형식 |
| `policy` | 정책 언급 여부 | True / False |
| `forgiveness_direction` | 용서 방향 (T2) | `state_to_victim` / `victim_to_perpetrator` / `general` |
| `tense` | 시제 | 과거 / 현재 / 미래 |

### `data/analysis/`

논문 3장 절 구성에 대응하는 분석 산출 파일입니다.

| 파일 | 내용 |
|------|------|
| `an_3_1_theme_distribution.csv` | 전체 주제 범주 분포 |
| `an_3_1_type_distribution.csv` | 문장 유형(THEME/CONTEXT/RITUAL/POLICY) 분포 |
| `an_3_1_cooccurrence_top.csv` | 전체 주제 공기 패턴 상위 목록 |
| `an_3_2_t4_timeline.csv` | T4(정의/진상규명) 연도별 추이 |
| `an_3_3_adjacency_by_theme.csv` | 주제별 인접성 분석 |
| `an_3_3_cooccurrence_by_theme.csv` | 주제별 공기어 분석 |
| `an_3_3_t1t2t4_freq.csv` | T1·T2·T4 빈도 분석 |
| `an_3_3_t3_focus.csv` | T3(화해·통합) 집중 분석 |
| `an_3_4_t6t7_cooccurrence.csv` | T6·T7 공기어 분석 |
| `an_3_5_tense_distribution.csv` | 정권별 시제 분포 |

---

## 코딩 체계 / Coding Scheme

7개 주제 범주(T1–T7)의 정의 및 코딩 기준은 `codebook/coding_scheme.md`를 참조하십시오.

코딩은 연구자 정의 코드북에 기반한 LLM 보조 자동 코딩 후, 전체의 10%에 해당하는 표본(130문장)에 대해 독립 연구자 수작업 코딩과의 일치율 검증을 거쳤습니다.

Coding was performed using an LLM-assisted pipeline guided by a researcher-defined codebook, with reliability verified through independent manual coding of a 10% sample (130 sentences).

---

## 인용 / Citation

**데이터셋 인용 / Dataset citation**

> 정성윤 (2026). 5·18 공식 기념 연설 코퍼스 (1997–2025) [Data set]. GitHub. https://github.com/orilan/may18-official-speeches

> Chung, Sungyoun (2026). Official May 18 Commemorative Address Corpus (1997–2025) [Data set]. GitHub. https://github.com/orilan/may18-official-speeches

**논문 인용 / Paper citation**

> 정성윤 (2026). 5·18 공식 기념 연설의 담론 구조 비교: 이행기정의 담론의 정권별 분화. 『기억과 전망』, 55.

> Chung, Sungyoun (2026). Discourse Structure Comparison of Official May 18 Commemorative Addresses: Regime-Based Divergence in Transitional Justice Discourse. *Memory and Vision*, 55.

---

## 라이선스 / License

| 대상 | 라이선스 | 조건 |
|------|----------|------|
| 코딩 데이터셋 (`data/`) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | 출처 명시 시 자유 이용 (상업적 이용 포함) |
| 연설문 원문 (`speeches_full.csv`) | 공공저작물 (공공누리 제1유형) | 출처 명시 시 자유 이용 |
| 대시보드 코드 (`dashboard/`) | [MIT License](https://opensource.org/licenses/MIT) | 자유 이용 |

데이터셋 이용 시 위 인용 정보의 형식으로 출처를 명시해 주십시오.

---

## 문의 / Contact

sungyounchung@gmail.com
