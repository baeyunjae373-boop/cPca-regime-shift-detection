# cPCA-based Multivariate Time-Series Regime Shift Detection

FRED 거시경제 데이터를 활용해 다변량 시계열의 구조적 변곡점을 자동 탐지하는 방법론 연구

## 연구 개요

기존 PCA는 전체 구간을 하나의 공분산 구조로 가정하기 때문에, 특정 시기에만 나타나는 고유한 충격 패턴이 희석된다는 한계가 있습니다. 이를 보완하기 위해 cPCA를 적용해 코로나19 충격의 구조적 특성을 분리하고, 나아가 사전 시점 지정 없이 구조 변화를 자동 탐지하는 DSSI(Dual-State Structural Index)를 직접 설계했습니다.

## 핵심 내용

- **PCA vs cPCA 비교 분석**: 코로나19 전후 경제 구조 변화 정량 분석
- **DSSI 설계**: 변동성 비율(trace ratio)과 주성분 간 코사인 유사도를 결합한 통합 지수로 위기 진입·지속·회복을 실시간 판별
- **상태 전이형 탐지 파이프라인**: 사전 변곡점 지정 없이 구조 변화 자동 탐지

## 데이터

FRED(Federal Reserve Economic Data) 거시경제 지표 6개
- 실물 경제: INDPRO, RSAFS, PCE
- 고용·물가: UNRATE, CPIAUCSL
- 금융 시장: DGS10

## 주요 결과

- cPCA alpha 37.35 → 코로나 충격이 기존 추세의 연장이 아닌 구조적 단절임을 입증
- 2022년 4월 코로나 충격 해소 시점 정량 확인
- 2024년 이후 과거·코로나 시기와도 다른 제3의 경제 구조 전환 탐지

## 기술 스택

Python, numpy, pandas, scikit-learn, matplotlib


데이터 출처: FRED (Federal Reserve Economic Data) — https://fred.stlouisfed.org
