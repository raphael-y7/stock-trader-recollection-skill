# Stage 4 压力测试摘要

> 本书包：股票大作手回忆录（丁圣元注疏版） · 10 个能力单元 · single 1 入口 / pack 8 入口
> 数据来源：`evals/test-results.md`、`evals/test-prompts.json`、归档 `审计过程/PIPELINE_STATE.md`
> 记录日期：2026-10-24（ZCode / GLM-5.3-flash，1M 上下文）

## 测试范围

- **skill 数量**：10 个能力单元 —— 7 张 promoted（`min-resistance-trend`、`key-point-trading`、`probe-and-scale-in`、`position-holding-exit`、`mind-state-discipline`、`tips-and-authority-defense`、`stock-sector-behavior`）+ 3 张 router（`liquidity-and-execution`、`forecast-log`、`livermore-rules-checklist`）；编译后为 single 1 个入口、pack 8 个可发现入口。
- **test-prompts 文件**：1 份 suite 级文件（`evals/test-prompts.json`；仓库内 `single/stock-trader-recollection-skill/test-prompts.json` 是同一份副本，内容逐字一致），内含 10 个 skill 块 × 9 条 = **90 条触发用例**。
- **覆盖类型**：`should_trigger` 40 条、`should_not_trigger` 30 条（跨卡混淆诱饵 29 + 一般诱饵 1）、`edge_case` 20 条。
- **输出用例**：归档另有 `审计过程/tests/output-cases.json` 22 条，本次未收入仓库；仓库只保留 `evals/test-results.md` 中的逐项记录。
- **测试方式**：触发为独立盲测 sub-agent（只给 10 个技能的 name + description 菜单与 prompt 文本）；输出为独立执行 sub-agent（只读任务与卡片、不读断言），配机械断言 + 人工复核。

## 结构检查

以下为本次实测结果（检查脚本只读，未改动文件）：

- **JSON 可解析性**：`evals/test-prompts.json` 与 `single/stock-trader-recollection-skill/test-prompts.json` 均可被 `json.load` 解析，两者内容完全一致（10 个 skill 块、90 条用例）。
- **frontmatter**：9 个 `SKILL.md`（single 入口 1 + pack 路由入口 1 + pack 独立 skill 7）全部带 YAML frontmatter，`name` / `description` 字段齐全。
- **六段完整性**：10 张能力卡在 `bundle/cards/`、`single/.../references/capabilities/`、`pack/stock-trader-recollection-skill-router/references/capabilities/` 三处各 10 份，R / I / A1 / A2 / E / B 六段全部齐全；pack 下 7 张单文件卡同样六段齐全。
- **路由入口结构**：`pack/stock-trader-recollection-skill-router/SKILL.md` 按设计使用「触发与不触发 / 核心原则 / 能力路由 / 加载规则 / 边界与判停」五段，不套能力卡六段，属预期结构，不计为缺段。
- **candidates/**：已从归档 `审计过程/candidates/` 补齐 5 份文本候选（`framework.md`、`principle.md`、`case.md`、`counter-example.md`、`glossary.md`），无图片 / PDF 入仓。
- **构建清单**：`BUILD_MANIFEST.json` 的 `published_hashes` 与当前文件逐一核对通过（single 15 条、pack 23 条，无缺失、无哈希不符）；`test-prompts.json` 属编译后新增文件，不在 manifest 的哈希清单内，本次也未重跑 `validate`。

## 结果

- **skills**：10
- **test_json**：1（suite 级，90 条触发用例；输出用例 22 条仅在归档，未入仓）
- **通过情况**（摘自 `evals/test-results.md`，未作改写）：
  - 触发盲测：**86 / 90（95.6%）** —— should_trigger 40 / 40、跨卡混淆诱饵 29 / 29、一般诱饵 1 / 1、edge_case 16 / 20。
  - 4 条 edge（预测明日涨跌、求情感陪伴、代生成预测、规则排序）被盲测员判为「不激活」，理由与各卡 B 段边界一致；按方法论「修测试」重新归类为边界输出用例，不计为路由失败。
  - 首轮正向为 39 / 40：`min-resistance-trend-skill-st-04`（研报基本面与股价背离）被误路由到信息防御卡；判定为修 skill（收窄两卡 description 的「消息与盘面背离」重叠），修复后独立复测通过。
  - 输出质量：**22 / 22** 用例通过，机械断言 22 / 22；完成方式分布为正常完成 12、判停询问 7、拒绝误用 3。
- **局限（原报告已如实声明）**：每用例单次运行，未做多轮稳定性测试；无 old_skill 基线、无 without_skill 对照组；触发盲测基于 description 文本，未在真实宿主 skill 机制上验证；90 条未切分 train / validation。

## 可接入 darwin-skill 的后续动作

- **直接作回归样本**：90 条触发用例（含 30 条 should_not_trigger、20 条 edge）可整包接入，改动 description 或路由表后重跑；重点盯跨卡混淆诱饵是否回退——这是原报告里唯一判定为「真实失败」的维度。
- **输出评分器迁移**：`test-results.md` 记录的判分口径（must_include / must_not_include / 判停三分类）可改写成 darwin-skill 的输出断言；如需复现，得先把归档的 `output-cases.json`（22 条）随样本一起入仓。
- **切分隐藏集**：按 60 / 40 切 train / validation 并保留隐藏集，避免用全量 90 条调参造成过拟合。
- **补真实宿主回归**：现有盲测是 description 文本模拟，建议在真实 skill 机制上补一轮，验证激活链路。
- **建议回归门槛**：should_trigger ≥ 95%、跨卡诱饵 100%、edge 拒答行为不得回退；任一不达即按「修 skill」回炉，不用改测试的方式放过。
