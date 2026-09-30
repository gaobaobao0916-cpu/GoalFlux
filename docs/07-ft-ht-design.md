# 07 — FT / HT Design / 全场与半场独立设计

## 独立原则

FT 与 HT 是完全独立的两条链，共享框架但不共享状态。

| 维度 | HT | FT |
|---|---|---|
| 盘口类型 | FIRST_HALF_ASIAN_TOTAL | FULL_TIME_ASIAN_TOTAL |
| 结算边界 | 半场结束 | 全场结束 |
| λ | 独立 | 独立 |
| 概率 | 独立 | 独立 |
| 结算 | 独立 | 独立 |
| 去重 key | fixture_id + HT | fixture_id + FT |

## 为何分离

- HT 盘口仅对上半场进球结算，FT 盘口对全场进球结算
- 两者的剩余进球时间窗口不同，λ 与概率不可混用
- 独立去重避免同一场比赛的 FT / HT 记录互相覆盖
