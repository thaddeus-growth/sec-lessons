# Learning Record 0006 — 13F 与机构持仓

**Date**: 2026-06-17
**Lesson**: 0006-13f-institutional-holdings.html
**Status**: 已完成

## Key insights

1. **13F 的本质**：季度末快照，不是季度内流水。所有跨期对比都是相邻两期 13F 之间的"调仓近似"——不是真实 turnover。
2. **单位陷阱是 bug 高发区**：`value_x1000` 字段名 = "以千美元为单位"。错放 1000 倍 = 经典错误。验证方法：股价 × 股数 ≈ value_x1000 × 1000。
3. **跨期对比看股数不看市值**：股数变化 = 主动调仓；市值变化会被股价波动污染。某机构持有 CVNA 100 万股不动、股价从 $100 涨到 $150 = 被动市值上涨，不是加仓。
4. **13F 的盲区是结构性约束**：只覆盖多头、只覆盖美股、只覆盖季末、只覆盖 >$1 亿机构。看不到做空、期权、季度内调仓、小机构和散户。**这决定了 13F 能回答"谁在买卖"，不能回答"为什么买卖"**。
5. **边界条件（5 种持仓状态）**：Initiation / Liquidation / Increase / Decrease / No change。FULL OUTER JOIN 后用 institution_name 补全，避免 prev_value = 0 时除零。
6. **汇总时按机构分别排名，不能简单 SUM**：Carvana 上 $1.92B 的持仓 vs UXIN 上 $3M 的持仓差 600 倍，直接求和会把 UXIN 的信号淹没。Top Buyers/Sellers 必须按"per ticker"或"per institution"分组。
7. **IHS Markit 报告 P2-P7 几乎全部建立在 13F 数据上**——这就是为什么 13F 是"交叉持股分析的数据底座"。

## Action items

- 验证：检查 cross_holding.py 的 pivot_table 是否按"per ticker"分组排序（不是简单 SUM）
- 验证：检查 value_x1000 字段在数据流中是否全程保持 SEC 原始单位
- 跟进：考虑是否在 Dashboard 上加一个 "股数变化 vs 市值变化" 的对比卡片，让 Top Buyers/Sellers 排名更准确
