# 原则/规则/清单候选（阶段 1 · principle-extractor）

- 书目: 股票大作手回忆录（丁圣元注疏版），人民邮电出版社 2022.1
- 来源标注约定: 【作者】= 正文利文斯顿（利弗莫尔）自述原则；【丁注】= 丁圣元注疏原则（译者前言 / 页下注 / 附录）；【封底】= 出版社编辑提炼
- 基准: BOOK_OVERVIEW.md（阶段 0）；扫描范围: 译者前言 + 第 1—24 章 + 附录一/二/三 + 封底，全文无跳读
- 候选总数: 68（principle 24 / rule 26 / calculation 6 / maxim 10 / checklist 2）
- 说明: 附录二 15 条与封底 6 条为成文总表，以 checklist 整体收录并标注与正文对应关系，不重复拆条

```yaml
- id: p01
  title: 趋势是核心概念，行为要领是服从纪律
  type: maxim
  source_chapter: 译者前言（丁圣元注疏）
  source_quote: |
    "在技术分析领域，趋势是核心概念，而行为要领就是服从纪律……把趋势永远放在技术分析的核心地位。"
  summary: |
    【丁注】技术分析只有两条根：判断对象是趋势，执行要领是纪律。任何具体规则都必须挂靠在这两条之上。
  tags: [maxim, trend, discipline, ding-shengyuan]

- id: p02
  title: 认清大势并立即行动，站错边立即止损纠正
  type: principle
  source_chapter: 译者前言（丁圣元注疏）
  source_quote: |
    "其核心能力就在于能认清市场趋势，立即采取必要行动，力求始终站在市场正确的一边；如果未能站在正确的一边，则必须立即止损纠正。"
  summary: |
    【丁注】成功交易者的基本特征被归结为一个循环：识别趋势—立即行动—错了立即纠正。止损被定义为"站错边"的纠错动作，而非可选成本。
  tags: [principle, trend, stop-loss, ding-shengyuan]

- id: p03
  title: 收益与风险一体两面，承担力所能及的风险
  type: principle
  source_chapter: 译者前言（丁圣元注疏）
  source_quote: |
    "不是盈利越多越'正确'，而是收益与风险一体两面，必须被同时纳入考虑范围：承担力所能及的风险，获得相称的、可持续的回报。"
  summary: |
    【丁注】以盈亏作为交易正确性的唯一检验标准时，必须同时度量风险侧；只看盈利规模是对"正确"的误读。为原书补足的资金管理总纲。
  tags: [principle, risk-management, ding-shengyuan]

- id: p04
  title: 敬业守纪是立足点；没有平衡的人生就没有持久成功的交易
  type: principle
  source_chapter: 译者前言（丁圣元注疏）
  source_quote: |
    "即便是交易天才，也不能违背市场交易的基本原则。敬业、守纪是市场参与者的根本立足点。""没有平衡的人生，就没有持久成功的交易事业。"
  summary: |
    【丁注】以利弗莫尔 1934 年第四次破产、1940 年自杀为鉴：规则层知识不保证执行，生活失衡会摧毁交易事业。对本书"只谈交易不谈人生"的补课。
  tags: [principle, discipline, life-balance, ding-shengyuan]

- id: p05
  title: 借鉴他人交易行为，不崇拜不鄙夷其财富
  type: principle
  source_chapter: 译者前言（丁圣元注疏）
  source_quote: |
    "他们的财富再多，也不会分给你一分钱……他的交易行为往往体现出典型人性的某一方面……规避自身的人性弱点，追求正确的交易行为，是所有交易者的必备修养。"
  summary: |
    【丁注】市场是交易者"绝不走形的好镜子"：他人盈亏是行为正确与否的证据，学习对象是行为而非财富本身。
  tags: [principle, learning, behavior, ding-shengyuan]

- id: p06
  title: 华尔街没有新鲜事
  type: maxim
  source_chapter: 第 1 章 行情纸带悟模式（作者）
  source_quote: |
    "华尔街没有新鲜事。投机乃人类天性，就像山包一般古老，华尔街不可能有什么新鲜的。"
  summary: |
    【作者】历史重演、人性不变是全书全部形态识别方法成立的前提假设；也是本书方法可跨时代迁移的论证基础。
  tags: [maxim, market-history, human-nature]

- id: p07
  title: 纸带不解释原因，当下必须行动
  type: rule
  source_chapter: 第 1 章 行情纸带悟模式（作者）
  source_quote: |
    "纸带从不关心原因。纸带也不做任何解释……原因可以放一放，以后再追查。但是，你必须立刻行动，不然就会被市场抛弃。"
  summary: |
    【作者】交易依据是价格行为本身，不是事后才披露的原因；原因追查与即时交易在时间上分离。霍洛管道下跌 3 个点即为例证。
  tags: [rule, price-action, timing]

- id: p08
  title: 不要天天交易，只在市场前兆有利时入市
  type: rule
  source_chapter: 第 2 章 首战纽约遭挫败（作者）
  source_quote: |
    "不顾实际市场状况，只顾不停地买卖，是导致华尔街许多交易者亏损的罪魁祸首……没人能够天天找到充分理由，天天买进或者卖出股票。"
  summary: |
    【作者】"天下万物皆有定时"：交易频率本身是亏损源；仅当看到市场前兆确实有利时才入市。附录二第 2 条即此规则的成文版。
  tags: [rule, trading-frequency, timing]

- id: p09
  title: 必须把执行偏差计入交易（限价预留/滑点）
  type: rule
  source_chapter: 第 2 章 首战纽约遭挫败（作者）
  source_quote: |
    "仅仅阅读纸带、不考虑经纪行执行指令的情况是不行的。"
  summary: |
    【作者】1901 年 5 月 9 日破产主因：市价单在纸带滞后与巨量成交下成交价偏离预期 15—40 点。纸带信号之外，成交机制是独立的亏损源（现代对应：滑点与流动性）。
  tags: [rule, execution, slippage]

- id: p10
  title: 市场只有一个方面：正确的方面
  type: principle
  source_chapter: 第 3 章 行情纸带拖后腿（作者）
  source_quote: |
    "股票市场只有一个方面，既不是多头的方面，也不是空头的方面，而是只有正确的方面。我花了很长时间才把这项基本原则牢牢地扎根在脑子里。"
  summary: |
    【作者】立场必须让位于市场验证；多头/空头身份认同是错误来源。封底六原则之一；与第 14 章"不与市场哪一边山盟海誓"同源。
  tags: [principle, mindset, objectivity]

- id: p11
  title: 必须相信自己、不听内幕消息
  type: principle
  source_chapter: 第 3 章 行情纸带拖后腿（作者）
  source_quote: |
    "如果打算在这一行谋生的话，你必须相信自己，相信自己的判断。这就是我从不听信内幕消息的缘故。"
  summary: |
    【作者】买卖依据若来自他人，卖出时点也被他人绑定；独立判断是可执行体系的前提。与第 6 章萨拉托加损失 4 万美元教训互证。
  tags: [principle, independence, tips]

- id: p12
  title: 从不与行情纸带争辩
  type: maxim
  source_chapter: 第 3 章 / 第 10 章（作者）
  source_quote: |
    "我从来不对股票市场发脾气。我从不与行情纸带争辩。抱怨市场无济于事。""决不和纸带争辩，决不要求纸带说明缘由或给你解释原因。"
  summary: |
    【作者】在第 3、8、10、20 章反复出现的情绪纪律：市场错误不能归咎、不能赌气对抗；"得肺炎时对肺生气一样荒唐"。
  tags: [maxim, emotional-discipline]

- id: p13
  title: 亏损是学费：不重复同一个错误
  type: maxim
  source_chapter: 第 3 章 行情纸带拖后腿（作者）
  source_quote: |
    "对我来说，亏损从来都不仅仅意味着损失，更重要的是其中的教训……我不希望第二次重复同一个错误。"
  summary: |
    【作者】把每次亏损转化为清单上新添的戒律（"在我的清单里，就会添加一条新的戒律"）；错误分析是交易学习的正途。
  tags: [maxim, learning-from-loss]

- id: p14
  title: 先学会绝不可做什么，才开始学习应该做什么
  type: maxim
  source_chapter: 第 4 章 回老家"疗伤"反省（作者）
  source_quote: |
    "当你学会绝不可做什么才不会赔钱的时候，才是你开始学习应该做什么才能赢利的时候。明白吗？就这样，你才开始学习！"
  summary: |
    【作者】否定性知识（避损清单）先于肯定性知识（盈利方法）；止损、不摊平等"不做"规则优先级最高。
  tags: [maxim, negative-knowledge]

- id: p15
  title: 判别大势是盈利的全部要诀
  type: principle
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "如果市场大势看涨，那么即便是一场世界大战，也不能阻止牛市行情；或者如果大势看跌，同样也没什么能阻止熊市行情。想盈利，判别大势才是你需要了解的一切。"
  summary: |
    【作者】以数学家图表体系的百年巨亏为反例：方法精巧不抵大势误判；大势研判优先于一切技术细节。
  tags: [principle, major-trend]

- id: p16
  title: "这是牛市"：大钱来自主要趋势，头寸不可丢
  type: principle
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "大钱不是从哪一次或哪几次行情起伏中产生的，而是从主要趋势中产生的""没人承担得起失去头寸的后果，就算约翰·D.洛克菲勒也不行。"
  summary: |
    【作者】老帕特里奇教条：牛市中不为抢小差价卖出（丢头寸=丢饭碗）；利润载体是头寸而非差价。全书最核心的持有原则。
  tags: [principle, position-holding, major-trend]

- id: p17
  title: 挣大钱靠耐心坚守，不靠进进出出
  type: principle
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "我之所以挣大钱，从来不是凭着进进出出，而始终是凭借耐心坚守。明白吗？凭我的耐心坚守。"
  summary: |
    【作者】"既能正确判断又能耐心坚守的人凤毛麟角……不是市场打败了他们，是他们自己打败了自己。"方向正确而拿不住是普遍亏损模式。
  tags: [principle, patience, holding]

- id: p18
  title: 不抓头尾两个 1/8 美元
  type: rule
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "不再企图抓住行情最后的1/8美元——或者行情最初的1/8美元。这两个1/8美元，是世上最昂贵的1/8美元。"
  summary: |
    【作者】放弃最高点与最低点的极值交易；为逃顶抄底付出的代价"足以修建一条横跨美洲大陆的高速公路"。封底六原则之一。
  tags: [rule, entry-exit, extremes]

- id: p19
  title: 牛市中买进并持有，直到确信牛市接近尾声
  type: rule
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "在牛市行情中，只能买进并持有，直到你确信牛市已经接近尾声。要做到这一点，就必须研究总体市场状况。"
  summary: |
    【作者】牛市基本动作只有"买入—持有—观察总体状况"，且"忘掉你所有的股票，忘掉，才能保住盈利"；退出信号是总体市场状况反向。
  tags: [rule, bull-market, holding]

- id: p20
  title: 股票习性：行为不对路就不碰
  type: rule
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "如果某个股票行为不对路，就不要碰它。因为，既然不能准确了解何处不对，就不能分辨它到底要走哪条路。不能查清事实，便不能判断。没有判断，就没有利润。"
  summary: |
    【作者】个股有历史行为模式（习性），现价表现与前兆不符即为危险信号；与第 20 章"股票没按应有方式变化就放弃"同一规则。
  tags: [rule, stock-behavior, avoidance]

- id: p21
  title: 绝不能当肥羊
  type: maxim
  source_chapter: 第 5 章 梅开三度华尔街（作者）
  source_quote: |
    "从老经验们金口玉牙里掉出来的所有禁忌戒条，他们都记得滚瓜烂熟——除了最主要的一条：绝不能当肥羊。"
  summary: |
    【作者】半瓶子醋记住了所有格言却仍是肥羊；避免亏损的元规则是认识到自己在生态中的猎物位置，而非背诵戒条。
  tags: [maxim, sucker-trap, self-awareness]

- id: p22
  title: 步步上涨买进，绝不步步下降摊低
  type: rule
  source_chapter: 第 7 章 顺势操作先试探（作者）
  source_quote: |
    "当我看空、做空某只股票时，每次卖出的价格都必须比前一次卖出的价格更低。当我买进的时候，情况正相反。我必须按照步步上涨的方式买进，而不是按照步步下降的方式买入。"
  summary: |
    【作者】加码方向与常识相反：只在头寸已有账面利润时顺势加码，绝不逢低摊平。"这就是为什么我从来不愿意低价买进股票。"
  tags: [rule, pyramiding, no-averaging-down]

- id: p23
  title: 试探建仓程序与测试单（110→114 案例口径）
  type: calculation
  source_chapter: 第 7 章 顺势操作先试探（作者）
  source_quote: |
    "在 110 买进了 2000 股。如果买进之后，股价上涨到 111，那么至少表明，我的操作暂时是正确的……我又买进了 2000 股。如果市场仍然处在上涨状态，我会再买进第三笔 2000 股。"
  summary: |
    【作者】建仓程序完整口径：首笔 2000 股→每涨 1 点加 2000 股共 3 笔→回落至 112-1/4 后涨回 113-3/4 时买 4000 股；若 4000 股成交呆滞（集中 113-3/4）即发出测试指令卖出 1000 股观察市场反应，成交逐级走高（114→114-1/2→115-1/2）则验证正确。inputs: 前笔成交价与股数；output: 加码/测试/放弃决策；missing: 首笔占总资金比例未给出。
  tags: [calculation, pyramiding, test-order, probing]

- id: p24
  title: 首笔有利润才做第二笔
  type: rule
  source_chapter: 第 7 章 顺势操作先试探（作者）
  source_quote: |
    "在第一笔交易之后，除非第一笔交易有利润，否则不可以做第二笔。"
  summary: |
    【作者】加码的硬性前置条件；第 10 章重述为"如果这笔头寸未形成账面利润，他绝不可以增加持仓"。首笔亏损=至少暂时做错的判定信号。
  tags: [rule, pyramiding, first-profit-condition]

- id: p25
  title: 不一笔满仓，哪怕限额只有 500 股
  type: rule
  source_chapter: 第 7 章 顺势操作先试探（作者）
  source_quote: |
    "即使最大投资限额只有 500 股股票，也不应该一笔满仓买进，如果把投机看作严肃的生意的话。如果只想赌一赌运气，那我只有一个建议：别玩这个！"
  summary: |
    【作者】分步建仓适用于任意资金规模；一次性满仓与赌博同义。首笔亏损时"为什么还要雪上加霜，再买进更多股票呢"。
  tags: [rule, position-sizing, no-all-in]

- id: p26
  title: 股价太高可买、太低可卖
  type: rule
  source_chapter: 第 7 章 / 第 10 章（作者）
  source_quote: |
    "股票永远不会因为价格太高而不可买进，或者因为价格太低而不可卖出。"
  summary: |
    【作者】价格绝对高低不是买卖依据，最小阻力路线才是；"绝不要因为股票价格太高而不能买进，绝不要因为价格太低而不能卖出"（第 10 章重申）。附录二第 12 条成文版。
  tags: [rule, price-level, contrarian-anchor]

- id: p27
  title: 在能够卖出的时候卖出，而非想卖出的时候
  type: rule
  source_chapter: 第 7 章 / 第 11 章（作者）
  source_quote: |
    "他不得不在能够卖出的时候卖出，而不是在他想要卖出的时候卖出。为了拿捏分寸，他既必须观察，也必须试探。"
  summary: |
    【作者】大额头寸的流动性约束：必须等"市场有胃口"吸纳全部头寸；第 11 章 14 万包棉花靠《世界报》报道才得以离场。对个人投资者为降维参考。
  tags: [rule, liquidity, exit, large-position]

- id: p28
  title: 时机是独立变量：头寸对、做法错照样破产
  type: principle
  source_chapter: 第 8 章 今是昨非识大局（作者）
  source_quote: |
    "头寸是对的，但做法是错的。""在熊市行情刚刚开始的时候，即使看空是完全正确的，最好也不要立即大笔卖出，一定要等到不存在发动机回火的风险后再行动。"
  summary: |
    【作者】1906 年看对熊市却因过早卖空两次被扫地出门；方向判断与入市时机是两把独立的锁，"操之过急"本身即致命错误。
  tags: [principle, timing, premature-entry]

- id: p29
  title: 等待市场自我界定的信号再动手（增发广告信号）
  type: rule
  source_chapter: 第 8 章 / 第 14 章（作者）
  source_quote: |
    "问题正在于没有明智地等待这样的信号。"北太平洋与大北方宣布增发股票、"分期付款"条款即做空信号——"该等的都等到了。"
  summary: |
    【作者】关键心理时刻由市场事件确认（银根紧张时投资银行让步分期付款=资金枯竭信号）；1915 年同样"守候市场敲响全速前进铃声的关键心理时刻"才买伯利恒钢铁。
  tags: [rule, signal, key-moment]

- id: p30
  title: 整数关突破买入法（100/200/300，续涨 30—50 点）
  type: calculation
  source_chapter: 第 9 章 / 第 14 章（作者）
  source_quote: |
    "当只股票的价格第一次超越100、200或300美元整数大关之后，它不会停留在这些整数附近，而要继续上升较大的幅度。""几乎总是会保持上升势头，继续上涨30～50点——而且在突破300后，上涨比在100或200之后来得更快。"
  summary: |
    【作者】久经考验的触发规则：首次突破整数大关立即买进。inputs: 整数关价位（100/200/300）与"第一次"条件；output: 30—50 点预期涨幅；missing: 失效位仅个别案例（见 p31），无统计样本（阶段 0 已标注待核查）。实例：阿纳康达破 300、伯利恒钢铁破 100。
  tags: [calculation, breakout, round-number]

- id: p31
  title: 突破失效即离场（阿纳康达 301 规则）
  type: rule
  source_chapter: 第 9 章 紧缩银根酿恐慌（作者）
  source_quote: |
    "我打定主意，如果阿纳康达跌回301，就必须断定它的整个这轮行情都是假象。如果它的上涨行情合理，价格应该已经一鼓作气达到310了。"
  summary: |
    【作者】突破买入须预设失效判定：跌破起涨关键点（301）即承认"观察到的范例辜负了我"，全部卖出。当一个人犯错时唯一该做的就是停止继续犯错。
  tags: [rule, invalidation, stop-loss]

- id: p32
  title: 离场要利索：不设限价，按市价出
  type: rule
  source_chapter: 第 9 章 紧缩银根酿恐慌（作者）
  source_quote: |
    "我从来不以限价方式交易是对的……当你想离场的时候，一定要利利索索离场。"
  summary: |
    【作者】卖出离场用市价指令保证成交优先于价格（阿纳康达 299-3/4 逐级成交）；与之配套，买进"宁愿支付更高的价格"（第 10 章）。
  tags: [rule, market-order, exit]

- id: p33
  title: 价格沿最小阻力路线运动
  type: principle
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "价格沿着阻力最小的路线运动。因此，如果它在上升时受到的阻力比在下降时受到的阻力更小，它就会上升；反之亦然。"
  summary: |
    【作者】全书核心理论：趋势即最小阻力路线；突破关键点位的那一刻即路线显现。附录三给出机制解释（倒水试验、买卖压力表）。
  tags: [principle, line-of-least-resistance, trend]

- id: p34
  title: 读纸带只做两项评估：怎样交易、何时交易
  type: principle
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "阅读纸带的目的是进行两项评估，第一，怎样交易；第二，何时交易。也就是说，确定到底是买进还是卖出更明智。"
  summary: |
    【作者】价格行为分析的功能边界：不预测具体价位与时间，只回答方向与时机两个问题；"纸带绝不会告诉你下一个星期四下午 1:35 你有多少身家"。
  tags: [principle, tape-reading, scope]

- id: p35
  title: 横盘区间：突破极限位置才动手
  type: rule
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "在窄幅波动的市场行情中……企图预期市场下一步大动作到底是向上还是向下，是没有任何道理的……拿定主意，除非市场在哪一个方向上突破了上述极限位置，否则绝不沾手。"
  summary: |
    【作者】区间市操作规则：记录上下极限（如 120—130、小麦 1.10—1.20 美元），等待突破才顺突破方向建仓；区间内猜方向是"人们损失的金钱左一百万、右一百万"的主因。
  tags: [rule, range, breakout]

- id: p36
  title: 首笔试探为总额度五分之一
  type: calculation
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "随着市场逐渐上升，他应该亦步亦趋逐渐加仓。起初，他只买进全部额度的五分之一。如果这笔头寸未形成账面利润，他绝不可以增加持仓。"
  summary: |
    【作者】股票建仓的比例口径：首笔=计划总额度的 1/5，账面盈利为加码前提；亏损时纸带含义从"涨"变为"等一等"。这是原书少见的仓位数字。
  tags: [calculation, position-sizing, one-fifth]

- id: p37
  title: 棉花梯度加码 1:1:2（10 点/20 点台阶）
  type: calculation
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "假设我决定投入的总额度为 4 万～5 万包……我会先买进 1 万包。如果市场比我最初买进的价格上涨了 10 个点，我就再吃进另外 1 万包……如果我能取得每包 20 个点……就会再买进 2 万包。"
  summary: |
    【作者】期货加码梯度口径：总额度 4—5 万包，按 1 万→1 万→2 万包递增（1:1:2），台阶为 +10 点、+20 点；首笔或次笔浮亏立即全平。试探止损成本约"5 万或 6 万美元"，由后续主行情覆盖。missing: 大宗商品"1 点=1 美分"（第 14 章脚注）。
  tags: [calculation, pyramiding, futures, gradient]

- id: p38
  title: 帕特·赫恩体系：逐笔 100 股、1 个点止损上限
  type: calculation
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "他会先买进某只活跃股 100 股，如果它有 1 个点的上涨，这时再买入另一笔 100 股……总要在最后一笔买入的成交价格的 1 个点之下设置止损指令……只要超过 1 个点，都是没有任何道理的。"
  summary: |
    【作者】完整的机械化下注体系：+1 点加 100 股，止损=最后成交价−1 点且随上涨上移；无论亏损出自本金还是账面利润，上限均为 1 个点。反例：罗伯茨弃用该体系 15000 美元利润归零。missing: 体系隐含震荡市反复止损的成本未量化。
  tags: [calculation, stop-loss, mechanical-system]

- id: p39
  title: 希望与恐惧必须倒过来用
  type: principle
  source_chapter: 第 10 章 守候行情关键时刻（作者）
  source_quote: |
    "在天性让你充满希望的时候，不可希望，而是必须戒惧戒惕；在天性让你恐惧的时候，不可恐惧，而是必须满怀希望。"
  summary: |
    【作者】亏损两大根源：亏损时抱希望（不接受最初损失，"亏损反而变本加厉"）、盈利时怀恐惧（过早平仓）。封底六原则之一（防范你自己）。
  tags: [principle, psychology, hope-fear]

- id: p40
  title: 没有哪个活人能够击败股票市场
  type: principle
  source_chapter: 第 10 章 / 第 24 章（作者）
  source_quote: |
    "某人在某一时期有可能战胜某只股票甚至某一类股票，但是没有哪个活人能够击败股票市场！""没有人能够始终如一、持续不断地打败股票市场。"
  summary: |
    【作者】市场不可战胜论：交易者只能顺应并"间或"正确；第 24 章重申且写入封底六原则。为所有规则设定了收益预期上限与敬畏底线。
  tags: [principle, humility, market-limit]

- id: p41
  title: 关键点位的定义（突破即趋势信号）
  type: rule
  source_chapter: 第 10 章脚注②（丁圣元注疏）
  source_quote: |
    "关键点位指的是主要价格水平，一旦市场确定无疑地突破了这类价格水平，要么表明新趋势已经产生，要么表明调整过程结束，原有趋势恢复。"
  summary: |
    【丁注】关键点=分水岭式价格水平，突破的两种含义（新趋势产生/调整结束原趋势恢复）；"最小阻力路线"大体即趋势，突破关键点即路线显现时刻。
  tags: [rule, key-point, breakout, ding-shengyuan]

- id: p42
  title: 基本分析与纸带结合，但以纸带信号为准
  type: rule
  source_chapter: 第 10 章脚注（丁圣元注疏）
  source_quote: |
    "首先，纸带是对基本形势的验证；其次，操作时只能以纸带信号为准。"
  summary: |
    【丁注】对棉花 20 万美元教训的注疏：基本形势分析可先行，但决定性的是纸带验证；利弗莫尔"自以为可以帮市场捅破窗户纸"即背离此条的种子。
  tags: [rule, tape-verification, ding-shengyuan]

- id: p43
  title: 不为账单交易（市场不是财神爷）
  type: principle
  source_chapter: 第 12 章 巧舌如簧蔽主见（作者）
  source_quote: |
    "在华尔街，抱着让股票市场替你支付账单的念头去交易，正是最常见的亏损因由。如果死抱着这样的念头不放，终将亏光所有本金。"
  summary: |
    【作者】带具体盈利目标（大衣、账单）入市会扭曲时间预期与风险度量，"误以为这只是一半对一半的机会"；裘皮大衣案例为佐证。
  tags: [principle, motive, psychology]

- id: p44
  title: 卖掉亏损头寸、保留盈利头寸，绝不摊低成本
  type: rule
  source_chapter: 第 12 章 巧舌如簧蔽主见（作者）
  source_quote: |
    "在投机者铸成的所有大错中，几乎没有什么比企图为已经亏损的交易摊低成本更要命的了。绝对要卖掉账面亏损的头寸，永远保留账面赢利的头寸。"
  summary: |
    【作者】托马斯棉花教训的操作面：留亏卖盈（小麦 800 万美元利润空间拱手让出）是"愚蠢透顶"的反向操作；附录二第 8/9 条成文版。
  tags: [rule, stop-loss, no-averaging-down]

- id: p45
  title: 警惕权威人物的花言巧语（免疫力有限）
  type: principle
  source_chapter: 第 12 章 巧舌如簧蔽主见（作者）
  source_quote: |
    "交易者的另一个危险的敌人是容易受到一位吸引力难以抗拒的人物以非凡的才华表达出来的似是而非之论的感染。"
  summary: |
    【作者】珀西·托马斯代价数百万美元的教训：被说服到"将信将疑、犹豫不决"比被直接说反更糟——丧失信心即无法安心交易；图书推销商故事证明无人有完全免疫力。
  tags: [principle, persuasion, independence]

- id: p46
  title: 感恩与人情不得压倒独立判断
  type: principle
  source_chapter: 第 13 章 诡计羁绊遭利用（作者）
  source_quote: |
    "允许任何人情世故的考虑压倒自己的独立判断，既不恰当也极为不明智。感恩图报诚然品行高贵，但是，在股票市场上来不得。"
  summary: |
    【作者】威廉森事件：感激缚手脚致错过百万美元机会、负债更重；"感激是一位体面人不可缺少的感情成分，然而必须把它克制在一定范围之内，不能把自己的手脚完全捆起来。"
  tags: [principle, gratitude, independence]

- id: p47
  title: 债务焦虑毁判断力；本金与生活隔离
  type: principle
  source_chapter: 第 13 章 / 第 14 章（作者）
  source_quote: |
    "只要我处在焦虑不安的心理状态，就绝不能够完成任何有益的事务。""我把另外相当大一笔钱投入到年金中。我下定决心，再也不能被捆住手脚。"
  summary: |
    【作者】负债（尤其可随意骚扰的债权人）使身心无法投入交易，1914 年申请破产以解脱；获救后立即以年金+妻儿信托隔离生活费，"不冒任何风险"。
  tags: [principle, debt, capital-segregation]

- id: p48
  title: 没有足够本金就不可能有良好判断力
  type: principle
  source_chapter: 第 14 章 行情惨淡债务缠身（作者）
  source_quote: |
    "除非拥有足够的本金，否则不可能拥有良好的判断力。没有足够的保证金，要对这个行当采取冷静、不带感情的客观态度是不可能的。"
  summary: |
    【作者】1915 年 6 周盯盘不动手的依据：500 股额度下首笔必须稳操胜券，故等待伯利恒钢铁逼近 98→100 关键点才出手；本金规模决定可承受的试错次数。
  tags: [principle, capital, waiting]

- id: p49
  title: 领头羊滞涨是牛市终结的警告信号
  type: rule
  source_chapter: 第 14 章 行情惨淡债务缠身（作者）
  source_quote: |
    "过去那些充当牛市领头羊的股票一个接一个从其顶部下跌了几个点，这是几个月以来首次出现的现象，之后再也没有涨回去，这正是我长期以来一直小心守候的警告信号。"
  summary: |
    【作者】1916 年逃顶实操：老领头羊回落 6—7 个点不再收复→卖出滞涨股（每只 5000 股×12 只），转做新领头羊多头；整体转熊确认（每只 4 点利润）后空头加倍。"炒股票炒领头羊"（译注）。
  tags: [rule, leading-stock, top-signal]

- id: p50
  title: 绝不求卖最高点：等回落不能涨再卖
  type: rule
  source_chapter: 第 14 章 行情惨淡债务缠身（作者）
  source_quote: |
    "绝不要企图卖到最高点，否则是不明智的。等行情回落后，如果市场不能上涨，再卖出。"
  summary: |
    【作者】顶部确认式退出：放弃最后一次上冲，以"回落失败"为卖出触发；与 p18（不抓尾部 1/8）同一纪律的时机面。
  tags: [rule, exit, top]

- id: p51
  title: "人为打压"100 例中 99 例是合理下跌
  type: principle
  source_chapter: 第 15 章 政府干预拉偏架（作者）
  source_quote: |
    "所谓人为打压的情形，100例中有99例实际上都属于合理的下跌，只不过是市场在下跌过程中不时加速而已。"
  summary: |
    【作者】下跌归因的先验概率：把急跌解释为"空头打压"是让人不卖的反间计贴士；若真被打压，内部人低位买进会阻止价格停留低位。
  tags: [principle, attribution, manipulation-debunk]

- id: p52
  title: 利润入银行才算数
  type: rule
  source_chapter: 第 15 章 政府干预拉偏架（作者）
  source_quote: |
    "它们时常蹂躏你，除非已经把利润存入银行账户了，否则都算不上数。"
  summary: |
    【作者】账面利润在兑现前可被规则突变、政府干预等清零（咖啡案 350 万美元泡汤）；应及时利用流动性好的时点变现（"泄密事件"急跌中平仓 150 万美元）。
  tags: [rule, profit-taking, realization]

- id: p53
  title: 把"不可预料的无妄之灾"列入绊脚石清单
  type: principle
  source_chapter: 第 15 章 政府干预拉偏架（作者）
  source_quote: |
    "正是刚刚对你说的这次经历促使我把'不可预料的无妄之灾'添加到了我的绊脚石清单上。"
  summary: |
    【作者】咖啡限价案后确立的风险分类：除市场风险外，须为政府干预、交易所规则突变等不可预见事件预留敬畏；"对投机事业带来危害的特定因素，我始终戒慎恐惧。"
  tags: [principle, risk, unforeseeable]

- id: p54
  title: 绝不听信托士
  type: principle
  source_chapter: 第 16 章 / 第 24 章（作者）
  source_quote: |
    "在我眼中，听凭贴士交易从来都是愚蠢至极的行为。""听凭'内部人'的贴士行事，将比饥荒、瘟疫、谷物歉收、政治动荡或者其他常见的意外遭际更快将你摧毁。"
  summary: |
    【作者】贴士受众是"希望的醉汉"；第 16 章婆罗洲锡业（内部人反向派发）、G.O.H.（老丈人贴士亏 3500 美元）等为证。个股异常表现才是最好的"内幕消息"。
  tags: [principle, tips, information]

- id: p55
  title: 罗斯柴尔德法：不在底部买进，总是过早卖出
  type: maxim
  source_chapter: 第 16 章 心机费尽传贴士（作者引述）
  source_quote: |
    "我从不在底部买进，而且我总是过早卖出。"
  summary: |
    【作者引述】老罗斯柴尔德自陈的获利之道：放弃极值两端（与 p18 同构），以"过早卖出"锁定确定性利润；作者以此为投机适用的格言。
  tags: [maxim, entry-exit, extremes]

- id: p56
  title: 只寻求一种迹象——内部人买进的情况
  type: rule
  source_chapter: 第 16 章 / 第 17 章（作者）
  source_quote: |
    "我是一位交易者，因此只寻求一种迹象——内部人买进的情况。"
  summary: |
    【作者】内部人行为解读清单：该涨不涨（婆罗洲锡业）、拒绝买进（切斯特汽车、圭亚那黄金）、低位沉默高位喧哗，均先于消息发出卖出信号；"即使内部人完全清楚，即使在牛市行情下也不应该买进自己的股票"。
  tags: [rule, insider-behavior, signal]

- id: p57
  title: 板块一致性：与群体对着干不明智
  type: rule
  source_chapter: 第 17 章 长期训练成本能（作者）
  source_quote: |
    "与我称为股票群体的抱团倾向对着干不明智。""经验教导我，买入一个拒绝追随群体领头羊的股票，务必慎之又慎。"
  summary: |
    【作者】牛市同板块齐涨、熊市齐跌；掉队成员=内部人知道坏事的信号（切斯特汽车、圭亚那黄金先跌后证实）；"我不能指望只在确有把握的条件下交易，必须追随大概率"。
  tags: [rule, sector-consistency, laggard]

- id: p58
  title: 成功交易者四要素：观察、经验、记忆、数学
  type: principle
  source_chapter: 第 17 章 长期训练成本能（作者）
  source_quote: |
    "观察、经验、记忆和数学，这些方面都是成功的交易者必须仰仗的。……尽力预期事态发生的可能性。"
  summary: |
    【作者】交易是需要多年训练的专业（类比医生训练）；所谓"盘感"是多年经验经潜意识压缩的快速输出，"建筑在事实的基础之上"，不是神秘能力。
  tags: [principle, training, professionalism]

- id: p59
  title: 卖空规模不超过流通盘一定比例
  type: rule
  source_chapter: 第 18 章 市场历史重演（作者）
  source_quote: |
    "我已经做空了 3 万股股票，在流通股数中已经占了较大比例，我认为明智地做空不应超过这个比例。"
  summary: |
    【作者】空头头寸占流通盘比例是逼空风险变量；热带贸易公司 3 万股即自设上限。大户视角规则，对个人投资者为降维参考（原书约束）。
  tags: [rule, short-selling, position-limit]

- id: p60
  title: 投机成功的原则假定人们将继续重复过去的错误
  type: maxim
  source_chapter: 第 19 章 市场操纵故事多（作者引述伍德洛克）
  source_quote: |
    "指导股票投机成功的原则建立在以下假定之上：未来，人们将继续重复过去曾经犯下的错误。"
  summary: |
    【作者引述并认同】全书认识论总结：方法有效性根植于人性不变（与 p06 同源）；"虽然武器改变了，但是，计谋还是那些计谋。"
  tags: [maxim, epistemology, human-nature]

- id: p61
  title: 操作规则：拉高后于下跌途中派发
  type: rule
  source_chapter: 第 20 章 批量分销需操作（作者）
  source_quote: |
    "通过操作把股票价格尽可能推升到高位，然后在市场下跌的过程中把股票卖给公众。"
  summary: |
    【作者】市场操作基本规则（基恩传承）：公众抢反弹与空头回补构成下跌途中的买盘；拉抬的目的是开发市场而非在顶部出清。识读派发行为的底层逻辑，非个人操作建议。
  tags: [rule, distribution, operator]

- id: p62
  title: 持续下跌从来不是空头打压
  type: principle
  source_chapter: 第 23 章 内部人巧借"空头打压"（作者）
  source_quote: |
    "导致行情长期持续下跌的真实原因从来都不是空头打压。当某只股票保持下跌的时候，你可以肯定该股票一定有什么地方不对，要么是它的市场，要么是它的公司。"
  summary: |
    【作者】纽黑文 255→12 美元大崩溃为例：持续下跌=内部人不断卖出且不出手支撑；"空头打压"解释的作用是阻止公众卖出。
  tags: [principle, downtrend, attribution]

- id: p63
  title: 匿名权威利好不可信
  type: rule
  source_chapter: 第 23 章 内部人巧借"空头打压"（作者）
  source_quote: |
    "我坚定不移地认为，如果不允许刊登任何利好性质的匿名言论，将会极大地减轻公众蒙受的损失。"
  summary: |
    【作者】信息鉴别规则："首要的内部人士""著名董事"等匿名利好是派发工具；利好发布时点规律——吸筹期沉默、上涨中放话、下跌时归罪空头。具名才可能负责任。
  tags: [rule, information-credibility, anonymous-authority]

- id: p64
  title: 趋势转变无需等待解释，跟随即可
  type: rule
  source_chapter: 第 24 章 到处陷阱须谨慎（作者）
  source_quote: |
    "只要股票保持上涨，并且在这过程中只是不时发生小幅的自然回落，那么追随该股票的上涨行情就是一个相当安全的策略。但是，如果某只股票经历了长期稳定的上涨行情之后，掉转方向，开始逐步下降……其最小阻力路线已经从上升转为下降。既然如此，为什么你还需要任何解释呢？"
  summary: |
    【作者】趋势跟随的操作化定义（附录三指出"基本上正是上升趋势和下降趋势的定义"）：上涨=连续买进+小幅回落→追随安全；转跌=逐步下降+偶尔回升→无需理由即离场。知情者不可能说破真相。
  tags: [rule, trend-following, exit]

- id: p65
  title: 利弗莫尔 15 条股票交易规则（成文总表）
  type: checklist
  source_chapter: 附录二（丁圣元整理）
  source_quote: |
    "买进上涨中的股票，卖出下跌中的股票。不要天天交易，只有行情明显看涨或看跌的时候才交易。交易方向与总体市场保持一致。"
  summary: |
    【丁注】原书唯一成文规则总表，逐条照录：1 买涨卖跌；2 不天天交易、方向与总体市场一致；3 交易步调与时间价格关键点相协调；4 等市场证明观点后再交易不迟，交易则兵贵神速；5 有利润继续持有、有亏损从速了结；6 事态明朗、原趋势终结时了结交易；7 做股票就做领头羊（走势最强）；8 绝不平摊亏损头寸（不补套牢仓）；9 绝不追加保证金，干脆平付认赔；10 创新高买进做多、创新低卖出做空；11 股票下跌就放手，别炒成股东；12 绝不因股价太高不可买进、太低不可卖出；13 看法千错万错，市场永远没错；14 赢利最多的交易往往一开头就有账面利润；15 没有百发百中的交易规则。与正文对应：2=p08，5/6=p50+p52，7=p49，8/9=p44，10=p30，12=p26，14=p24。规则间无优先级与冲突消解说明（阶段 0 已标注）。
  tags: [checklist, rules-list, livermore, ding-shengyuan]

- id: p66
  title: 趋势定义三分类与"更高/更低"的辨识阈值
  type: calculation
  source_chapter: 附录三 市场最小阻力路线（丁圣元注疏）
  source_quote: |
    "上升趋势的定义是市场行情走出了更高的高点、更高的低点……下降趋势……更低的低点、更低的高点……横向趋势……既无明显的新高，也无明显的新低。""相差 0.5% 以内，人们的感觉或许不那么明显，而相差 5% 以上则十分明显。"
  summary: |
    【丁注】趋势的操作化定义：上升（更高高点+更高低点）、下降（更低低点+更低高点）、横向（无新高无新低）。"更高/更低"为定性描述，须达到多数参与者明显可辨的程度——0.5%/5% 仅为感知举例而非硬阈值；视觉共识优先于想法观点。inputs: 相邻高/低点对；output: 趋势三分类；missing: 无统一量化阈值（原文明示按常识理解）。
  tags: [calculation, trend-definition, ding-shengyuan]

- id: p67
  title: 行情演变的基本模式：密集区与突破交替
  type: principle
  source_chapter: 附录三 市场最小阻力路线（丁圣元注疏）
  source_quote: |
    "行情演变的基本模式是调整与突破交替进行的模式，或者说密集区（区块）—快速变化（线条）交替的模式。""重力"方向就是趋势方向，最小阻力路线便是行情趋势的方向。
  summary: |
    【丁注】以倒水试验给出最小阻力路线的机制论证：市场"不停地试"以发现价格，水团（密集区）—突破—线条交替即趋势的实现方式；"事后可以合理解释"与"当时知晓"不可混淆——只能从突破把握动向。
  tags: [principle, consolidation-breakout, mechanism, ding-shengyuan]

- id: p68
  title: 杰西·利弗莫尔的交易原则（封底六条）
  type: checklist
  source_chapter: 封底"杰西·利弗莫尔的交易原则"（出版社编辑）
  source_quote: |
    "不要企图抓住行情最后的 1/8 美元——或者行情最初的 1/8 美元。这两个 1/8 美元，是世上最昂贵的 1/8 美元。"
  summary: |
    【封底】出版社提炼的六条：1 股票市场只有一个方面——正确的方面（=p10）；2 不抓头尾两个 1/8 美元（=p18）；3 价格沿阻力最小的路线运动（=p33）；4 交易方法简单但最重要的是防范你自己——警惕你的人性（=p39）；5 站在正确一面的人得到两股力量帮助：基本形势+站在错误一面的人（第 10 章）；6 没有人能始终如一、持续不断地打败股票市场（=p40）。可作全书原则的官方摘要卡。
  tags: [checklist, maxim-set, backcover]
```

## 覆盖自检

- [x] 全书分 10 块通读（1—3666 行，无跳读）：译者前言、第 1—24 章、附录一/二/三、封底
- [x] 附录二 15 条逐条照录于 p65；附录三趋势定义与阈值照录于 p66/p67；封底六条照录于 p68
- [x] 数字口径精确照录：首笔 1/5 额度（p36）、棉花 1:1:2 梯度与 10/20 点台阶（p37）、帕特·赫恩 1 个点止损上限（p38）、整数关 30—50 点（p30）、阿纳康达 301（p31）、"人为打压"99/100（p51）、领头羊 5000 股×12 只与 4 点加倍（p49）
- [x] 作者原则与丁圣元注疏原则分别标注（p01—p05、p41、p42、p65—p67 为丁注/整理，p68 为封底）
- [x] 引用均 ≤150 字；缺省条件（首笔仓位百分比、止损幅度、趋势量化阈值）已标注 missing，未以常识补齐
- [x] 与 framework/counter-example 的边界项（盘感解释、具体战役情节、破产归因）未纳入本清单，留待相应 extractor
