# Learning Record 0008 — Schedule 13D/G 与 Activist

**Date**: 2026-06-17
**Lesson**: 0008-13dg-activist-investors.html
**Status**: 已完成

## Key insights

1. **13D vs 13G 的本质区别在"意图"**：13D = 主动投资者（activist），持股 >5% 且意图影响公司；13G = 被动投资者（指数基金、养老金），纯投资不干预经营。竞品监控几乎只关心 13D。
2. **13D 一年只有几百次，相对 13F 的 2 万次/季 = 极稀缺但信号极强**。每一次都代表"有人大举建仓到你家"。
3. **Item 4 (Purpose of Transaction) 是 13D 的灵魂**：activist 在这里写明"我买这家公司是要做什么"。常见意图：要求分拆、推动 M&A、要求换 CEO、要求资本配置调整。
4. **判断 activist 的标准**：① 历史 13D 申报记录；② proxy fight 记录；③ 公开 activist campaign；④ 对冲基金 + 集中持仓 + 高换手率。
5. **常见 activist 策略（按信号强度排序）**：
   - 董事会席位（⭐⭐⭐⭐⭐）— 公开对抗管理层
   - 资本配置（⭐⭐⭐⭐）— 不信任投票
   - M&A 推动（⭐⭐⭐⭐）— 控制权变更
   - 运营改善（⭐⭐⭐）— 隐藏价值信号
6. **13D 申报的"不可逆性"**：一旦公开提交 13D，activist 和公司董事会就进入"公开博弈"——双方都必须回应。这不是被动持有，是**主动宣战**。
7. **Item 4 措辞模糊 = "先举旗后观望"型 activist**：可能只是占位逼宫，没有真打。要看后续 60-90 天内有没有补充 13D / proxy fight / 公开提名董事。
8. **中国 ADR 的特殊性**：UXIN 是 ADR 所以 13D/G 适用，但流动性差 + 中国董事会 + 法律环境差异 → activist 实际推动能力有限。出现一次反而是强信号（罕见事件）。
9. **我们当前 vs IHS 的差距**：静态名单 8 家 vs IHS ~50-100 家。补齐需要采购 WhaleWisdom / SharkWatch 或人工月度扫描 EDGAR 13D 月报。MVP 阶段用"8 家 + 人工月度扫描 + 新 activist 出现告警"组合最经济。

## Action items

- 验证：config.py 的 ACTIVIST_INSTITUTIONS 名单是否包含主流 activist（Elliott、Starboard、Third Point、Baupost、Pershing Square 等）
- 验证：Dashboard "Activists" Tab 是否单独成页（不是和其他机构混在一起）
- 验证：13D Item 4 的提取是自动还是手工（MVP 应该是手工 review + 高亮显示）
- 跟进：评估采购 WhaleWisdom 最低 tier 的 ROI（$500-2000/年）
- 跟进：是否需要建立"新 activist 出现"自动告警（基于 EDGAR 13D 月报 + keyword 过滤）
