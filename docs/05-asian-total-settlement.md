# 05 — Asian Total Settlement / 五态结算

## 五态

| 结果 | 说明 |
|---|---|
| WIN | 两注全赢 |
| HALF_WIN | 一注赢、一注走水 |
| PUSH | 两注全走水 |
| HALF_LOSS | 一注输、一注走水 |
| LOSS | 两注全输 |

## 半盘拆分

Asian Total 的 `.25` / `.75` 盘口拆为两注等注：

```text
Over 2.75 = 0.5 × Over 2.5  +  0.5 × Over 3.0
Under 2.75 = 0.5 × Under 2.5 + 0.5 × Under 3.0
```

## 结算示例（Over 2.75）

| 全场总进球 | Over 2.5 | Over 3.0 | 综合 |
|---|---|---|---|
| 4+ | WIN | WIN | WIN |
| 3 | WIN | PUSH | HALF_WIN |
| 2 | PUSH | LOSS | HALF_LOSS |
| ≤1 | LOSS | LOSS | LOSS |

仅展示数学结算逻辑，不构成投注建议。
