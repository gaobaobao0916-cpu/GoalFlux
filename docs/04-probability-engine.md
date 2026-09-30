# 04 — Probability Engine / 剩余进球引擎

## 输入

- 当前分钟（canonical minute）
- 当前比分（home_score / away_score）
- Asian Total 盘口 line
- 剩余进球强度 λ（lambda_model）

## 剩余进球分布

基于 λ 与泊松分布，推导从当前时刻到结算边界（FT 或 HT）的剩余进球概率。

## 输出字段

| 字段 | 含义 |
|---|---|
| λ_market | 市场隐含剩余进球强度 |
| λ_model | 模型估计剩余进球强度 |
| P3 / P5 / P7 / P10 | 未来 3/5/7/10 分钟至少再进 1 球 |
| P_HT | 到半场结束前至少再进 1 球 |
| P_FT | 到全场结束前至少再进 1 球 |
| P_POSITIVE | 当前盘口 WIN + HALF_WIN 概率 |

> P_POSITIVE 是盘口结算口径，不等于 P_HT / P_FT（事件口径）。
