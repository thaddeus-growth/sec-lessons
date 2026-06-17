# Learning Record 0006 — 13F와 기관 보유

**Date**: 2026-06-17
**Lesson**: 0006-13f-institutional-holdings.html
**Status**: 완료

## 핵심 인사이트

1. **13F의 본질**: 분기말 스냅샷이며, 분기 내 흐름이 아니다. 모든 기간 간 비교는 인접한 두 13F 사이의 "조정의 근사치"이며 실제 turnover이 아니다.
2. **단위 함정은 버그 다발 구역**: `value_x1000` 필드명 = "천 달러 단위". 1000배 오배치는 전형적 오류. 검증 방법: 주가 × 주식 수 ≈ value_x1000 × 1000.
3. **기간 간 비교는 시가총액이 아닌 주식 수로**: 주식 수 변화 = 능동적 조정; 시가총액 변화는 주가 변동에 오염됨. 기관이 CVNA 100만 주를 보유하고 주가 $100→$150 = 수동적 시가총액 상승, 추가 매수가 아님.
4. **13F의 사각지대는 구조적 제약**: 롱 포지션만, 미국 주식만, 분기말만, $1억 초과 기관만 포함. 공매도, 옵션, 분기 내 조정, 소규모 기관과 개인 투자자는 보이지 않음. **이것이 13F가 "누가 사고팔고 있는가"는 답할 수 있어도 "왜 사고팔고 있는가"는 답할 수 없는 이유다**.
5. **경계 조건(5가지 보유 상태)**: Initiation / Liquidation / Increase / Decrease / No change. FULL OUTER JOIN 후 institution_name으로 보완, prev_value = 0일 때 0 나누기 회피.
6. **집계 시 기관별로 따로 순위 매기기, 단순 SUM 금지**: Carvana의 $1.92B 보유 vs UXIN의 $3M 보유는 600배 차이, 단순 합산 시 UXIN 신호가 묻힘. Top Buyers/Sellers는 반드시 "per ticker" 또는 "per institution" 그룹화.
7. **IHS Markit 보고서 P2-P7은 거의 전부 13F 데이터 위에 구축** — 이것이 13F가 "교차 보유 분석의 데이터 기반"인 이유다.

## Action items

- 검증: cross_holding.py의 pivot_table이 "per ticker"로 그룹화·정렬되는지 확인(단순 SUM 아님)
- 검증: value_x1000 필드가 데이터 흐름 전체에서 SEC 원 단위를 유지하는지 확인
- 후속: Dashboard에 "주식 수 변화 vs 시가총액 변화" 비교 카드를 추가하여 Top Buyers/Sellers 순위를 더 정확하게 할지 검토
