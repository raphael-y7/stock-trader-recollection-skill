# verified 汇总（阶段 1.5 产出）

> 汇总范围: verify/verify-framework.md（verified 32）+ verify/verify-principle.md（verified 49），合计 **81 条**
> 判定来源: 三重验证（task-first-v2）逐条通过 V1/V2/V3，完整记录见 verify-framework.md 与 verify-principle.md；本文件保留每条的 V1/V2/V3 结论与出处（压缩格式），供阶段 1.6 编译使用。
> 合并说明: 跨文件重复按 verify 文件标注的合并建议归入 23 个合并组（M01–M23），组成员 id 已注明；阶段 1.6 按组建能力单元，组内 p 类候选（引文与数字口径）并入对应 f 类框架作证据层，不重复建能力。**合并只影响编译组织，81 条判定全部有效。**

## 合并组总览

| 组 | 组名（能力方向） | 主条目 | 成员 id | 合计 | 对应 task |
|---|---|---|---|---|---|
| M01 | 趋势判读（最小阻力路线+三分类+跟随） | f01 | p33, f33, p64, p66, p67 | 6 | task-01/02 |
| M02 | 方向与时机两项评估（时机独立变量） | f03 | p34, p28, p29 | 4 | task-01/03 |
| M03 | 关键点体系（横盘区间+定义+整数关+失效） | f02 | p35, p41, f05, p30, p31, p26 | 7 | task-03/05 |
| M04 | 大势优先与牛市持有（"这是牛市"） | f04 | p15, p16, p18, p19, p50 | 6 | task-01/06 |
| M05 | 试仓—验证—加码建仓程序 | f06 | f07, p22, p23, p24, p25, p36, p37 | 8 | task-04 |
| M06 | 跟随止损体系（帕特·赫恩） | f28 | p38 | 2 | task-04/07 |
| M07 | 止损与退出纪律 | f30 | p44, p32, p52, p02 | 5 | task-07 |
| M08 | 心理自检（希望恐惧/账单/仓位压力） | f08 | f29, p39, p43 | 4 | task-13 |
| M09 | 信息辨别与权威防御 | f09 | p11, p54, p45, p46, p63, f17, f44, f42 | 9 | task-11 |
| M10 | 内部人行为与板块一致性 | f14 | f15, p49, p56, p57 | 5 | task-08/09/12 |
| M11 | 下跌归因排障（"空头打压"） | f16 | p51, p62 | 3 | task-10 |
| M12 | 行为证据优先于言语 | f45 | — | 1 | task-11/12 |
| M13 | 错误复盘转化程序 | f18 | — | 1 | task-13/14 |
| M14 | 交易状态与资金生存 | f19 | f21, p47, p48 | 4 | task-14 |
| M15 | 可交易性判定 | f23 | p08 | 2 | task-15 |
| M16 | 牛熊转换分阶段过渡 | f24 | — | 1 | task-08 |
| M17 | 流动性与执行（市场胃口+执行偏差） | f25 | p09 | 2 | task-16 |
| M18 | 心态与立场（不与纸带争辩/只站正确一边） | f32 | f39 | 2 | task-01/13 |
| M19 | 基本形势与方法分层 | f40 | f36, p42 | 3 | task-01 |
| M20 | 股票习性过滤 | f13 | p20 | 2 | task-08/09/12 |
| M21 | 判断校准（预测日志） | f11 | — | 1 | task-02/03 |
| M22 | 成文规则总表（附录二 15 条+封底 6 条） | p65 | p68 | 2 | task-18 |
| M23 | 盘面优先即时行动 | p07 | — | 1 | task-10/11 |

## 逐条记录

```yaml
- id: f01
  title: 最小阻力路线（趋势方向判定总框架）
  type: framework
  group: M01
  tasks: [task-01, task-02]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1720（第10章）；L1738/L2487/L1357 佐证"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "横盘→突破→顺向的完整决策链演练通过", boundary: "无量能参数；最小阻力路线是判定结论而非公式，判读质量依赖 f33"}
  V3_task_utility: {passed: true, benefit: "task-01 总纲；把价格高低排除出买卖理由，减少锚定偏差"}
  merge_note: "组 M01 主条目；p33（原则面）、p64（转变跟随）、p66/p67（附录三定义与模式）并入作证据层"

- id: p33
  title: 价格沿最小阻力路线运动
  type: principle
  group: M01
  tasks: [task-01, task-02]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1720（第10章）；封底 L3655 互证"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "决策依据（阻力对比决定方向）明确；判读操作由 f01/p66/p67 承载"}
  V3_task_utility: {passed: true, benefit: "全书核心理论锚点；为 A 股趋势判定提供统一语言"}
  merge_note: "并入 M01/f01；封底六原则第 3 条"

- id: f33
  title: 趋势定义三分类判读（更高/更低高低点）
  type: framework
  group: M01
  tasks: [task-02]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L3607/L3613/L3625（附录三）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "对任意 K 线序列可机械三分类", boundary: "'明显可辨'阈值为定性+举例，随周期自定"}
  V3_task_utility: {passed: true, benefit: "task-02 操作化定义，f01 的落地判据"}
  merge_note: "组 M01 成员；与 p66 同源（p66 为丁注 calculation 面）"

- id: p66
  title: 趋势定义三分类与"更高/更低"的辨识阈值
  type: calculation
  group: M01
  tasks: [task-02]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L3607-3613（附图 3.1-3.3）；L3625（0.5%/5% 感知举例）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "三分类判定可复算", boundary: "0.5%/5% 仅为感知举例，不得写成硬阈值"}
  V3_task_utility: {passed: true, benefit: "技术分析原点；A 股指数/个股状态三分类语言"}
  merge_note: "并入 M01/f33"

- id: p64
  title: 趋势转变无需等待解释，跟随即可
  type: rule
  group: M01
  tasks: [task-01, task-02]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L3467（第24章）；附录三 L3603 指认为趋势定义"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "结构判定（连续买进+小幅回落 vs 逐步下降+偶尔回升）与动作明确"}
  V3_task_utility: {passed: true, benefit: "'不需要解释'直接对治找理由拖延离场"}
  merge_note: "并入 M01/f01+f33"

- id: p67
  title: 行情演变的基本模式：密集区与突破交替
  type: principle
  group: M01
  tasks: [task-01, task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "附录三 L3633-3635；L3557（倒水试验）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "划分密集区/突破段并定位当前位置；'事后合理解释'≠'当时知晓'"}
  V3_task_utility: {passed: true, benefit: "为'突破才动手'提供机制理解，防密集区内预测方向"}
  merge_note: "并入 M01/f01"

- id: f03
  title: 纸带阅读两项评估：怎样交易＋何时交易（时机是独立变量）
  type: framework
  group: M02
  tasks: [task-01, task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1718（第10章）；L1399（第8章，看对熊市过早卖空反例）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "两步决策（方向+时机闸门）演练通过"}
  V3_task_utility: {passed: true, benefit: "把时机检查强制插入下单前流程；T+1 下减少冲动单"}
  merge_note: "组 M02 主条目；p34/p28 并入"

- id: p34
  title: 读纸带只做两项评估：怎样交易、何时交易
  type: principle
  group: M02
  tasks: [task-02, task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1718（第10章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "分析产出格式可检验（两项之外=越界）"}
  V3_task_utility: {passed: true, benefit: "划定价格行为分析的功能边界，防算命式预测"}
  merge_note: "并入 M02/f03"

- id: p28
  title: 时机是独立变量：头寸对、做法错照样破产
  type: principle
  group: M02
  tasks: [task-03, task-05]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1391（第8章）、L1409（发动机回火）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "抑制立即行动，等下跌动能确认再动手"}
  V3_task_utility: {passed: true, benefit: "'看对做错'归因于第二把锁；对治抢反弹抄底/抢跑"}
  merge_note: "并入 M02/f03；案例面 ce01（reference）"

- id: p29
  title: 等待市场自我界定的信号再动手
  type: rule
  group: M02
  tasks: [task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1415/L1423（第8章增发广告）；L2435（第14章全速前进铃声）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "有无市场确认信号可判定，动作（等待/行动）明确"}
  V3_task_utility: {passed: true, benefit: "'等市场先表态'减少 T+1 冲动单的不可逆成本"}
  merge_note: "并入 M02/f03（确认信号机制）"

- id: f02
  title: 窄幅横盘"极限位置突破才动手"决策规则
  type: decision
  group: M03
  tasks: [task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1756（第10章）；小麦案例 L1772/L1776"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "记录上下限→区间内不动→突破顺向，完整可执行", boundary: "涨跌停制度下'突破'确认方式需 A 股重新界定"}
  V3_task_utility: {passed: true, benefit: "task-03 核心规则；横盘期'绝不沾手'抑制频繁交易"}
  merge_note: "组 M03 主条目；p35/p41/p26 及整数关 f05/p30/p31 同组"

- id: p35
  title: 横盘区间：突破极限位置才动手
  type: rule
  group: M03
  tasks: [task-01, task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1756；行1730-1734（120—130 例）；行1758-1778（小麦 1.10—1.20 例）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "输入→判停→动作完整"}
  V3_task_utility: {passed: true, benefit: "区间市唯一正确动作集；对治'区间内猜方向'"}
  merge_note: "并入 M03/f02"

- id: p41
  title: 关键点位的定义（突破即趋势信号）
  type: rule
  group: M03
  tasks: [task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "第10章脚注② L1744（丁圣元）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "两种含义（新趋势产生/调整结束）分支明确", boundary: "'确定无疑'的量化口径为缺口，如实声明"}
  V3_task_utility: {passed: true, benefit: "关键点/突破触发的统一定义；与 p30/p35 构成关键点清单"}
  merge_note: "并入 M03/f02+f05"

- id: f05
  title: 整数关/关键点突破买入法（100/200/300 关口）
  type: decision
  group: M03
  tasks: [task-05]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2437（第14章）；L1483（第9章）；证伪条款 L1495-1497"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "触发与证伪（回落至关口下即离场）均可执行", boundary: "'续涨 30～50 点'系单案例经验归纳，无统计检验（B 字段）"}
  V3_task_utility: {passed: true, benefit: "task-05 触发与失效规则；矫正低吸偏好"}
  merge_note: "组 M03 成员；与 p30（calculation 面）合并"

- id: p30
  title: 整数关突破买入法（100/200/300，续涨 30—50 点）
  type: calculation
  group: M03
  tasks: [task-05]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1483（第9章）；L2437（第14章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "输入（整数关+首次条件）→动作→预期完整", boundary: "1920s 单案例归纳、无统计验证，须随 B 声明"}
  V3_task_utility: {passed: true, benefit: "明确的触发型买点规则"}
  merge_note: "并入 M03/f05；失效条件由 p31 补足"

- id: p31
  title: 突破失效即离场（阿纳康达 301 规则）
  type: rule
  group: M03
  tasks: [task-05, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1495（第9章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "失效位定义（跌回起涨关键点）与动作（清仓）完整"}
  V3_task_utility: {passed: true, benefit: "突破交易止损设定模板；原书少有的可量化失效位示例"}
  merge_note: "并入 M03/f05（补足失效条件）"

- id: p26
  title: 股价太高可买、太低可卖
  type: rule
  group: M03
  tasks: [task-05, task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1357（第7章）；L1736（第10章重申）；附录二第12条 L3541"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "否定性规则明确（不得以绝对价格高低否决交易）"}
  V3_task_utility: {passed: true, benefit: "直接对治'恐高/捡便宜'两大锚定偏差；ce18 互证"}
  merge_note: "并入 M03（创新高买入法的否决项配套）"

- id: f04
  title: "这是牛市——大势优先与头寸坚守（老帕特里奇模型）"
  type: mental-model
  group: M04
  tasks: [task-01, task-06]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1024（第5章）；L2469（第14章）互证"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "先问'牛市是否接近尾声'再定持有/卖出，流程明确"}
  V3_task_utility: {passed: true, benefit: "task-06 持有纪律；纠正'赚差价丢头寸'"}
  merge_note: "组 M04 主条目；p15/p16/p18/p19/p50 同组"

- id: p15
  title: 判别大势是盈利的全部要诀
  type: principle
  group: M04
  tasks: [task-01]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L938（第5章，数学家反例同段）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "门控条件（大势是否已判）可判定，判读工具由 f01/f33 供给"}
  V3_task_utility: {passed: true, benefit: "确立'方向优先于一切技术细节'的决策顺序"}
  merge_note: "并入 M04（方向门控面）"

- id: p16
  title: "这是牛市：大钱来自主要趋势，头寸不可丢"
  type: principle
  group: M04
  tasks: [task-06]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1028、L1024（第5章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件（浮盈+回撤诱惑）→动作（持有不丢）明确"}
  V3_task_utility: {passed: true, benefit: "全书最核心持有原则；对治'赚小差价丢大趋势'"}
  merge_note: "并入 M04/f04；p17（诊断面，reference）为其引文补充"

- id: p18
  title: 不抓头尾两个 1/8 美元
  type: rule
  group: M04
  tasks: [task-03, task-05, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1040（第5章）；封底 L3654"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "放弃头尾极值的行为约束明确；顶部触发在 p50"}
  V3_task_utility: {passed: true, benefit: "对治'卖飞/抄底摸顶'冲动；封底官方摘要卡条目"}
  merge_note: "并入 M04；p55（rejected，罗斯柴尔德法）引文并入本条参考区"

- id: p19
  title: 牛市中买进并持有，直到确信牛市接近尾声
  type: rule
  group: M04
  tasks: [task-01, task-06]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1040（第5章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "状态→动作映射完整（牛市→买持；总体状况反向→退出）"}
  V3_task_utility: {passed: true, benefit: "牛市基本动作与退出条件一句话成规则"}
  merge_note: "并入 M04/f04"

- id: p50
  title: 绝不求卖最高点：等回落不能涨再卖
  type: rule
  group: M04
  tasks: [task-06, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2487（第14章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "触发（回落失败确认）与动作（卖出）可判定"}
  V3_task_utility: {passed: true, benefit: "顶部确认式退出模板；与 p49 组成'预警→确认→离场'链"}
  merge_note: "并入 M04（p18 的时机面落地）"

- id: f06
  title: 试探—验证—逐步加码建仓程序（步步为营）
  type: procedure
  group: M05
  tasks: [task-04]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1245、L1357（第7章）；棉花案例第10/11章"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "步骤、判停（首笔亏损即停）、输出完整", boundary: "首笔百分比、加码级差、交易成本原书未给，待 A 股参数化"}
  V3_task_utility: {passed: true, benefit: "task-04 建仓程序；试错成本制度化"}
  merge_note: "组 M05 主条目；f07/p22/p23/p24/p25/p36/p37 同组"

- id: f07
  title: 测试交易：以市场反应验证判断与信息
  type: procedure
  group: M05
  tasks: [task-11, task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1343（第7章怀特执事糖业）；L2827（第17章小麦测试）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "输入（判断+测试仓）、步骤、输出（扩大或放弃）完整", boundary: "测试仓相对规模量化标准原书未给（已记）"}
  V3_task_utility: {passed: true, benefit: "把消息验证从言语层挪到成交层"}
  merge_note: "并入 M05/f06"

- id: p22
  title: 步步上涨买进，绝不步步下降摊低
  type: rule
  group: M05
  tasks: [task-04, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1245（第7章，含双向表述）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "可判定（新价 vs 前笔价）、可执行"}
  V3_task_utility: {passed: true, benefit: "直接反制摊平习惯；与 ce04 互证"}
  merge_note: "并入 M05/f06（加码方向面）"

- id: p23
  title: 试探建仓程序与测试单（110→114 案例口径）
  type: calculation
  group: M05
  tasks: [task-04]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1247（第7章，全数字序列逐项核对）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "判断分支（成交形态→加码/测试/怀疑）完整可复用", boundary: "首笔占总资金比例原书未给，未以常识补齐"}
  V3_task_utility: {passed: true, benefit: "建仓程序完整案例口径，作演练题与判停示范"}
  merge_note: "并入 M05/f06（数字口径来源）"

- id: p24
  title: 首笔有利润才做第二笔
  type: rule
  group: M05
  tasks: [task-04, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1357（第7章）；L1782（第10章重述）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "硬性前置条件完全可判定"}
  V3_task_utility: {passed: true, benefit: "加码体系核心闸门；试错成本制度化"}
  merge_note: "并入 M05/f06"

- id: p25
  title: 不一笔满仓，哪怕限额只有 500 股
  type: rule
  group: M05
  tasks: [task-04]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1359、L1361（第7章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "任意规模都分步，与 p36 的 1/5 比例衔接"}
  V3_task_utility: {passed: true, benefit: "分步建仓适用于任意资金规模的底线规则，对治'一把梭'"}
  merge_note: "并入 M05/f06"

- id: p36
  title: 首笔试探为总额度五分之一
  type: calculation
  group: M05
  tasks: [task-04]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1782（第10章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "比例（1/5）与前置条件（账面利润）明确可算", boundary: "'1/5'为额度内比例而非总资金比例，入 B 声明"}
  V3_task_utility: {passed: true, benefit: "原书罕见的仓位比例数字，可落成建仓计划模板"}
  merge_note: "并入 M05/f06"

- id: p37
  title: 棉花梯度加码 1:1:2（10 点/20 点台阶）
  type: calculation
  group: M05
  tasks: [task-04]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1784-1788（第10章）；单位脚注 L2511（第14章，1 点=1 美分）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "梯度、台阶、放弃条件完整，可独立复算", boundary: "1920s 棉花市场语境，入 B；A 股为方法论参照"}
  V3_task_utility: {passed: true, benefit: "期货/杠杆品种的加码梯度模板"}
  merge_note: "并入 M05/f06"

- id: f28
  title: 帕特·赫恩跟随止损体系（1 个点递进加码＋trailing stop）
  type: procedure
  group: M06
  tasks: [task-04, task-06, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1796/L1798（第10章）；反例 L1804-1806（罗伯茨）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "闭环完整、每步可执行", boundary: "'1 个点'系 1/8 美元报价环境，换算步长需按波动率自定义并声明"}
  V3_task_utility: {passed: true, benefit: "原书少有的全参数化趋势跟随模板"}
  merge_note: "组 M06 主条目；p38 为 calculation 面并入"

- id: p38
  title: 帕特·赫恩体系：逐笔 100 股、1 个点止损上限
  type: calculation
  group: M06
  tasks: [task-04, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1796（第10章）；L1806（罗伯茨反例）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "完整机械规则，任一价格序列可独立复算", boundary: "A 股最小报价 0.01 元、无 1/8 美元语境，入 B；震荡市反复止损成本未量化"}
  V3_task_utility: {passed: true, benefit: "可直接落地的 trailing stop 机械化模板"}
  merge_note: "并入 M06/f28"

- id: f30
  title: 错误识别即平仓的零延迟规则
  type: decision
  group: M07
  tasks: [task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2872（第17章）；案例支撑 L1495-1497（第9章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "零延迟动作规则明确；证伪条件由 f02/f05 提供"}
  V3_task_utility: {passed: true, benefit: "止损纪律核心机制（消灭'识别—执行'时差）"}
  merge_note: "组 M07 主条目；p02/p32/p44/p52 同组"

- id: p02
  title: 认清大势并立即行动，站错边立即止损纠正
  type: principle
  group: M07
  tasks: [task-01, task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "译者前言 L165（丁圣元）；L2451（正文）互证"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件（站错边）与动作（立即止损纠正）明确"}
  V3_task_utility: {passed: true, benefit: "把止损定义为纠错动作而非可选成本，对治'套牢装死'"}
  merge_note: "并入 M07（止损的定义面）"

- id: p44
  title: 卖掉亏损头寸、保留盈利头寸，绝不摊低成本
  type: rule
  group: M07
  tasks: [task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2158、L2160（第12章）；附录二第8/9条 L3537-3538"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "双动作（卖亏/留盈）+禁令（不摊平）完全可判定"}
  V3_task_utility: {passed: true, benefit: "止损与持有的操作总则；对治'卖盈保亏'处置效应"}
  merge_note: "并入 M07/f30；与 p22 分工（p22=加码方向，p44=亏损处置）；ce04 为案例面"

- id: p32
  title: 离场要利索：不设限价，按市价出
  type: rule
  group: M07
  tasks: [task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1539、L1541（第9章，299-3/4 起成交明细）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件与动作明确（成交优先于价格）", boundary: "电子化限价单风险远低于 1920s 纸带时代，入 B"}
  V3_task_utility: {passed: true, benefit: "防'挂单等不成交'错离场窗口"}
  merge_note: "并入 M07（执行面）"

- id: p52
  title: 利润入银行才算数
  type: rule
  group: M07
  tasks: [task-07]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2533（第15章）；咖啡案 L2553-2569；150 万兑现 L2499（1917-02 通牒次日，候选归属已更正）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "触发（意外事件创造流动性窗口）与动作（变现）明确", boundary: "与 p16 持有原则的适用边界（限意外窗口，非日常差价）须协调说明"}
  V3_task_utility: {passed: true, benefit: "落袋纪律与'纸面利润≠利润'意识"}
  merge_note: "并入 M07；与 f22（needs_review）重叠，可迁移部分归并时按本条执行"

- id: f08
  title: 希望与恐惧倒置（人性使用说明书）
  type: mental-model
  group: M08
  tasks: [task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1812（第10章），同段完整机理"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "两情境产出与天性相反的明确动作，可固化为自检问句"}
  V3_task_utility: {passed: true, benefit: "task-13 核心自检；附录二多条规则的心理学底座"}
  merge_note: "组 M08 主条目；f29/p39/p43 同组"

- id: p39
  title: 希望与恐惧必须倒过来用
  type: principle
  group: M08
  tasks: [task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1812（第10章）；封底 L3656"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "两种情绪状态→两种反直觉动作，可照做"}
  V3_task_utility: {passed: true, benefit: "对治'套牢装死+蝇利急卖'"}
  merge_note: "并入 M08/f08；ce07 为失败面案例"

- id: f29
  title: "卖到睡不着为止"仓位压力自检
  type: troubleshooting
  group: M08
  tasks: [task-13, task-14]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1708（第10章）；L952（第5章）互证"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "零参数自检回路（减仓→自检→减到心理负荷消失）"}
  V3_task_utility: {passed: true, benefit: "用身心症状反推仓位过重的最简排障"}
  merge_note: "并入 M08"

- id: p43
  title: 不为账单交易（市场不是财神爷）
  type: principle
  group: M08
  tasks: [task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2172（第12章，裘皮大衣案例同章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "动机自检条件（有无具体盈利用途）明确，动作可执行"}
  V3_task_utility: {passed: true, benefit: "交易动机检查项；'让市场为账单付钱是最常见亏损因由'"}
  merge_note: "并入 M08；ce08 为案例面"

- id: f09
  title: 信息来源依赖链推理（拒绝贴士的结构性理由）
  type: reasoning
  group: M09
  tasks: [task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L656（第3章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "'来源可持续性检验'（出场由谁决定）产出可执行"}
  V3_task_utility: {passed: true, benefit: "给'拒绝贴士'结构化判据；A 股小作文/熟人荐股直接适用"}
  merge_note: "组 M09 主条目；p11/p54/p45/p46/p63/f17/f44/f42 同组"

- id: p11
  title: 必须相信自己、不听内幕消息
  type: principle
  group: M09
  tasks: [task-11, task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L656（第3章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件（依据是否来自他人）→动作（不采信）明确"}
  V3_task_utility: {passed: true, benefit: "独立判断是可执行体系的前提"}
  merge_note: "并入 M09/f09；与 p54 互补（p11 正面表述、p54 禁令面）"

- id: p54
  title: 绝不听信托士
  type: principle
  group: M09
  tasks: [task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2667（第16章）；L3471（第24章）；G.O.H. 案例 L2673/L2687"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "禁令明确，替代路径明确（个股/板块异常表现，p56）"}
  V3_task_utility: {passed: true, benefit: "信息拒绝清单总纲；A 股'小作文'第一道防线"}
  merge_note: "并入 M09/f09"

- id: p45
  title: 警惕权威人物的花言巧语（免疫力有限）
  type: principle
  group: M09
  tasks: [task-11, task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2166、L2144（第12章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "感染判据（能否凭自身观察安心交易）可自测"}
  V3_task_utility: {passed: true, benefit: "防御大 V/权威解释的同化效应"}
  merge_note: "并入 M09；ce03/c27 为案例面"

- id: p46
  title: 感恩与人情不得压倒独立判断
  type: principle
  group: M09
  tasks: [task-11, task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2367（第13章，威廉森事件同章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "动机判据（判断驱动还是人情驱动）明确"}
  V3_task_utility: {passed: true, benefit: "熟人社交情境（荐股、人情仓）的防御规则"}
  merge_note: "并入 M09；ce10/c29 为案例面"

- id: p63
  title: 匿名权威利好不可信
  type: rule
  group: M09
  tasks: [task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L3387（第23章规则句）；L3381/L3385；L3397/L3401（时点规律）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "署名检验+时点检验双重可操作"}
  V3_task_utility: {passed: true, benefit: "信息可信度分级规则；迁移为 A 股署名与时点鉴别"}
  merge_note: "并入 M09/f17（f17 为排障程序面）"

- id: f17
  title: 匿名权威利好鉴别（署名检验标准）
  type: troubleshooting
  group: M09
  tasks: [task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L3387（第23章）；L3457/L3463（第24章法律不对称）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "四步判定（具名？时点？内部人行为？结论？）完整", boundary: "A 股荐股监管使匿名权威形态不同，需换算（已记）"}
  V3_task_utility: {passed: true, benefit: "task-11 信息可信度分级核心判据"}
  merge_note: "并入 M09（p63 的程序化面）"

- id: f44
  title: 新闻按趋势过滤解读（消息的心理放大器模型）
  type: framework
  group: M09
  tasks: [task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1738（第10章）；L2487（第14章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "消息解读次序与两类观察结论（利空被忽略=健康；利好被麻木=警惕）"}
  V3_task_utility: {passed: true, benefit: "纠正'由消息推趋势'的因果倒置"}
  merge_note: "并入 M09"

- id: f42
  title: 恩惠—缴械防御：人情不得压倒独立判断
  type: mental-model
  group: M09
  tasks: [task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2367（第13章）；L2134（第12章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "三道防线（感激限定/预设不免疫/区分金钱债与人情债）均可检查"}
  V3_task_utility: {passed: true, benefit: "A 股熟人荐股/投顾人情场景的直接防御"}
  merge_note: "并入 M09（p46 的防线程序面）"

- id: f14
  title: 板块一致性与领头羊监测（异常即内幕）
  type: framework
  group: M10
  tasks: [task-08, task-09]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2469（第14章）；L2835-2852、L2862（第17章）；L2473-2475"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "掉队=预警，三项动作产出", boundary: "'滞涨/掉队'量化（时间与幅度阈值）原书未给"}
  V3_task_utility: {passed: true, benefit: "task-08/09；板块一致性检查可直接落成对照表"}
  merge_note: "组 M10 主条目；f15/p49/p56/p57 同组"

- id: f15
  title: 内部人行为解读框架
  type: framework
  group: M10
  tasks: [task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2864（第17章）；L2581（第15章）；L3200/L3255（第22章）；L2589-2665（第16章反例）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "查内部人实际行为→按派发宣传处理", boundary: "A 股内部人数据按定期报告披露、时效滞后（换算缺口已记）"}
  V3_task_utility: {passed: true, benefit: "task-12 言行分离检验的可操作取数清单"}
  merge_note: "并入 M10"

- id: p49
  title: 领头羊滞涨是牛市终结的警告信号
  type: rule
  group: M10
  tasks: [task-08]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2463（第14章）；L2465-2483（回落 6～7 点、5000 股×12 只、双倍加仓）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "信号与动作明确（卖出/看空滞涨领头羊）", boundary: "'每只 4 点利润'原文未见（候选摘要已更正）"}
  V3_task_utility: {passed: true, benefit: "顶部预警清单首条；1916 逃顶实操为 A 股板块退潮监测模板"}
  merge_note: "并入 M10/f14"

- id: p56
  title: 只寻求一种迹象——内部人买进的情况
  type: rule
  group: M10
  tasks: [task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2864、L2862（第17章）；婆罗洲锡业（第16章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "信号→含义→动作链明确", boundary: "内部人行为数据 A 股可得性缺口如实声明"}
  V3_task_utility: {passed: true, benefit: "个股异常=最好的'内幕消息'（task-12）"}
  merge_note: "并入 M10/f15"

- id: p57
  title: 板块一致性：与群体对着干不明智
  type: rule
  group: M10
  tasks: [task-09]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2833、L2850（第17章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "对照条件（板块其余成员表现）与动作明确"}
  V3_task_utility: {passed: true, benefit: "板块强弱对照表的操作规则；A 股板块效应显著适用性高"}
  merge_note: "并入 M10/f14"

- id: f16
  title: "空头打压"归因排障（下跌解释的可信度检验）
  type: troubleshooting
  group: M11
  tasks: [task-10]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2581（第15章，99/100 及检验逻辑）；L3415-3417（第23章纽黑文）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "五步排障路径完整、每步有判据", boundary: "'内部人行为'A 股可观测渠道不同（换算缺口已记）"}
  V3_task_utility: {passed: true, benefit: "task-10 下跌归因决策树；防被'权威解释'麻痹在高位不卖"}
  merge_note: "组 M11 主条目；p51/p62 同组"

- id: p51
  title: "人为打压"100 例中 99 例是合理下跌
  type: principle
  group: M11
  tasks: [task-10]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2581（第15章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "归因先验+机制检验可操作"}
  V3_task_utility: {passed: true, benefit: "下跌归因决策树核心先验"}
  merge_note: "并入 M11/f16"

- id: p62
  title: 持续下跌从来不是空头打压
  type: principle
  group: M11
  tasks: [task-10]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L3413（第23章）；纽黑文 255→12 L3415/L3421"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "与 p51 互补（p51=急跌先验，p62=持续下跌归因）"}
  V3_task_utility: {passed: true, benefit: "下跌归因决策树第二支柱"}
  merge_note: "并入 M11/f16"

- id: f45
  title: 行为证据优先于言语（用眼睛核实一切断言）
  type: reasoning
  group: M12
  tasks: [task-11, task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2775（第16章信纸/信封）；L1427（第8章铁路抢跑）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "取证清单逻辑可执行", boundary: "A 股披露环境使部分私人观察不可得，换算为公开行动数据"}
  V3_task_utility: {passed: true, benefit: "task-11/12 取证原则；与 f15 合成'言行分离'检验"}
  merge_note: "独立组（与 f15 组合使用）"

- id: f18
  title: 错误复盘转化程序（把亏损变成学费收据）
  type: procedure
  group: M13
  tasks: [task-13, task-14]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L928（第4章）；L1046（第5章戒律清单）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "定位→归因→转戒律→不重犯验收完整", boundary: "无结构化模板、归因易受自辩偏差污染（入 B）"}
  V3_task_utility: {passed: true, benefit: "给复盘固定交付物（戒律条目）"}
  merge_note: "独立组；p13（maxim，reference）为引文补充"

- id: f19
  title: 交易状态管理：债务/健康/情绪不佳即停手
  type: procedure
  group: M14
  tasks: [task-14]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2401、L2397（第13章）；L952（第5章）；L2429（第14章）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "识别→停手→消除根源→恢复条件完整", boundary: "量化触发阈值原书未给，需下游自定义并声明"}
  V3_task_utility: {passed: true, benefit: "task-14 停手条件与恢复程序"}
  merge_note: "组 M14 主条目；f21/p47/p48 同组"

- id: f21
  title: 本金隔离：信托与年金的生存工程
  type: procedure
  group: M14
  tasks: [task-14]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2519、L2523（第14章）；附录一 L3508"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "清偿→划隔离→不可撤销设计→只留风险资本，完整可执行", boundary: "隔离比例无数值；现代工具映射需声明来源"}
  V3_task_utility: {passed: true, benefit: "物理隔离降低'翻本式重仓'概率"}
  merge_note: "并入 M14/f19"

- id: p47
  title: 债务焦虑毁判断力；本金与生活隔离
  type: principle
  group: M14
  tasks: [task-14]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2401（第13章）；L2519（第14章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "状态条件与动作（停手+隔离）明确"}
  V3_task_utility: {passed: true, benefit: "对'短钱长投、借钱炒股'的直接禁令"}
  merge_note: "并入 M14/f19+f21"

- id: p48
  title: 没有足够本金就不可能有良好判断力
  type: principle
  group: M14
  tasks: [task-03, task-14]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2429（第14章）；伯利恒 98→100 L2443"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件（本金→试错预算）与动作（降低频率、只等关键点）明确"}
  V3_task_utility: {passed: true, benefit: "小资金账户的节奏规则；对治'本金越小越频繁'反向螺旋"}
  merge_note: "并入 M14（与 f20 needs_review 互补：本条提供其缺失的'等待'面）"

- id: f23
  title: 可交易性判定：没有行情就不做
  type: decision
  group: M15
  tasks: [task-15]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L408（第2章）；L2385、L2429（第13-14章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "判据（波动幅度与趋势清晰度）→空仓/防守，明确", boundary: "'行情存在'量化阈值需下游自定义"}
  V3_task_utility: {passed: true, benefit: "A 股震荡市的频繁交易止损器"}
  merge_note: "组 M15 主条目；p08 同组"

- id: p08
  title: 不要天天交易，只在市场前兆有利时入市
  type: rule
  group: M15
  tasks: [task-15, task-18]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L410（第2章）；附录二第2条 L3532"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件（有无充分理由）→动作（不交易/入市）明确"}
  V3_task_utility: {passed: true, benefit: "频率纪律直接对应 task-15 与 task-18 清单第 2 条"}
  merge_note: "并入 M15/f23（附录二第 2 条成文版）"

- id: f24
  title: 牛熊转换的分阶段过渡程序（既买又卖→净空→加倍）
  type: procedure
  group: M16
  tasks: [task-08]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L2473-L2479（第14章，全链条同章）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "三阶段序列完整；A 股无做空常态时映射为单边减仓序列", boundary: "各阶段比例无量值、A 股映射需声明换算"}
  V3_task_utility: {passed: true, benefit: "顶部仓位过渡节奏；避免'一次性清仓/一次性死扛'两极"}
  merge_note: "独立组（task-08 的程序面）"

- id: f25
  title: 大额头寸的"市场胃口"测试与顺势退出
  type: procedure
  group: M17
  tasks: [task-16]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1357（第7章）；L2827（第17章）"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "测试单→分批→能卖时卖，步骤与输出完整", boundary: "大户视角降维为个人流动性检查（相对成交量规模约束）"}
  V3_task_utility: {passed: true, benefit: "task-16 降维参考；小盘股/大额持仓进出可行性自检"}
  merge_note: "组 M17 主条目；p09 同组；p27（reference）为其原则面"

- id: p09
  title: 必须把执行偏差计入交易（限价预留/滑点）
  type: rule
  group: M17
  tasks: [task-16]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L724（第2章）；1901-05-09 案例 L708-712（'20 点以上/30 或 40 点'口径已更正）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "下单前检查项（指令类型/预期成交价/流动性约束）明确"}
  V3_task_utility: {passed: true, benefit: "把'成交机制'列为独立亏损源；对应 A 股涨跌停挂单与冲击成本"}
  merge_note: "并入 M17/f25；规则较薄，阶段 1.6 建议并入执行/流动性单元"

- id: f32
  title: 不与纸带争辩、心态归零
  type: mental-model
  group: M18
  tasks: [task-01, task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1756（第10章）；L3553（附录三）；L1367（第8章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "归零重判动作可检查（复盘验证'是否曾为观点辩护'）"}
  V3_task_utility: {passed: true, benefit: "改善判读独立性；与 f39 构成'去自尊化'两翼"}
  merge_note: "组 M18 主条目；p12（maxim，reference）为标志句并入"

- id: f39
  title: 只站正确的一边：不与多空任一方结盟
  type: mental-model
  group: M18
  tasks: [task-01, task-13]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L644（第3章）；封底 L3653"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "去身份化重述规则与换边动作产出明确"}
  V3_task_utility: {passed: true, benefit: "消除多空立场对判断的绑架"}
  merge_note: "并入 M18；p10（reference）为其原则面"

- id: f40
  title: 基本形势同盟军（顺大势者得两股力量之助）
  type: mental-model
  group: M19
  tasks: [task-01]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L1463（第8章）；L1740（第10章）；L2910（第18章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "方向一致性+预期规模双判定", boundary: "'基本形势'构成（银根/盈亏/商业周期）无量化监测法"}
  V3_task_utility: {passed: true, benefit: "task-01 宏观层整合；给持有耐心以基本面依据"}
  merge_note: "组 M19 主条目；f36/p42 同组"

- id: f36
  title: 个体与整体层面区分：基本分析管企业、统计规律管市场
  type: reasoning
  group: M19
  tasks: [task-01]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L205/L207（译者前言）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "两层决策结构（基本分析入池、行情层裁决买卖）"}
  V3_task_utility: {passed: true, benefit: "防'基本面好就逆势买'的层次混用"}
  merge_note: "并入 M19/f40"

- id: p42
  title: 基本分析与纸带结合，但以纸带信号为准
  type: rule
  group: M19
  tasks: [task-01]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "第10章脚注① L1752（丁圣元）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "冲突裁决规则明确（纸带优先）"}
  V3_task_utility: {passed: true, benefit: "'基本面好却不涨'场景的裁决规则"}
  merge_note: "并入 M19/f40"

- id: f13
  title: 股票习性：行为不对路就不碰
  type: mental-model
  group: M20
  tasks: [task-08, task-09, task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L932、L934（第5章）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "行为偏离习性→不碰/退出", boundary: "前提是持有该股历史行为记录，无记录时退化为'不熟不碰'"}
  V3_task_utility: {passed: true, benefit: "个股层过滤器（与 f01 市场层构成双层过滤）"}
  merge_note: "组 M20 主条目；p20 同组"

- id: p20
  title: 股票习性：行为不对路就不碰
  type: rule
  group: M20
  tasks: [task-08, task-09, task-12]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L932（第5章）；旁证 L2797（第17章，候选'第 20 章'标注已更正）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件与动作明确，纸面可操作"}
  V3_task_utility: {passed: true, benefit: "异常信号族通则（与 p56/p57 组合）"}
  merge_note: "并入 M20/f13"

- id: f11
  title: 小本预测—事后核对验证法（预测日志）
  type: procedure
  group: M21
  tasks: [task-02, task-03]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L303（第1章），同段明确与纸上模拟的区别"}
  V2_executability: {passed: true, check_mode: completeness_check_with_new_input, note: "步骤完整、产出可核对", boundary: "样本量与'部分正确'处理原书未述（不阻塞执行）"}
  V3_task_utility: {passed: true, benefit: "判断质量校准器；防事后诸葛"}
  merge_note: "独立组（f13/f31 的能力地基）"

- id: p65
  title: 利弗莫尔 15 条股票交易规则（成文总表）
  type: checklist
  group: M22
  tasks: [task-18]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "附录二 L3529-3545（丁圣元整理）；与正文对应关系抽查属实"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "15 条逐项可勾选，产生违规项清单", boundary: "规则间无优先级与冲突消解说明（原书如此，如实声明）；第 5 条与 p52 适用边界按 p16/p52 协调"}
  V3_task_utility: {passed: true, benefit: "原书唯一成文规则总表=现成日常执行清单，零改造成本"}
  merge_note: "组 M22 主条目；p68（封底 6 条）为其摘要卡；task-18 的直接承载"

- id: p68
  title: 杰西·利弗莫尔的交易原则（封底六条）
  type: checklist
  group: M22
  tasks: [task-18]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "封底 L3649-3659；条目与 p10/p18/p33/p39/p40 一一对应核实"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "六条逐项过；第 5 条（两股力量）为独特条目（L1740 有原文）"}
  V3_task_utility: {passed: true, benefit: "全书原则官方摘要卡，作 overview 参考区总览或心理自检卡"}
  merge_note: "并入 M22/p65；编译时按引用合并，不重复建能力"

- id: p07
  title: 纸带不解释原因，当下必须行动
  type: rule
  group: M23
  tasks: [task-10, task-11]
  decision: verified
  V1_source_sufficiency: {passed: true, location: "L310（第1章，霍洛管道例证同段）"}
  V2_executability: {passed: true, check_mode: walkthrough, note: "条件（价格异动）与动作（立刻行动、原因以后追查）明确"}
  V3_task_utility: {passed: true, benefit: "对治'等消息、找原因'拖延处置；确立以盘面为准的决策顺序"}
  merge_note: "独立组（与 g08/f03 同源；A 股'小作文'环境下盘面优先的总规则）"
```

## 统计与移交

- **总数 81**（framework 32 + principle 49），与 verify-framework.md / verify-principle.md 的判定分布一致；rejected 3 条（p55→p18、p60→p06、c52→c33）不在本文件，见 rejected/ 目录与 references.md 备注。
- 合并组 M01–M23 供阶段 1.6 编排能力单元；组内 p 类候选作证据层并入 f 类主条目，不重复建能力。
- 全部候选自记的边界（量化参数缺口、A 股制度换算、单案例经验律）必须随对应能力单元的 B 字段交付，明细见 needs-review.md 缺口清单。
