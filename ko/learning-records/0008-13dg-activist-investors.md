# Learning Record 0008 — Schedule 13D/G와 Activist

**Date**: 2026-06-17
**Lesson**: 0008-13dg-activist-investors.html
**Status**: 완료

## 핵심 인사이트

1. **13D vs 13G의 본질적 차이는 "의도"**: 13D = 능동 투자자(activist), 5% 초과 보유 + 회사 경영에 영향 의도; 13G = 수동 투자자(인덱스 펀드, 연금), 순수 투자이며 경영 간섭 없음. 경쟁사 모니터링은 거의 13D에만 관심을 둔다.
2. **13D는 일년에 수백 건, 13F의 분기당 2만 건 대비 극히 희소하지만 신호는 극강**. 매 건이 "누군가가 우리 회사에 대거 진입했다"는 의미다.
3. **Item 4 (Purpose of Transaction)는 13D의 영혼**: activist가 여기서 "이 회사를 산 이유가 무엇인지" 명시. 일반적 의도: 분할 요구, M&A 추진, CEO 교체 요구, 자본 배분 조정 요구.
4. **activist 판단 기준**: ① 과거 13D 신고 이력; ② proxy fight 이력; ③ 공개 activist 캠페인; ④ 헤지 펀드 + 집중 보유 + 높은 회전율.
5. **일반적 activist 전략(신호 강도 순)**:
   - 이사회 의석(⭐⭐⭐⭐⭐) — 경영진과 공개 대립
   - 자본 배분(⭐⭐⭐⭐) — 불신 투표
   - M&A 추진(⭐⭐⭐⭐) — 지배권 변경
   - 운영 개선(⭐⭐⭐) — 숨겨진 가치 신호
6. **13D 신고의 "비가역성"**: 일단 공개 13D를 제출하면, activist와 회사 이사회는 "공개 대립"에 진입 — 양측 모두 응답해야 함. 수동 보유가 아니라 **능동적 선전포고**.
7. **Item 4의 모호한 어조 = "깃발만 들고 지켜보는" 형 activist**: 자리만 차지하고 진짜 공격은 없을 수 있음. 후속 60-90일 내 보완 13D / proxy fight / 공개 이사 후보 추천 여부 확인 필요.
8. **중국 ADR의 특수성**: UXIN은 ADR이므로 13D/G 적용 대상이지만, 유동성 부족 + 중국 이사회 + 법률 환경 차이 → activist의 실제 추진 능력은 제한적. 한 번 발생하면 오히려 강한 신호(희귀 이벤트).
9. **현재 vs IHS의 격차**: 정적 명단 8개사 vs IHS 50-100개사. WhaleWisdom / SharkWatch 구매 또는 EDGAR 13D 월보 수동 스캔 필요. MVP 단계에서는 "8개사 + 수동 월간 스캔 + 신규 activist 출현 경보" 조합이 가장 경제적.

## Action items

- 검증: config.py의 ACTIVIST_INSTITUTIONS 명단에 주류 activist(Elliott, Starboard, Third Point, Baupost, Pershing Square 등)가 포함되는지
- 검증: Dashboard의 "Activists" 탭이 별도 페이지로 구성되는지(다른 기관과 혼합되지 않음)
- 검증: 13D Item 4 추출이 자동인지 수동인지(MVP는 수동 리뷰 + 하이라이트 표시여야 함)
- 후속: WhaleWisdom 최소 티어의 ROI 평가($500-2000/년)
- 후속: "신규 activist 출현" 자동 경고 구축 필요 여부(EDGAR 13D 월보 + keyword 필터 기반)
