<h1 align="center">股票大作手回忆录 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把埃德温·勒菲弗《股票大作手回忆录》中利弗莫尔（书中化名"拉里·利文斯顿"）的实战方法论，蒸馏成 10 张可单独触发、也可组合调用的能力卡。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- 把"该看多还是看空"和"现在能不能动手"混成一件事——方向对了、时机没到，照样出局（1906 年看空美股却因过早卖空而破产）
- 横盘里手痒想提前埋伏，却说不清哪条线才算"确定无疑的突破"，也不知道突破失败时该在哪认错
- 一次买还是分批买、被套要不要补仓：书里唯一的量化建仓程序是首笔 1/5 试探、首笔有利润才加码、绝不摊平
- 浮盈拿不住、卖飞又追不回来——跟进止损该挂在哪、什么时候只能上移不能下移
- 连亏之后想翻本、为账单交易、仓位压到睡不着，却还在继续找下一个标的
- 一条荐股、一份研报、一句"这跌是空头打压"摆在面前，判断不了该信谁、该以盘面还是以消息为准

## 蒸馏了什么

10 张能力卡，按"先判方向、再定入场、然后建仓持有、最后守纪律"的顺序组织：

- **趋势与入场**：`min-resistance-trend-skill`（最小阻力路线趋势判读）、`key-point-trading-skill`（关键点体系）
- **建仓与持有**：`probe-and-scale-in-skill`（试探—验证—加码建仓程序）、`position-holding-exit-skill`（头寸管理：持有、跟进与退出）
- **心理与信息防御**：`mind-state-discipline-skill`（交易心理与状态自检）、`tips-and-authority-defense-skill`（贴士与权威信息防御）
- **甄别与工具**：`stock-sector-behavior-skill`（个股与板块行为甄别）、`liquidity-and-execution`（流动性与执行）、`forecast-log`（判断校准预测日志）、`livermore-rules-checklist`（利弗莫尔成文规则总表）

## 两种打包模式：single 与 pack

同一套 10 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在"agent 能看到几个入口"。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`stock-trader-recollection-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 10 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1–2 张 | 7 张卡各自独立成 skill；其余 3 张仍在 router 的 `references/` 里 |
| 触发方式 | 只有入口的 description 参与匹配，进入后靠路由表分流 | 7 个高频能力可被 description 直接命中，少一跳 |
| 升级维护 | 替换 1 个目录 | 替换 8 个目录 |

pack 里被晋级为独立 skill 的 7 张卡：

- `min-resistance-trend-skill` — 最小阻力路线趋势判读
- `key-point-trading-skill` — 关键点体系
- `probe-and-scale-in-skill` — 试探—验证—加码建仓程序
- `position-holding-exit-skill` — 头寸管理：持有、跟进与退出
- `mind-state-discipline-skill` — 交易心理与状态自检
- `tips-and-authority-defense-skill` — 贴士与权威信息防御
- `stock-sector-behavior-skill` — 个股与板块行为甄别

留在 router 里的 3 张卡：`liquidity-and-execution`（流动性与执行）、`forecast-log`（判断校准预测日志）、`livermore-rules-checklist`（利弗莫尔成文规则总表）。

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，10 张能力卡一张不少 |
| 日常问题高度集中在"趋势方向 / 关键点 / 分批建仓 / 持有与止损 / 心理自检 / 消息辨伪 / 板块甄别" | pack | 这 7 类正是被晋级的独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：突破整数关口，要不要追

**用户问题**

"这票在 8.6 到 9.8 之间横了两个月，今天冲到 9.9，突破了前高，是不是可以追？"

**skill 如何判断**

- 进 `key-point-trading-skill` 的 Step 1：先建关键点清单——区间上下限（9.8）、整数关（10 元）、前高前低，每项标价位、类型、来源
- Step 3 突破确认：核对"确定无疑"。原书语境是 1920s 连续报价市场，突破当场可见；A 股涨跌停制度下封板当日无法验证真假，该卡给的**约定**是"收盘站上／跌破＋次日不跌回"
- Step 4 预设失效位：进场前先写下来——跌回起涨关键点之下即判定整轮行情是假象，按市价离场
- Step 5 价格高低否决项：检查结论有没有被"太高了不敢买／跌这么多够便宜了"污染

**最终回答示例**

> 先别追，把清单列出来：9.8 是区间上沿，10 元是整数关，这两个价位性质不同——突破 9.8 只是离开区间，站上 10 元才是过整数关。按这张卡，突破要"确定无疑"才动手，但原书没有给出这个口径的量化定义（注疏也指出这是原书的缺口），A 股封板当日更验证不了，所以这里用约定口径：今天收盘站上 9.8、明天不跌回，才算确认。确认之后再进场，进场之前先把失效位写死：跌回 9.8 以下就是假象，按市价走，不解释不等待。另外提醒一句，原书那句"首破 100/200/300 美元整数关后常续涨 30—50 点"是 1920s 美股个案归纳，只能当结构参照，不能写进结论当承诺。区间宽度多少才算有效、要等几天，原书都没给，你这一轮用哪个口径请写进预案，否则同样的图形下次会忽认忽不认。

### 示例 2：首笔就亏了，要不要补仓摊低成本

**用户问题**

"我按计划先买了计划仓位的五分之一，结果买完就跌了 6%，现在补一笔把成本摊下来，可以吗？"

**skill 如何判断**

- 进 `probe-and-scale-in-skill` 的 Step 2——这是该卡的核心闸门：检查首笔账面盈亏。亏损＝判断被证伪，**程序当场终止，不存在补仓分支**
- 该卡同时给了摊平的反面案例：珀西·托马斯为"维持价格"从 6 万包一路加到 44 万包，同时卖掉盈利的小麦（错过约 800 万美元），亏掉十分之九以上本金
- 若首笔是盈利的，才进入 Step 3：只在盈利方向加、每笔成交价必须高于前一笔（"步步上涨"）
- Step 4 用成交散布验证承接：越买价越高＝承接健康；全堵在同一个价＝上方乏力，减量并卖出小部分测试市场反应

**最终回答示例**

> 不可以，而且这不是"谨慎一点"的问题，是程序已经判停了。这张卡的闸门写得很硬：首笔出现账面亏损，说明"开头便错，至少暂时是错的"，程序终止，不存在"跌了更便宜所以多买"的分支。摊平之所以被列为全书最强禁令，是因为它让亏损头寸反过来决定你的仓位——书里 44 万包棉花就是这么来的。现在该做的两件事：按退出规则处理这笔小仓（怎么设止损、怎么离场，转 `position-holding-exit-skill`）；然后问一句，这笔首笔亏损里有多少是"想快点赚回来"的情绪，那部分归 `mind-state-discipline-skill`。另外提醒两个口径：原书的"1/5"是**额度内**比例，不是占你账户资金的比例，别直接换算成总仓；A 股 T+1 下试仓当天认不了赔，首笔比例宜更小——这两条都是约定，不是原书给的数字。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

这本书是访谈体传记，蒸馏时多做了两件事：一是把散在 24 章叙事里的方法（1/5 试探、+10/+20 点台阶、赫恩 1 点跟进止损、阿纳康达 301 失效位）从故事里剥出来，二是为每条方法加上 1920s 美股语境的边界声明——T+1、涨跌停、无裸卖空这三条制度差异会改变执行细节，凡是原书没给的量化口径（"确定无疑的突破"怎么算、区间多宽算有效）一律标注为"约定"，不静默编造。

## 测试与验证

本仓库连生成过程的测试材料一起发布：`evals/test-prompts.json` 是 90 条触发用例，`evals/output-cases.json` 是 22 条输出用例，`evals/blind/` 是盲测记录，`evals/test-results.md` 是逐项评分与失败修复记录。

- **触发精度**：should_trigger 40 / 40、should_not_trigger（跨卡混淆诱饵）29 / 29、一般诱饵 1 / 1、edge_case 16 / 20，合计 86 / 90（95.6%）
- **一次真实修复**：首轮正向为 39 / 40——"研报基本面与股价背离，该信谁"被盲测员路由到了信息防御卡。原因是两张卡的 description 在"消息与盘面背离"上重叠；修法是趋势卡显式接住"已核实的业绩/行业形势与股价背离"并保留"纸带为准"，信息防御卡收窄为"事件性消息/传闻辨伪"，独立复测通过
- **4 条 edge 的处理**：趋势卡"预测明日涨跌"、心理卡"求情感陪伴"、预测日志"代生成预测"、规则卡"规则排序"这 4 条，盲测员都判不激活，理由与各卡 B 段边界一致。它们实际检验的是"激活后的拒答行为"而非"是否激活"，按方法论重新归类为边界输出用例，不计为触发失败
- **输出质量**：22 / 22 用例通过机械断言；完成方式分布为正常完成 12、判停询问（缺输入先问不编造）7、拒绝误用 3（摊平指令、横盘埋伏、规则排序）
- **如实记录的局限**：每个用例单次运行，未做多轮稳定性测试；首版交付，没有 without_skill 基线对照；触发盲测基于 description 文本（模拟编译后的 frontmatter），未在真实宿主 skill 机制上验证；90 条用例未切分 train / validation，后续调优时应按 60/40 切分并保留隐藏集

## 仓库结构

```text
stock-trader-recollection-skill/
├── README.md                      ← 你正在看的
├── README.en.md                   ← English version
├── LICENSE                        ← MIT
├── BOOK_OVERVIEW.md               ← 整书理解（Adler 四步拆解，阶段 0 产出）
├── verified.md                    ← 81 条候选的三重验证结论与 23 个合并组
├── single/                        ← 单一入口模式
│   └── stock-trader-recollection-skill/
│       ├── SKILL.md               ← 入口：触发条件 + 路由表 + 加载规则
│       ├── BUILD_MANIFEST.json    ← 编译清单与文件哈希
│       └── references/
│           ├── overview.md        ← 整书概览
│           ├── capability-index.md  ← 完整意图与关键词索引
│           ├── cheatsheet.md      ← 决策规则速查
│           ├── glossary.md        ← 术语表
│           └── capabilities/      ← 10 张能力卡
├── pack/                          ← 多入口模式（compact pack）
│   ├── BUILD_MANIFEST.json
│   ├── capability-destinations.json
│   ├── stock-trader-recollection-skill-router/
│   │   ├── SKILL.md               ← 来源路由入口
│   │   └── references/            ← 10 张卡 + 索引，供 router 内部调用
│   ├── min-resistance-trend-skill/
│   │   └── SKILL.md
│   ├── key-point-trading-skill/
│   │   └── SKILL.md
│   ├── probe-and-scale-in-skill/
│   │   └── SKILL.md
│   ├── position-holding-exit-skill/
│   │   └── SKILL.md
│   ├── mind-state-discipline-skill/
│   │   └── SKILL.md
│   ├── tips-and-authority-defense-skill/
│   │   └── SKILL.md
│   └── stock-sector-behavior-skill/
│       └── SKILL.md
└── evals/                          ← 触发与输出测试材料
    ├── README.md                   ← 测试套件说明与覆盖矩阵
    ├── test-results.md             ← 逐项评分、失败修复与局限声明
    ├── test-prompts.json           ← 90 条触发用例
    ├── output-cases.json           ← 22 条输出用例
    └── blind/                      ← 触发盲测记录
        ├── menu.json
        ├── batch1.md
        ├── batch2.md
        └── batch3.md
```

## 如何使用

先把仓库克隆下来：

```bash
git clone https://github.com/raphael-y7/stock-trader-recollection-skill.git
```

### 装 single（推荐先试这个）

```bash
# macOS / Linux
cp -r stock-trader-recollection-skill/single/stock-trader-recollection-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\stock-trader-recollection-skill\single\stock-trader-recollection-skill "$env:USERPROFILE\.agents\skills\"
```

### 装 pack

只复制含 `SKILL.md` 的目录，不要把 `pack/` 下的两个 json 一起拷进 skills 目录：

```bash
# macOS / Linux
cd stock-trader-recollection-skill/pack
cp -r stock-trader-recollection-skill-router \
      min-resistance-trend-skill \
      key-point-trading-skill \
      probe-and-scale-in-skill \
      position-holding-exit-skill \
      mind-state-discipline-skill \
      tips-and-authority-defense-skill \
      stock-sector-behavior-skill ~/.agents/skills/
```

```powershell
# Windows
$pack = ".\stock-trader-recollection-skill\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('stock-trader-recollection-skill-router','min-resistance-trend-skill','key-point-trading-skill','probe-and-scale-in-skill','position-holding-exit-skill','mind-state-discipline-skill','tips-and-authority-defense-skill','stock-sector-behavior-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` 是 DSH 的 skill 目录；用别的 agent 时换成它自己的 skills 目录即可（例如 Claude Code 是 `~/.claude/skills`）。

### 怎么确认装好了

装完问一句"我这笔首笔建仓亏了，能不能补一笔摊低成本"，看 agent 是否直接进入 `probe-and-scale-in` 的判停流程、明确告诉你"程序终止、不存在补仓分支"，而不是给你一段泛泛的仓位管理建议。装的是 single 时，它会先读入口再按路由表进能力卡；装的是 pack 时，对应能力会被直接命中。

## 来源

- 《股票大作手回忆录》埃德温·勒菲弗 著
- 全书蒸馏，共产出 10 张能力卡

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有数字判据（首笔 1/5 比例、+10/+20 点加码台阶、1 点跟进止损、整数关后 30—50 点续涨等）都来自 1920s 美股的个案叙事，原书未提供统计回测背书；A 股 T+1、涨跌停、无裸卖空三项制度差异会改变执行细节，凡本仓库自行设定的口径均标注为"约定"。这本书记录的方法出自一位五次破产、最终于 1940 年破产离世的交易者，规则本身不保证盈利。本仓库内容不构成投资建议。

## License

[MIT](https://opensource.org/licenses/MIT)
