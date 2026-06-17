# Learning Record 0009 — 交叉持股分析的方法论

**Date**: 2026-06-17
**Lesson**: 0009-cross-holding-methodology.html
**Status**: 已完成

## Key insights

1. **每页回答一个具体的投资问题**是交叉持股报告的核心设计哲学。IHS P4 报告 10 页 = 10 个问题。堆砌数据 ≠ 报告。
2. **跨页交叉验证才是真正的洞察**。4 个经典场景：
   - 确认性（P2 大持仓 + P3 加仓 + P5 Top Buyer）= 强信号
   - 矛盾性（P2 大持仓 + P3 小减仓 + P6 非 Top Seller）= 可能是再平衡
   - 危险（P4 activist + P7 新建仓）= 高度预警
   - 转向（P8 被动资金上升 + P9 价值/成长轮动）= 行业生命周期变化
3. **正确的报告阅读顺序**：30 秒速览 → 2 分钟趋势 → 5 分钟深度 → 15 分钟研究。Dashboard 设计要支持这个节奏（概览卡片最显眼，深度数据藏 tab）。
4. **6 条设计原则**：
   - 每页回答一个问题
   - 每页底部留 Commentary 空白（给分析师写判断）
   - 表格列要对齐行业通用（Style / Turnover / Peer Average 缺一不可）
   - 排名表必须标排名指标
   - 图表和表格配套（饼图看分布，柱状图看流向）
   - 免责声明必须可见（每页底部，不在文档末尾）
5. **Top Buyers/Sellers 单向流动 = 99% 是 bug**。正常情况下双向（有人买有人卖）。常见原因：跨期对比错、字段映射错、数据源缺失。**自检清单必加"Buyers 和 Sellers 是否都有数据"**。
6. **跨期对比看股数（shares delta）不看市值（value delta）**。市值变化会被股价波动污染。Top Buyers 应按"主动加仓"或"股数变化"排序。
7. **Carvana 2026Q1 实战分析**：Vanguard/BlackRock 持股不变（被动指数资金稳定）+ Baupost 新增 $480M（价值投资者重新进入）+ 无 activist = "指数稳定 + 价值重估 + 无 activist 干扰" → 偏正面状态。
8. **输出质量 10 项自检清单**：单位、排名指标、institution_name、delta_pct 边界、Buyers/Sellers 对称、跨期相邻、免责声明、时滞、Item 4 review、中国 ADR "不适用"标注。

## Action items

- 验证：cross_holding.py 的输出是否符合"每页回答一个问题"的设计（参考 IHS P2-P10）
- 验证：Markdown 报告的阅读节奏是否支持 30 秒 / 2 分钟 / 5 分钟 / 15 分钟分层
- 验证：自检清单的 10 项是否在导出报告前自动执行（不是手工 check）
- 跟进：是否需要把"Commentary 空白"加到 Dashboard 的每页底部（分析师写判断的地方）
- 跟进：评估是否把"跨期对比"逻辑统一到 `comparative_holdings()` 函数里（避免不同 tab 各自实现）
