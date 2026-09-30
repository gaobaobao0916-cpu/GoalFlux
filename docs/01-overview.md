# 01 — Overview / 概述

## 中文

GoalFlux 是一套面向实时足球比赛的概率分析与 Asian Total 结算研究系统。系统将实时比赛状态、亚洲大小球市场、剩余进球分布与五态结算模型组织为统一数据链，为全场（FT）与半场（HT）场景提供 WATCH_ONLY 人工观察界面。

### 定位

- **研究与实时分析工具**：不将未经验证的概率差异包装成"已证明优势"
- **WATCH_ONLY**：正式自动化信号保持关闭，仅做人工观察
- **Fail-Closed**：数据质量存疑即阻断

### 核心模块

1. Remaining Goals λ 引擎
2. Asian Total 五态结算引擎
3. FT / HT 双范围独立链
4. WATCH_ONLY 观察视图与 Top 排名
5. 实时资格漏斗与诊断

## English

GoalFlux is a real-time football probability analytics and Asian Total settlement research system. It unifies live match state, Asian Total markets, remaining-goals distributions, and five-state settlement into a single FT/HT WATCH_ONLY observation pipeline.

### Positioning

- Research and real-time observation only — no proven edge is claimed.
- WATCH_ONLY: official automated signals remain disabled.
- Fail-closed: any data-quality doubt blocks the fixture.
