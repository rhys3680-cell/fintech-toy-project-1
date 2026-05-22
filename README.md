# Fintech Data Analysis

> 데이터 분석 학습 프로젝트 — EDA부터 머신러닝까지

## 개요

데이터 분석의 실무 프로세스(데이터 이해 → EDA → 전처리 → 모델링)를
공개 데이터셋에 적용하며 익히는 학습용 레포입니다.

> 진행 중: **프로젝트 1 (Iowa Housing) — EDA 완료, 전처리 단계 예정**

---

## 프로젝트 1: 주택 가격 예측 (Iowa Housing)

- **데이터**: [House Prices / Ames Housing](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) — 1,460건 × 81컬럼
- **문제**: 주택 특성으로 판매가(SalePrice)를 예측하는 **회귀(Regression)**
- **접근**: EDA(분포·결측·상관) → 전처리(결측·log 변환·인코딩) → 회귀 모델 → 평가
- **주요 결과 (EDA)**:
  - SalePrice 우편향(skew 1.88) → log 변환으로 정규분포화
  - 가격 핵심 변수: OverallQual(0.79), GrLivArea(0.71) — 품질·크기
  - 결측의 두 종류: 구조적("시설 없음") vs 진짜 누락 구분

📁 [EDA 노트북](notebooks/iowa-housing/)

---

## 향후 계획

- **모바일 결제 사기 탐지** — PaySim 데이터셋 기반 불균형 분류 (보류)
- **주식 시장 백테스팅** — 기술적 지표 매매 전략 검증

---

## 기술 스택

| 분야 | 도구 |
|---|---|
| 언어 | Python 3.13, SQL |
| 분석 환경 | JupyterLab |
| 데이터 | pandas, numpy |
| DB | SQLite |
| ML | scikit-learn, XGBoost, imbalanced-learn |
| 시각화 | matplotlib, seaborn |
| 데이터 취득 | Kaggle API, yfinance |
| 환경 관리 | uv |

---

## 실행 방법

```powershell
# 의존성 설치
uv sync

# Jupyter Lab 실행
uv run jupyter lab
```

데이터셋은 [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)에서 다운로드 후 `data/iowa-housing/` 폴더에 위치.

---

## 디렉토리 구조

```
.
├── notebooks/      # 분석 노트북 (iowa-housing 등 프로젝트별)
├── src/            # 재사용 모듈
├── data/           # 원본 데이터 (gitignore)
├── db/             # SQLite DB (gitignore)
└── reports/        # 요약 리포트
```

---

## 진행 상황

- [ ] 프로젝트 1: 주택 가격 예측 (Iowa Housing)
  - [x] EDA: 분포 · 범주형 · 결측 · 타겟 상관
  - [ ] 전처리: 결측 채우기 · log 변환 · 인코딩 · 이상치 제거
  - [ ] 모델링: 회귀 모델 학습 + 평가
  - [ ] 리포트 정리
- [ ] 향후: 사기 탐지(PaySim) · 시장 백테스팅