# Skill 地图 — 股票大作手回忆录

这是本书 10 张能力卡的导航页：先按总表定位「这件事归哪张卡」，再按依赖关系决定同一次任务里要不要多读一张卡。能力卡本体在 `bundle/cards/`，可直接安装的编译产物在 `single/` 与 `pack/`。

## 能力总表

10 个能力，重要度与去向均取自 `bundle/verified.yaml`。

| capability_id | slug | 中文标题 | 重要度 | 去向 |
|---|---|---|---|---|
| cap.som.min-resistance-trend-skill | min-resistance-trend-skill | 最小阻力路线趋势判读 | critical | promoted → 独立 skill |
| cap.som.key-point-trading-skill | key-point-trading-skill | 关键点体系 | critical | promoted → 独立 skill |
| cap.som.probe-and-scale-in-skill | probe-and-scale-in-skill | 试探—验证—加码建仓程序 | high | promoted → 独立 skill |
| cap.som.position-holding-exit-skill | position-holding-exit-skill | 头寸管理：持有、跟进与退出 | critical | promoted → 独立 skill |
| cap.som.mind-state-discipline-skill | mind-state-discipline-skill | 交易心理与状态自检 | critical | promoted → 独立 skill |
| cap.som.tips-and-authority-defense-skill | tips-and-authority-defense-skill | 贴士与权威信息防御 | critical | promoted → 独立 skill |
| cap.som.stock-sector-behavior-skill | stock-sector-behavior-skill | 个股与板块行为甄别 | high | promoted → 独立 skill |
| cap.som.liquidity-and-execution | liquidity-and-execution-skill | 流动性与执行 | medium | router → 路由入口 |
| cap.som.forecast-log | forecast-log-skill | 判断校准预测日志 | medium | router → 路由入口 |
| cap.som.livermore-rules-checklist | livermore-rules-checklist-skill | 利弗莫尔成文规则总表 | high | router → 路由入口 |

重要度口径（取自 `verified.yaml` 的 `importance` 字段）：critical 5 张、high 3 张、medium 2 张、low 0 张，合计 10 张。去向口径：promoted 7 张（在 pack 里各自独立成 skill）、router 3 张（只由路由入口调用）。

## 依赖关系

`also_read` 是能力卡自带的「同一任务里值得一并读」的关联（不是前置依赖，也不是必读清单），10 张卡共 21 条。下表右列按卡名（`bundle/cards/` 的文件名去掉 `.md`）列出；`verified.yaml` 里对应字段写的是 capability_id，其中 `cap.som.forecast-log` 与 `cap.som.liquidity-and-execution`、`cap.som.livermore-rules-checklist` 的卡名分别带 `-skill` 后缀。

| 能力（slug） | also_read |
|---|---|
| min-resistance-trend-skill | key-point-trading-skill、position-holding-exit-skill、forecast-log-skill |
| key-point-trading-skill | min-resistance-trend-skill、probe-and-scale-in-skill |
| probe-and-scale-in-skill | key-point-trading-skill、position-holding-exit-skill、liquidity-and-execution-skill |
| position-holding-exit-skill | probe-and-scale-in-skill、min-resistance-trend-skill、mind-state-discipline-skill |
| mind-state-discipline-skill | position-holding-exit-skill、livermore-rules-checklist-skill |
| tips-and-authority-defense-skill | stock-sector-behavior-skill、min-resistance-trend-skill |
| stock-sector-behavior-skill | min-resistance-trend-skill、tips-and-authority-defense-skill |
| liquidity-and-execution-skill | probe-and-scale-in-skill |
| forecast-log-skill | min-resistance-trend-skill |
| livermore-rules-checklist-skill | mind-state-discipline-skill、position-holding-exit-skill |

被引用最多的枢纽能力：`min-resistance-trend-skill`（5 次）、`position-holding-exit-skill`（4 次）、`probe-and-scale-in-skill`（3 次）、`key-point-trading-skill` 与 `mind-state-discipline-skill`（各 2 次）。这说明「先判大势」是全书被反复接回的第一道总闸门，而「仓位怎么处置」是第二道——两者都不在自己那张卡里解决，需要上下游配合。

## 加载顺序

1. **先读入口**：single 模式读 `single/stock-trader-recollection-skill/SKILL.md`；pack 模式读 `pack/stock-trader-recollection-skill-router/SKILL.md`（若问题直接命中 7 个独立 skill 之一，则读那个 skill 的 `SKILL.md`，不必再进路由入口）。
2. **按路由表加载 1 张能力卡**：入口的「能力路由」表按用户意图给出「先读」的那一张，一次只进 1 张；任务明确跨域时最多 2 张。
3. **需要补读时只补 1 张**：按上面依赖关系表挑与本任务直接相关的一条，不要把 `also_read` 整组读进来——那会把上下文塞满，且不会提高判据精度。
4. **概览类问题不加载卡**：书名、作者、章节、整书结构类问题用入口的「核心原则」与 `references/overview.md` 回答。
5. **术语与速查**：术语解释查 `references/glossary.md`，不需要原文依据时用 `references/cheatsheet.md`。
6. **路由表不命中**：先查 `references/capability-index.md`（完整意图与关键词索引）；仍不命中就明确告知超出本书范围，不要硬套。
