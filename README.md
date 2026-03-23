\# 용서 없는 화해의 정치: 5·18 대통령 기념사의 담론 연쇄 구조와 정권별 분화



\*\*The Politics of Reconciliation Without Forgiveness: Discursive Chain Structures and Regime-Based Divergence in South Korea's May 18 Presidential Addresses\*\*



---



\## 개요 / Overview



이 리포지토리는 《기억과 전망》 투고 논문 "용서 없는 화해의 정치"의 분석에 사용된 코퍼스 데이터와 분석 결과 파일을 공개합니다.



This repository provides the corpus data and analysis outputs accompanying the paper "The Politics of Reconciliation Without Forgiveness," submitted to \*Memory and Prospect\* (민주화운동기념사업회).



1993년부터 2025년까지 5·18 광주민주화운동 기념식에서 발화된 대통령 기념사 전수(32편, 1,293문장)를 코퍼스로 구성하고, 사죄(T1)·용서(T2)·화해(T3)·정의/진상규명(T4)·치유/회복(T5)·기억/계승(T6)·역사의식(T7)의 7개 주제 범주로 코딩하여, 한국 공식 기념 담론에서 사죄-용서-화해의 규범적 연쇄가 구조적으로 단절되어 있음을 실증합니다.



The corpus comprises all 32 presidential addresses delivered at the May 18 Gwangju Uprising commemorations (1993–2025), totaling 1,293 sentences. Sentences are coded into seven thematic categories (T1–T7) covering apology, forgiveness, reconciliation, justice/truth-seeking, healing/recovery, memory/commemoration, and historical consciousness. The analysis demonstrates that the normative apology-forgiveness-reconciliation chain has been structurally severed in South Korea's official commemorative discourse, with asymmetric patterns across conservative and progressive administrations.



---



\## 논문 정보 / Paper Information



\- \*\*국문 제목\*\*: 용서 없는 화해의 정치: 5·18 대통령 기념사의 담론 연쇄 구조와 정권별 분화

\- \*\*영문 제목\*\*: The Politics of Reconciliation Without Forgiveness: Discursive Chain Structures and Regime-Based Divergence in South Korea's May 18 Presidential Addresses

\- \*\*투고 저널\*\*: 《기억과 전망》 (Korea Democracy Foundation)

\- \*\*저자\*\*: 정성윤 (전남대학교 5·18연구소) / Sungyoun Chung (The May 18 Institute, Chonnam National University, Korea)



---



\## 리포지토리 구조 / Repository Structure



```

may18-presidential-speeches/

│

├── data/

│   ├── raw/                        # 원문 텍스트 / Raw speech texts

│   │   └── speeches\_full.csv

│   ├── processed/                  # 전처리·코딩 완료본 / Preprocessed \& coded data

│   │   ├── speeches\_preprocessed.csv

│   │   ├── sentences\_preprocessed.csv

│   │   ├── full\_coding\_results\_final.csv

│   │   └── tense\_analysis\_all\_speeches.csv

│   └── analysis/                   # 분석 산출물 / Analysis outputs

│       ├── ch3\_s1\_cooccurrence\_all.csv

│       ├── ch3\_s1\_theme\_distribution.csv

│       ├── ch3\_s1\_type\_distribution.csv

│       ├── ch3\_s2\_t4\_timeline.csv

│       ├── ch3\_s3\_adjacency\_byregime.csv

│       ├── ch3\_s3\_cooccurrence\_byregime.csv

│       ├── ch3\_s3\_t2\_direction.csv

│       ├── ch3\_s4\_t6t7\_analysis.csv

│       └── ch3\_s5\_tense\_distribution.csv

│

├── codebook/                       # 코딩 기준 / Coding scheme

│   └── coding\_scheme.md

│

├── scripts/                        # 분석 코드 / Analysis scripts (추후 공개)

│

└── figures/                        # 논문 수록 그림 / Figures (게재 확정 후 공개)

```



---



\## 데이터 설명 / Data Description



\### `data/raw/`



| 파일 | 설명 |

|------|------|

| `speeches\_full.csv` | 1993–2025년 5·18 기념식 대통령 기념사 원문 전체 (32편) |



원문 출처: 대통령기록관, 국무총리비서실 총리연설문집, 언론보도 자료.



\### `data/processed/`



| 파일 | 설명 |

|------|------|

| `speeches\_preprocessed.csv` | 연설문 메타데이터 (연도, 대통령, 정권 유형 등) |

| `sentences\_preprocessed.csv` | 문장 단위 분리 결과 (1,293문장) |

| `full\_coding\_results\_final.csv` | 7개 주제 범주 코딩 결과 전체 |

| `tense\_analysis\_all\_speeches.csv` | THEME 유형 문장의 시제 분석 결과 (693문장) |



\### `data/analysis/`



3장 절 구성에 대응하는 분석 산출 파일입니다.



| 파일 | 대응 절 | 내용 |

|------|---------|------|

| `ch3\_s1\_theme\_distribution.csv` | 3장 1절 | 전체 주제 범주 분포 |

| `ch3\_s1\_type\_distribution.csv` | 3장 1절 | 문장 유형(THEME/RITUAL 등) 분포 |

| `ch3\_s1\_cooccurrence\_all.csv` | 3장 1절 | 전체 주제 공기 패턴 |

| `ch3\_s2\_t4\_timeline.csv` | 3장 2절 | T4(정의/진상규명) 시계열 변화 |

| `ch3\_s3\_adjacency\_byregime.csv` | 3장 3절 | 정권별 T3(화해) 인접 패턴 |

| `ch3\_s3\_cooccurrence\_byregime.csv` | 3장 3절 | 정권별 주제 공기 분석 |

| `ch3\_s3\_t2\_direction.csv` | 3장 3절 | T2(용서) 방향성 분석 |

| `ch3\_s4\_t6t7\_analysis.csv` | 3장 4절 | T6(기억/계승)·T7(역사의식) 분석 |

| `ch3\_s5\_tense\_distribution.csv` | 3장 5절 | 정권별 시제 분포 |



---



\## 코딩 체계 / Coding Scheme



7개 주제 범주(T1–T7)의 정의 및 코딩 기준은 `codebook/coding\_scheme.md`를 참조하십시오.



코딩은 연구자 정의 코드북에 기반한 LLM 보조 자동 코딩 후, 전체의 10%에 해당하는 표본(130문장)에 대해 독립 연구자 수작업 코딩과의 일치율 검증을 거쳤습니다.



Coding was performed using an LLM-assisted pipeline guided by a researcher-defined codebook, with reliability verified through independent manual coding of a 10% sample (130 sentences).



---



\## 인용 / Citation



> 정성윤. \[발행연도]. "용서 없는 화해의 정치: 5·18 대통령 기념사의 담론 연쇄 구조와 정권별 분화." 『기억과 전망』 \[권(호)]. \[페이지]. https://github.com/orilan/may18-presidential-speeches



---



\## 라이선스 / License



\- \*\*데이터\*\* (`data/`): \[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

\- \*\*코드\*\* (`scripts/`): \[MIT License](https://opensource.org/licenses/MIT)



원문 텍스트(`speeches\_full.csv`)는 대한민국 공공저작물로, 출처 명시 조건 하에 자유롭게 이용 가능합니다.



---



\## 문의 / Contact



jngsyn@gmail.com

