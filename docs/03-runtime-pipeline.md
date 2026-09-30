# 03 — Runtime Pipeline / 运行管线

## 阶段

1. **Snapshot 采集**：拉取实时比赛状态与主盘口快照
2. **Identity 校验**：确认 fixture 身份一致
3. **Sync 同步**：比分、分钟、盘口状态与主源对齐
4. **Freshness 新鲜度**：盘口年龄在阈值内才继续
5. **Scope 范围**：区分 FT / HT，各自独立结算边界
6. **Probability 计算**：λ → 泊松分布 → 各概率字段
7. **Settlement 结算**：五态概率 + 最终结算
8. **Watch 观察**：通过全部 Gate 后进入 WATCH_ONLY，参与排名

## 动态刷新

- 每次心跳 / 市场更新重新读取最新 Watch state
- 排名在数据入口一次性重算，不缓存陈旧排名
- 已结算记录不参与当前排名，仅在"全部"视图可见
