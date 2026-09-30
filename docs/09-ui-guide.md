# 09 — UI Guide / 界面指南

## 页面

| 页面 | 说明 |
|---|---|
| WATCH_ONLY 首页 | 统计、Top 排名、全量观察记录表 |
| WATCH 详情 | 单场盘口、λ、五态概率、结算记录 |
| Live 总览 | 实时比赛与资格漏斗 |
| Settlement | 已结算记录 |
| Diagnostics | 阻断原因与 Gate 诊断 |

## Top 排名

- `rank_score = P_POSITIVE × 50 + P_WIN × 30 + lambda_gap × 20`
- `lambda_gap = lambda_model - (line - 当前进球)`
- TOP 1-5 金色高亮，TOP 6-10 蓝色高亮
- 支持按综合评分 / P_POSITIVE / P_WIN / λ_model / 最新变化排序

## 标记

- `WATCH_ONLY`：观察模式
- `NO PROVEN EDGE`：未宣称已证明优势
