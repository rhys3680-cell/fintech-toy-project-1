# Fintech Data Analysis

> 핀테크 도메인 데이터 분석 프로젝트 — 사기 탐지 및 시장 분석

## 개요

본 레포는 두 가지 핀테크 분석 프로젝트를 다룹니다.

1. **모바일 결제 사기 탐지** — PaySim 데이터셋 (600만 거래) 기반 ML 분류
2. **주식 시장 백테스팅** — 기술적 지표 기반 매매 전략 검증

> 진행 중 (Week 1 / 14)

---

## 프로젝트 1: 모바일 결제 사기 탐지

- **데이터**: [PaySim](https://www.kaggle.com/datasets/ealaxi/paysim1) — 6,362,620건 거래
- **문제**: 사기 거래 비율 0.13%의 극심한 불균형 분류
- **접근**: SQL EDA → 베이스라인(로지스틱) → RF/XGBoost → Feature engineering
- **주요 결과**: _Phase 1 완료 후 업데이트_

📁 [Phase 1 노트북](notebooks/) · [Phase 1 요약 리포트](reports/)

---

## 프로젝트 2: 주식 시장 백테스팅

- **데이터**: yfinance / OpenBB (KOSPI, S&P500)
- **문제**: 단순 기술적 지표 매매 전략이 시장 수익률을 능가하는가?
- **접근**: 시계열 처리 → 지표 계산 → 백테스팅 → 포트폴리오 분석
- **주요 결과**: _Phase 2 완료 후 업데이트_

📁 [Phase 2 노트북](notebooks/) · [Phase 2 요약 리포트](reports/)

---

## 기술 스택

| 분야 | 도구 |
|---|---|
| 언어 | Python 3.12, SQL |
| 데이터 | pandas, numpy |
| DB | SQLite |
| ML | scikit-learn, XGBoost, imbalanced-learn |
| 시각화 | matplotlib, seaborn |
| 시장 데이터 | yfinance, OpenBB |
| 환경 관리 | uv |

---

## 실행 방법

```powershell
# 의존성 설치
uv sync

# Jupyter Lab 실행
uv run jupyter lab
```

PaySim 데이터셋은 [Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1)에서 다운로드 후 `data/` 폴더에 위치.

---

## 디렉토리 구조

```
.
├── notebooks/      # 정제된 분석 노트북
├── src/            # 재사용 모듈 (data_loader 등)
├── data/           # 원본 데이터 (gitignore)
├── db/             # SQLite DB (gitignore)
└── reports/        # Phase별 요약 리포트
```

---

## 진행 상황

- [ ] Phase 1: 사기 탐지 (Week 1-8)
  - [ ] Week 1-2: 환경 셋업 + EDA
  - [ ] Week 3-4: SQL 분석 + 시각화
  - [ ] Week 5-6: 베이스라인 모델
  - [ ] Week 7-8: 모델 개선 + 리포트
- [ ] Phase 2: 시장 분석 (Week 9-14)
  - [ ] Week 9-10: 데이터 수집
  - [ ] Week 11-12: 백테스팅
  - [ ] Week 13-14: 포트폴리오 + 마무리