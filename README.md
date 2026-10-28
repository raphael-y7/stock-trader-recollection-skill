<h1 align="center">股票大作手回忆录 Skill</h1>

<p align="center">中文 | <a href="README.en.md">English</a></p>

一套可直接使用的 AI skill 工具包——把埃德温·勒菲弗《股票大作手回忆录》里利弗莫尔的实战方法论，蒸馏成 10 张可单独触发、也可组合调用的能力卡：从趋势判读、关键点入场、试探建仓、头寸持有与退出，到交易心理自检、贴士与权威信息防御、板块与个股行为甄别。

它不是原书摘要，也不是读后感，而是把书中可复用的方法论拆成可触发、可执行、可测试的 skill 模块。

## 这套 skills 能解决什么问题

- 看对了方向却总在错的位置动手：横盘里手痒先买，真突破了又不敢追
- 被套之后想「补仓摊低成本」，浮盈又急着落袋——两个动作正好把亏损做大、把盈利做小
- 收到荐股、小作文、大 V 或「接近内部人」的利好，不知道该信还是该躲
- 持仓下跌时用「主力洗盘 / 空头打压」安慰自己，分不清是合理下跌还是话术
- 同板块都涨就自己那只不涨，想埋伏等补涨；龙头开始滞涨，又不知道是不是行情完了
- 连亏之后想立刻翻本，或带着「这个月必须挣出××」的账单压力下单，事后才承认当时根本不在状态

## 蒸馏了什么

10 张能力卡，按「先定方向与时机、再管仓位与纪律、最后防外部信息」的顺序组织。下列 slug 与 `bundle/verified.yaml` 的 10 个能力一一对应（`-skill` 后缀是规范化 slug 的一部分）：

- **方向与时机**（2 张）：`min-resistance-trend-skill`（最小阻力路线趋势判读）、`key-point-trading-skill`（关键点体系）
- **建仓与持仓程序**（2 张）：`probe-and-scale-in-skill`（试探—验证—加码建仓程序）、`position-holding-exit-skill`（头寸管理：持有、跟进与退出）
- **内功与信息防御**（2 张）：`mind-state-discipline-skill`（交易心理与状态自检）、`tips-and-authority-defense-skill`（贴士与权威信息防御）
- **选股与执行**（2 张）：`stock-sector-behavior-skill`（个股与板块行为甄别）、`liquidity-and-execution-skill`（流动性与执行）
- **校准与规则**（2 张）：`forecast-log-skill`（判断校准预测日志）、`livermore-rules-checklist-skill`（利弗莫尔成文规则总表）

合计 2 + 2 + 2 + 2 + 2 = 10 张。其中 7 张在 pack 里晋级为独立入口，3 张（`liquidity-and-execution-skill`、`forecast-log-skill`、`livermore-rules-checklist-skill`）只由路由入口调用——它们意图独立，但书中证据较薄或使用频率低，做成独立入口反而会稀释触发精度。每张卡的完整判据、原文依据、书中案例、触发场景、可执行步骤与边界盲点，都在 `bundle/cards/` 的对应文件里。

## 两种打包模式：single 与 pack

同一套 10 张能力卡，按两种粒度各编译了一次。两者内容完全相同，区别只在「agent 能看到几个入口」。

| | single（单一入口） | pack（compact pack，多入口） |
|---|---|---|
| 可发现入口 | **1 个**：`stock-trader-recollection-skill` | **8 个**：1 个来源路由入口 + 7 个已晋级独立 skill |
| 10 张能力卡放在哪 | 全部在入口的 `references/capabilities/` 里，由入口按路由表按需加载 1–2 张 | 7 张晋级卡把整张能力卡（R / I / A1 / A2 / E / B 六段）编进各自的 `SKILL.md`；其余 3 张只在 router 的 `references/` 里 |
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

### 该装哪一种

按你的工作方式选，**只装一种**：

| 你的工作方式 | 推荐 | 原因 |
|---|---|---|
| 用 DSH / Codex / Claude Code 等有 skills 目录，希望列表干净 | single | 只占 1 个入口，能力一张不少 |
| 日常问题高度集中在「现在能不能动手 / 这消息能不能信 / 浮盈该不该止盈 / 心理状态」 | pack | 这几类正是被晋级的独立 skill，能直接命中 |
| 要分发给多个 agent 或团队，各自按需取用 | pack | 可以只装其中几个独立 skill，不必整包 |
| 只想装一次、不想维护多个目录 | single | 升级时只替换 1 个目录 |

> 两版由同一个 Bundle 编译，能力内容一致。**同时安装会重复触发**，请只装一种。

## 效果示例

### 示例 1：横盘一个多月，先埋伏还是等突破

**用户问题**

「这票在 12 块到 13 块之间横了一个多月，现在 12.6，看着像要往上走，我先买一点埋伏着行不行？」

**skill 如何判断**

- 先过 `min-resistance-trend-skill`：按高低点结构判读，这是一段横向市——横向市不出方向结论，只记录区间上下极限，所以「看着要往上走」这个判断本身不成立
- 进 `key-point-trading-skill`：建关键点清单（区间上沿、下沿、整数关、前高前低），当前价在区间内 → 走判停分支「观望 / 不沾手」，输出向上突破买、向下跌破回避的待命触发价
- 突破确认按 A 股口径换算：涨跌停封板当日无法验证真假，约定「收盘站上 / 跌破 + 次日不跌回」为确认（**约定，非原书口径**，原书语境是连续报价市场）
- 预设失效位：跌回起涨的那个关键点之下，即判整轮行情为假象，按市价离场，不解释、不等待
- 自检绝对价格：原书「首破 100 / 200 / 300 美元整数关续涨 30—50 点」是 1920s 美股单案例归纳，只作结构参照；「12.6 比 13 便宜」不构成买入理由

**最终回答示例**

> 这段行情按本书口径叫横向市：价格在一个多月里没有走出明确方向，此时唯一正确的动作是不做——不是「先埋伏一点」，而是把区间上下沿记下来，等市场自己界定方向。所以先给你两个待命价：向上突破 13 那一带（要连着整数关和前高一起看）才谈买，向下跌破 12 就先回避。突破当天不急着认——A 股涨停封板那天你没法验证真假，按本仓库约定的口径，要「收盘站上 + 次日不跌回」才算确认，这条是我们换算的，原书没写。动手之前先把失效位写在纸上：跌回起涨的那个关键点之下，整轮就当假象，市价走人，别找理由。最后提醒一句：「现在 12.6 比 13 便宜」不是买入理由——原书对「太高不敢买、太低够便宜」有专门一条否决，价格高低本身不构成任何依据。

### 示例 2：朋友给的「内部消息」，能买吗

**用户问题**

「券商的朋友说这家公司下个月有重组，让我先埋伏进去，说消息很可靠。能买吗？」

**skill 如何判断**

- 进 `tips-and-authority-defense-skill`，走四道防御闸，第一步是盘面定序：先写出这只票当前的价格行为事实（涨跌、相对大盘与板块强弱），再允许讨论消息——原因是原因可以后追，处置不能等
- 第二道趋势过滤：消息只是趋势的放大器。若这是出利好却不涨、或逆着下跌趋势推不动的利好，判为「警惕」而非「机会」
- 第三道出场依赖链＋署名 / 时点 / 行为三重检验：这条消息谁署名？将来卖出由谁决定？该来源在你要卖的那一刻还在场、可追责吗？「下个月重组」既无署名也无责任主体，依赖链一断，采信就不成立
- 第四道下跌归因排障：跌了有人解释「主力洗盘 / 空头打压」时，默认先验是合理下跌（原书口径：100 例中 99 例），反证很简捷——真被打压到低于价值，买盘自然会止跌，不反弹就说明是话术；配套的行为核查要求看内部人实际增持减持，而 A 股只能从定期报告与公告里看、时效滞后，卡里要求明确声明「数据不可得」，不许用常识冒充
- 判停：匿名或不可追责的利好默认不能作为买入依据；用户若坚持要买，转 `position-holding-exit-skill` 处理仓位与止损，本卡不决定仓位大小

**最终回答示例**

> 先把它当一条待检验的信息，不是一条买入理由。三个问题按顺序问：一，这条消息有署名吗、谁为它负责？「券商的朋友」不是责任主体，重组这种级别的事一旦成立必然有公告，没有公告就先按传言处理。二，将来你靠什么卖？如果买进靠这条消息、卖出还得靠同一个人再告诉你一次，这条链迟早在你最需要的时候断掉——原书对这个结构有专门的判断，叫出场依赖链。三，盘面怎么说？先看它最近的涨跌和相对板块强弱，如果消息满天飞而股价不涨，那本身就是答案。所以结论是：这条消息暂不采信，也不建议因此建仓；真要参与，只能按「没有这条消息」的方式参与——用关键点体系等它自己突破，用头寸管理卡定仓位和止损。另外说明一点：A 股看不到实时内部人买卖，只能等定期报告，这一层本卡只能标注「数据不可得」，不会替你补。

## 这些 skill 是怎么生成出来的

这套 skill 使用 **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** 的 RIA-TV++ 流水线生成，整个流程分六个阶段：

1. **整书理解（Adler 分析）**——用 Mortimer Adler 的分析阅读法，对全书做结构、解释、批判、应用四步拆解，产出一份整书理解文档作为后续所有提取的全局上下文
2. **并行提取**——同时派多个专项提取器（框架、原则、案例、反例、术语），从原文中提取候选方法论单元
3. **三重验证筛选**——每个候选必须通过三项检验：书内至少有 2 处独立佐证（跨域）、能回答书中未明说的新问题（预测力）、不是常识（独特性）
4. **RIA++ 构造**——按 R（原文引用）/ I（用自己的话重写）/ A1（书中案例）/ A2（未来触发场景）/ E（可执行步骤）/ B（边界与盲点）六个维度结构化
5. **Zettelkasten 链接**——找出能力卡之间的依赖、对比、组合关系，生成能力索引与路由表
6. **触发与输出测试**——为每张卡设计触发盲测题（含诱饵题：该触发时要触发，不该触发时要沉默）与输出评测场景，未通过的卡回炉重做，回炉后再做回归验证

这本书的特殊性也影响了蒸馏：它是一本访谈体传记，方法论藏在故事里而不是章节标题里，所以提取阶段按「传主的一次具体操作 → 可复用的判据 → 可执行的步骤」逐段回填；同时所有方法都带 1920s 美股语境（纸带、对赌行、无涨跌停、可裸卖空），凡涉及执行的卡都加了 A 股制度换算与「约定」标注，不静默编造原书没有的参数。整书理解的产出在 `BOOK_OVERVIEW.md`，三重验证结论在 `verified.md`，规范化定义在 `bundle/verified.yaml`。

## 测试与验证

本仓库连生成过程的测试材料一起发布：测试材料见各 skill 目录下的 `test-prompts.json`——入口级 90 条触发用例在 `single/stock-trader-recollection-skill/`，pack 下 7 个晋级 skill 各有 9 条专属用例；逐项评分记录在仓库根目录 `test-results.md`，包含失败与回炉修复的完整过程，不是只留通过记录。

- **触发精度**：90 条独立盲测，合计 86 / 90（95.6%）。其中 should_trigger 正向 40 / 40、跨卡混淆诱饵 29 / 29、一般诱饵 1 / 1，edge_case 16 / 20
- **一处真实失败并修复**：首轮正向为 39 / 40——「研报基本面与股价背离，该信谁」被误路由到信息防御卡。判定为修 skill：两卡 description 在「消息与盘面背离」上重叠，趋势卡显式接住「已核实的业绩/行业形势与背离」，信息防御卡收窄为「事件性消息/传闻辨伪」，独立复测通过
- **输出质量**：22 / 22 用例通过（每个能力至少 1 条正常 + 1 条边界或缺输入），机械断言 22 / 22，判分器前三版假阳性已逐条人工复核确认；完成方式分布为正常完成 12、判停询问 7、拒绝误用 3
- **判停维度**：该拒答时拒答（摊平指令、横盘埋伏、规则排序），该追问时追问（缺标的、缺关键价位、缺消息原文），不硬给结论
- **如实记录的局限**：每用例单次运行，未做多轮稳定性测试；无旧版基线与不带 skill 的对照组；触发盲测基于 description 文本，未在真实宿主 skill 机制上验证；90 条未切分 train / validation。4 条 edge 用例属路由层与输出层的语义争议，已按「激活后拒答」重新归类并在输出评测中覆盖

## 仓库结构

```text
stock-trader-recollection-skill/
├── README.md              ← 你正在看的
├── README.en.md           ← English version
├── LICENSE                ← MIT
├── BOOK_OVERVIEW.md       ← 阶段 0 产出：全书 Adler 分析
├── DIGEST.md              ← 阶段 5 产出：面向读者的整书精华长文
├── INDEX.md               ← 阶段 3 产出：skill 总览 + 依赖关系
├── verified.md            ← 通过三重验证的 81 条判定（23 个合并组 → 10 个能力单元）
├── TEST_SUMMARY.md        ← 阶段 4 产出：压力测试摘要
├── CANGJIE_ADAPTATION.md  ← 仓颉适配说明
├── GITHUB_REPO.md         ← 仓库元数据
├── test-results.md        ← 测试结果记录
├── candidates/            ← 阶段 1 产出：原始候选池
│   ├── frameworks.md      ← 框架与方法候选
│   ├── principles.md      ← 原则 / 规则 / 计算候选
│   ├── cases.md           ← 书中案例候选
│   ├── counter-examples.md← 反例与边界候选
│   └── glossary.md        ← 术语候选
├── rejected/              ← 阶段 1.5 产出：被淘汰的单元 + 原因
├── bundle/                ← 编译事实源
│   ├── verified.yaml      ← 能力元数据、判据与去向
│   ├── cards/             ← 能力卡源文件（六段结构）
│   └── book/              ← overview.md + glossary.md
├── single/                ← single 模式（1 个入口 + 全部能力卡）
│   └── stock-trader-recollection-skill/SKILL.md  ← 入口：触发 + 路由表 + 加载规则
└── pack/                  ← pack 模式（1 个路由入口 + 7 个晋级 skill）
    └── */SKILL.md         ← 8 个 skill（1 个路由入口 + 7 个晋级 skill），每个附带 test-prompts.json
```

## 如何使用

把仓库克隆或下载到本地后，在仓库根目录执行下面的命令。

### 装 single（推荐先试这个）

```bash
# macOS / Linux
cp -r single/stock-trader-recollection-skill ~/.agents/skills/
```

```powershell
# Windows
Copy-Item -Recurse .\single\stock-trader-recollection-skill "$env:USERPROFILE\.agents\skills\"
```

### 装 pack

只复制含 `SKILL.md` 的目录，不要把 `pack/` 下的两个 json 一起拷进 skills 目录：

```bash
# macOS / Linux
cd pack
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
$pack = ".\pack"
$dest = "$env:USERPROFILE\.agents\skills"
@('stock-trader-recollection-skill-router','min-resistance-trend-skill','key-point-trading-skill','probe-and-scale-in-skill','position-holding-exit-skill','mind-state-discipline-skill','tips-and-authority-defense-skill','stock-sector-behavior-skill') |
  ForEach-Object { Copy-Item -Recurse -LiteralPath (Join-Path $pack $_) -Destination $dest }
```

> `~/.agents/skills` 是 DSH 的 skill 目录；用别的 agent 时换成它自己的 skills 目录即可（例如 Claude Code 是 `~/.claude/skills`）。

### 怎么确认装好了

装完问一句「这票横了一个月，现在能买吗」，看 agent 是否先判横向市、只给待命触发价而拒绝提前埋伏，而不是直接给你一个「可以轻仓试试」。装的是 single 时，它会先读入口再按路由表进能力卡；装的是 pack 时，对应能力会被直接命中。

## 来源

- 《股票大作手回忆录》埃德温·勒菲弗 著

## 声明

本仓库只发布蒸馏后的 skill、索引与规则速查材料，不包含原书 PDF、EPUB、OCR 文件、截图或全书转写稿。能力卡中出现的原文引用仅用于标注方法论出处和保持可审计性。

书中所有数字判据（1/5 首笔、1:1:2 加码梯度、10 / 20 点台阶、整数关续涨 30—50 点、100 例 99 例等）都是案例与经验归纳，原书未提供统计回测背书，且多为 1920s 美股制度下的产物；A 股使用需按 T+1、涨跌停、无裸卖空的制度边界换算，并声明所用口径。本仓库内容不构成投资建议。

## License

[MIT](./LICENSE)
