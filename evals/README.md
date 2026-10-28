# 《股票大作手回忆录》能力包 · 阶段 4 压力测试套件

> 对应 `cangjie-skill/methodology/06-stage4-pressure-test.md`（v2.1 分层测试对象）。
> 本套件**只构建，未执行**——执行按下方"盲测执行说明"进行。

## 1. 文件清单

| 文件 | 内容 | 格式 |
|---|---|---|
| `test-prompts.json` | 10 张能力卡的触发精度测试（90 条） | 顶层数组，每个元素为一组 `{skill, capability_id, version, test_cases[]}`，darwin 兼容字段：`skill / version / test_cases[{id, type, prompt, expected_behavior, notes}]` |
| `output-cases.json` | 全部 10 个 active 能力的输出质量测试（22 条） | 顶层 `{suite_id, schema_version, target, note, output_cases[]}`；每条含 `capability_id / case_id / task_ref / scenario_type / task / inputs / checks / boundary_note` |
| `README.md` | 本说明 | — |

`id` 规范：触发用例 `<slug>-st-NN`（should_trigger）/ `<slug>-snt-NN`（should_not_trigger）/ `<slug>-edge-NN`（edge_case）；输出用例 `<slug>-out-NN`。

## 2. 用例统计

### 触发用例（test-prompts.json）：合计 90 条

| # | 能力卡（slug） | should_trigger | should_not_trigger | edge_case | 小计 |
|---|---|---|---|---|---|
| 1 | min-resistance-trend-skill | 4 | 3 | 2 | 9 |
| 2 | key-point-trading-skill | 4 | 3 | 2 | 9 |
| 3 | probe-and-scale-in-skill | 4 | 3 | 2 | 9 |
| 4 | position-holding-exit-skill | 4 | 3 | 2 | 9 |
| 5 | mind-state-discipline-skill | 4 | 3 | 2 | 9 |
| 6 | tips-and-authority-defense-skill | 4 | 3 | 2 | 9 |
| 7 | stock-sector-behavior-skill | 4 | 3 | 2 | 9 |
| 8 | liquidity-and-execution | 4 | 3 | 2 | 9 |
| 9 | forecast-log | 4 | 3 | 2 | 9 |
| 10 | livermore-rules-checklist | 4 | 3 | 2 | 9 |
| — | **合计** | **40** | **30** | **20** | **90** |

- 30 条诱饵中 **29 条为跨卡混淆题**（应触发同包另一张卡），1 条为 out-of-scope 一般诱饵（trend-snt-03，期货操作）；每卡满足"至少 1 条跨卡混淆"的硬性要求。
- 20 条 edge_case 覆盖三类边界：B 段反场景、A 股制度边界（涨跌停/T+1/跌停）、缺行情/缺输入的"先询问而非编造"。

### 输出用例（output-cases.json）：合计 22 条

| # | 能力卡（capability_id 尾段） | 正常 | 边界/缺输入 | 小计 | 覆盖代表任务 |
|---|---|---|---|---|---|
| 1 | min-resistance-trend-skill | 1 | 1（缺行情→询问） | 2 | task-01/02 |
| 2 | key-point-trading-skill | 1 | 1（涨停确认滞后） | 2 | task-03/05 |
| 3 | probe-and-scale-in-skill | 1 | 1（亏损补仓→终止） | 2 | task-04/07 |
| 4 | position-holding-exit-skill | 1 | 2（缺大势→询问；跌停预案） | 3 | task-06/07 |
| 5 | mind-state-discipline-skill | 1 | 1（非心理治疗边界） | 2 | task-13/14 |
| 6 | tips-and-authority-defense-skill | 2 | 1（缺消息原文→询问） | 3 | task-10/11/12 |
| 7 | stock-sector-behavior-skill | 1 | 1（成员不足→降级） | 2 | task-08/09/12 |
| 8 | liquidity-and-execution | 1 | 1（缺成交量→询问） | 2 | task-16 |
| 9 | forecast-log | 1 | 1（模糊预测→询问） | 2 | task-02/03 |
| 10 | livermore-rules-checklist | 1 | 1（拒绝优先级排序） | 2 | task-18 |
| — | **合计** | **11** | **11** | **22** | task-01～18 中 13 项 |

每个 active 能力 ≥ 2 条（1 正常 + 1 边界/缺输入），符合方法论最低要求；三张 critical 卡（position / tips）各加 1 条补充场景。

## 3. 覆盖矩阵（能力 × 用例类型）

| 能力卡 | st 正面 | snt 跨卡 | snt 一般 | edge 反场景 | edge A股制度 | edge 缺输入 | out 正常 | out 边界 |
|---|---|---|---|---|---|---|---|---|
| min-resistance-trend-skill | 4 | 2 | 1 | 1 | — | 1 | 1 | 1 |
| key-point-trading-skill | 4 | 3 | — | 1 | 1 | — | 1 | 1 |
| probe-and-scale-in-skill | 4 | 3 | — | 1 | — | 1 | 1 | 1 |
| position-holding-exit-skill | 4 | 3 | — | 1 | 1 | — | 1 | 2 |
| mind-state-discipline-skill | 4 | 3 | — | 1 | — | 1 | 1 | 1 |
| tips-and-authority-defense-skill | 4 | 3 | — | 1 | — | 1 | 2 | 1 |
| stock-sector-behavior-skill | 4 | 3 | — | 1 | — | 1 | 1 | 1 |
| liquidity-and-execution | 4 | 3 | — | — | 1 | 1 | 1 | 1 |
| forecast-log | 4 | 3 | — | 1 | — | 1 | 1 | 1 |
| livermore-rules-checklist | 4 | 3 | — | 2 | — | — | 1 | 1 |

说明：
- edge 列按主边界归类（一题可兼含多重边界，如 checklist-edge-02 同时是反场景与收益承诺停止条件）。
- 出题依据：每卡的 A2 触发场景与语言信号（正面题）、A2"与相邻能力的区分"（跨卡诱饵）、B 段与 E 段输入契约（边界题）。

## 4. 跨卡混淆题清单（29 条，测哪对卡的区分线）

| 用例 id | 诱饵表面问题 | 应触发的正确卡 | 区分线（出题依据） |
|---|---|---|---|
| min-resistance-trend-skill-snt-01 | 要具体买入价位 | key-point-trading-skill | 趋势卡停在"方向＋时机闸门"，价位归关键点 |
| min-resistance-trend-skill-snt-02 | 浮盈止盈/移动止损 | position-holding-exit-skill | 动手后拿多久、怎么退出归头寸卡 |
| key-point-trading-skill-snt-01 | 大盘牛熊方向 | min-resistance-trend-skill | 关键点的前提是趋势状态已判 |
| key-point-trading-skill-snt-02 | 突破后分批买多少 | probe-and-scale-in-skill | 价位触发归关键点，建仓顺序归建仓程序 |
| key-point-trading-skill-snt-03 | "主力埋伏"说法可信吗 | tips-and-authority-defense-skill | 消息文本可信度归信息防御 |
| probe-and-scale-in-skill-snt-01 | 该等什么价位动手 | key-point-trading-skill | 建仓程序的前置触发归关键点 |
| probe-and-scale-in-skill-snt-02 | 翻本/为账单搏一把 | mind-state-discipline-skill | 加仓冲动背后的动机归心理卡 |
| probe-and-scale-in-skill-snt-03 | 800 万买小票进得去吗 | liquidity-and-execution | 单量可行性归流动性卡 |
| position-holding-exit-skill-snt-01 | 首笔买多少、怎么加 | probe-and-scale-in-skill | 首笔之前的问题归入场卡 |
| position-holding-exit-skill-snt-02 | 持仓失眠心慌 | mind-state-discipline-skill | "为什么拿不住"的内在状态归心理卡 |
| position-holding-exit-skill-snt-03 | 大盘是牛是熊 | min-resistance-trend-skill | 大势判定是头寸卡的前置，本身归趋势卡 |
| mind-state-discipline-skill-snt-01 | 止损挂多少、怎么卖 | position-holding-exit-skill | 仓位动作规则归头寸卡 |
| mind-state-discipline-skill-snt-02 | 内部人士截图可信吗 | tips-and-authority-defense-skill | 外来信息归信息防御，内在状态归心理卡 |
| mind-state-discipline-skill-snt-03 | 补仓违反哪条规则 | livermore-rules-checklist | 动作 vs 条文检索归清单卡 |
| tips-and-authority-defense-skill-snt-01 | 板块独跌无消息 | stock-sector-behavior-skill | 有消息文本→信息防御；只有行情异常→甄别卡 |
| tips-and-authority-defense-skill-snt-02 | 突破 9.8 该不该追 | key-point-trading-skill | 技术点位归关键点，信息卡不判形态 |
| tips-and-authority-defense-skill-snt-03 | 听消息后焦虑失眠 | mind-state-discipline-skill | 听消息后的情绪归心理卡 |
| stock-sector-behavior-skill-snt-01 | 大盘牛熊确认 | min-resistance-trend-skill | 板块卡只做个股/板块交叉验证 |
| stock-sector-behavior-skill-snt-02 | 政策利好文章可信吗 | tips-and-authority-defense-skill | 有消息文本→信息防御（补涨叙事恰是甄别卡警示的陷阱） |
| stock-sector-behavior-skill-snt-03 | 龙头持仓怎么拿怎么走 | position-holding-exit-skill | 甄别卡出信号，处置动作归头寸卡 |
| liquidity-and-execution-snt-01 | 该拿还是该卖、留几成 | position-holding-exit-skill | 决定层归头寸卡，可行性层归流动性卡 |
| liquidity-and-execution-snt-02 | 13 块算不算有效突破 | key-point-trading-skill | 流动性卡不管价位 |
| liquidity-and-execution-snt-03 | 建仓计划与判停 | probe-and-scale-in-skill | 建仓顺序归建仓程序卡 |
| forecast-log-snt-01 | 怎么判趋势结构 | min-resistance-trend-skill | 日志只记录计分，不提供判读方法 |
| forecast-log-snt-02 | 亏损归因＋戒律 | mind-state-discipline-skill | 日志止于对错判定，归因归心理卡 |
| forecast-log-snt-03 | 列铁律贴屏幕 | livermore-rules-checklist | 动作条文清单归清单卡 |
| livermore-rules-checklist-snt-01 | 规则背得出做不到 | mind-state-discipline-skill | 清单查动作，情绪动机归心理卡 |
| livermore-rules-checklist-snt-02 | 第 5 条落到具体止损 | position-holding-exit-skill | 条文命中后的操作细节按检索表转介 |
| livermore-rules-checklist-snt-03 | 怎么判总体市场涨跌 | min-resistance-trend-skill | 条文背后的深度方法归对应深度卡 |
| （trend-snt-03） | 期货做空 | （无，out-of-scope） | 一般诱饵：期货直接操作超出本书范围 |

覆盖的相邻卡对（无序对）：trend↔key-point、trend↔position、trend↔sector、trend↔forecast、trend↔checklist、key-point↔probe、key-point↔tips、key-point↔liquidity、probe↔mind、probe↔liquidity、position↔mind、position↔tips、position↔sector、position↔liquidity、mind↔tips、mind↔checklist、mind↔forecast、sector↔tips、sector↔forecast（经 forecast-snt-03）、checklist↔forecast、checklist↔position——共 19 对，覆盖 verified.yaml 中全部 `also_read` 相邻关系。

## 5. 盲测执行说明

**核心原则：盲测者只读 prompt 文本。** 隐藏 `type / expected_behavior / notes` 与一切预期答案；不把主流程的判断带给执行 agent。

### 5.1 触发精度盲测（test-prompts.json）

1. 对每条测试 prompt 启动一个干净的 sub-agent（资源有限时可对同卡一组 prompt 用一个干净 sub-agent）。
2. **只给 sub-agent**：本包全部 10 张能力卡 + 入口的 name + description 列表（取自 `verified.yaml` 的 frontmatter.description）、用户 prompt。**不给**：type、expected_behavior、notes、通过标准、任何卡的 A2/B 段原文。
3. 要求 sub-agent 输出三字段：`would_trigger`（激活哪张卡/哪个入口/不激活）、`reason`、`if_triggered_action`。
4. 主流程判卷：
   - `should_trigger`：sub-agent 须明确激活本卡，且 if_triggered_action 符合 expected_behavior；
   - `should_not_trigger`：**容错为 0**——不得激活本卡；跨卡混淆题中，激活包内其他卡＝该题通过，激活本卡＝失败；
   - `edge_case`：判断须符合 expected_behavior 定义的边界理由（如"拒答预测""先询问""声明约定"）。
5. 按"测试前固定的验收标准"分类汇总；重要负例（跨卡混淆）、关键计算、必需交付物不得用平均分掩盖；缺失样本不从分母排除。
6. 与 `schemas/eval-suite.schema.json` 的映射：`type=should_not_trigger` 且 notes 指明目标卡者，对应 schema 的 `expected="sibling"`＋`sibling_target`；其余一一对应。如需机械跑分与 train/validation 切分（60/40、固定种子 42，validation 在选版前保持隐藏），可转换后交 `scripts/run_trigger_evals.py`。

### 5.2 输出评测（output-cases.json）

1. 建议命令：`python3 scripts/run_output_evals.py prepare <suite> --out <run-dir>`，每个任务在 `<case_id>/<label>/` 中执行，回答写 `output.md`。
2. 执行者**只读每条用例的 `task` 与 `inputs`**，不看 checks / boundary_note / expected；固定同一宿主、模型、工具与预算，分别运行 `old_skill / new_skill / without_skill`（首次无旧版可只比后两者），独立工作目录、干净上下文。
3. 断言语义（checks）：
   - `must_include`：列表内**每条**字符串都须出现在输出中（AND、子串匹配）；
   - `must_not_include`：任一出现即违规；
   - `structure`：`regex:` 前缀者为正则匹配，其余为必备要素/表格描述（无法机械判定处转人工核查，不得只问模型"会不会做"）。
   - 映射到 schema 断言 kinds：must_include→`contains`、must_not_include→`not_contains`、structure→`regex`/`file_exists`。
4. 先机械断言、后盲评语义；退出码语义与汇总口径按方法论（计划数/完成数/全部断言通过数/失败原因/耗时/Token）。
5. 数值输入均自洽可复算，评分器可直接核对（示例见 §6）。

### 5.3 判分后动作

- 失败 case 暴露 trigger 描述歧义→修 skill（回炉 A2/E/B，不是改 description 措辞）；
- 失败 case 是此前未想到的合理场景→修 skill 覆盖或明确排除；
- 为凑诱饵设计过狠→修测试并记录理由；修改预期答案须独立理由与审计记录。
- 已看过的失败用例加入回归集；最终验收用未参与调优的保留用例，记录宿主/模型版本与运行条件。

## 6. 机械断言示例（output-cases.json）

1. **建仓比例**（probe-and-scale-in-skill-out-01）：输入"计划建仓 10000 股"→ `must_include: ["2000", "1/5"]`——首笔试探仓必须等于总额度 × 1/5 ＝ 2000 股，多一字股或少一字股即不通过；同时 `structure` 要求建仓档案占比合计 100%、`regex:(亏损|首笔错).*(终止|不加|停止)` 判停分支必须在场。
2. **成交量占比**（liquidity-and-execution-out-01）：输入"买 50 万股、日均成交 2500 万股"→ `structure: "regex:2\\s*%"`——占比 50 万 ÷ 2500 万 ＝ 2%，输出须给出该数值并触发分批与胃口测试（`regex:(试探单|测试单|试盘)`）；"一次性买入 50 万股"被 `must_not_include` 禁止。
3. **失效位价位**（key-point-trading-skill-out-01 / out-02）：输入"横盘区间 11.20—12.00、今收 12.60（或涨停 12.98）"→ `must_include: ["11.20", "12.00", "12.60", "失效"]`——失效位必须落在跌回 12.00 之下（跌回起涨关键点即判整轮行情假象），报价 11.80 × 1.10 ＝ 12.98 的涨停例还必须包含"次日""约定"（封板当日不可确认）。

## 7. 已知边界与注意

- 所有行情/持仓数字均为虚构但自洽（如 11.80 × 1.10 ＝ 12.98 涨停、15.60 × 0.90 ＝ 14.04 跌停、50 万 ÷ 2500 万 ＝ 2%），可复算。
- prompt 均为自然用户口语（中文为主、少量夹带英文 trigger 词），不含能力卡名称，不泄露 expected 字段内容；诱饵均为真实感场景，无一眼假的荒诞题。
- 本套件未执行；`test-results.md` 待盲测完成后另行产出（审计用），并须标注是否为独立 sub-agent 盲测或 fallback 主流程自测。
