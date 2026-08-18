# Hotel Booking Cancellation Analysis

EDA project by 윤동욱

호텔 예약 데이터를 분석하여 예약 취소 패턴과 취소 요인을 파악하고,
취소율 개선을 위한 인사이트를 도출하는 EDA 프로젝트입니다.

---

## Project Overview

### Goal

호텔 예약 데이터를 기반으로:
- 호텔 유형별 취소율 비교
- 예약 특성에 따른 취소 패턴 분석
- 고객 및 예약 채널별 취소 현상 파악

을 수행하여 예약 취소의 주요 요인을 분석합니다.

---

## Dataset

- Dataset: Hotel Booking Cancellation Dataset
- Source: Codeit Sprint (Modified Dataset)

주요 컬럼:
- `hotel`: 호텔 유형
- `is_canceled`: 예약 취소 여부 (Target Variable)
- `lead_time`: 예약 후 체크인까지의 기간
- `market_segment`: 예약 시장 유형
- `country`: 고객 국가
- `booking_changes`: 예약 변경 횟수

자세한 컬럼 설명:
[data/data_dictionary.md](./data/data_dictionary.md)

---

## Analysis Process

### 1. Data Preprocessing

- 데이터 구조 확인
- 결측치 처리
- 데이터 타입 확인
- 분석 대상 변수 선정

### 2. Exploratory Data Analysis (EDA)

#### Univariate Analysis
- 호텔 유형별 예약 분포
- Lead Time 분포
- 예약 채널 분포
- 고객 특성 분석

#### Cancellation Analysis
- 호텔별 취소율 비교
- 시장 세그먼트별 취소율 분석
- 예약 특성별 취소 패턴 분석

---

## Key Findings

- City Hotel의 취소율은 41.7%로 Resort Hotel의 27.8%보다 높게 나타났습니다.
- 주요 시장 유형 중 `Groups`의 취소율이 61.1%로 가장 높았습니다.
- 리드타임이 길어질수록 취소율이 증가했으며, 180일을 초과한 예약의 취소율은 50% 이상이었습니다.
- 포르투갈 예약은 장기 리드타임 구간에서 특히 높은 취소율을 보였습니다.
- 과거 취소 이력이 한 번 이상 있는 예약의 현재 취소율은 91.6%로 높게 나타났습니다.
- 과거 정상 예약 이력이 있는 예약의 취소율은 5.5%로 낮게 나타났습니다.
- 예약 변경이 없는 그룹의 취소율은 40.9%로, 한 번 이상 변경한 그룹의 15.7%보다 높았습니다.

---

## Recommendations

- `Groups` 및 장기 리드타임 예약에는 예치금이나 취소 시점별 차등 환불 정책을 검토합니다.
- 장기 예약 고객에게 정기적으로 예약 확인 메시지를 보내고, 취소 대신 일정 변경을 선택할 수 있도록 유도합니다.
- 과거 취소 이력이 있는 예약에는 추가적인 예약 확인 절차를 적용하는 방안을 검토합니다.
- 고객이 날짜나 객실 조건을 쉽게 변경할 수 있도록 예약 변경 절차를 간소화합니다.
- 국가 자체를 기준으로 정책을 다르게 적용하기보다 리드타임, 예약 유형, 과거 취소 이력 등 예약 조건을 기준으로 관리합니다.

> 본 분석은 EDA를 통해 변수와 예약 취소 사이의 관계를 확인한 결과이며, 특정 변수가 취소의 직접적인 원인임을 의미하지는 않습니다.

---

## Environment

Python 3.x

Libraries:
- pandas
- numpy
- matplotlib
- seaborn
- jupyter

설치:

```bash
pip install -r requirements.txt
```