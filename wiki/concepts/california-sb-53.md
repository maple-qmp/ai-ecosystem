---
title: 加州 SB 53
type: concept
tags: [standard]
layer: X
aliases: ["加州 SB 53", "SB 53", "Transparency in Frontier Artificial Intelligence Act", "TFAIA", "前沿人工智能透明度法", "RAISE Act", "纽约 RAISE 法案"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-policy-survey-2026-11]]"]
---

# 加州 SB 53

## 定义

美国第一部专门规范前沿 AI 模型开发者的州法，全称《前沿人工智能透明度法》（Transparency in Frontier Artificial Intelligence Act，TFAIA）。2025-09-29 由州长签署（Chapter 138, Statutes of 2025），2026-01-01 起施行。核心是透明度和事件报告：大型前沿开发者须公开自己的前沿 AI 安全框架、发布透明度报告，并在 15 天内报告关键安全事件。

## 关键特征

- **门槛**：“前沿模型”指训练算力超过 10^26 次整数或浮点运算的基础模型；“大型前沿开发者”指连同关联方上一年总收入超过 5 亿美元的前沿开发者
- **灾难性风险**：可预见且实质性地促成单次事件中 50 人以上死亡或重伤，或 10 亿美元以上财产损失的风险
- **前沿 AI 框架**：大型前沿开发者须编写、执行、遵守，并在官网显著公开，说明如何评估和缓解灾难性风险
- **透明度报告**：发布新的或经实质修改的前沿模型时发布；大型开发者还要附灾难性风险评估摘要，并定期向加州紧急服务办公室（OES）提交内部使用风险评估摘要（二手）
- **事件报告**：发现关键安全事件后 15 天内向 OES 报告
- **吹哨人保护**，以及内部匿名举报渠道
- **罚则**：按严重程度，每次违规不超过 100 万美元民事罚款

## 纽约 RAISE Act

- 2025-12-19 州长 Hochul 签署，附带让法律向 SB 53 靠拢的章节修正案（A9449 / S8828）；预计 2027-01-01 生效（二手）
- 门槛与加州相同（10^26 次运算、年收入 5 亿美元），高校学术研究豁免
- **比加州更严之处**：
  - 前沿 AI 框架要“详细”描述风险评估、未发布权重的安保、第三方评测、内部使用治理和事件响应，每年至少复审一次
  - 关键安全事件须在 **72 小时**内报告，存在迫在眉睫的死亡或重伤风险时 **24 小时**内报告（加州为 15 天）
- 纽约金融服务局（DFS）内设新办公室负责监督；州检察长可提起民事诉讼，首次违规最高 100 万美元，之后最高 300 万美元；无私人诉权

## 应用

- 实际受约束的是少数大型前沿实验室。[[entities/anthropic|Anthropic]] 以公开的 Frontier Compliance Framework 应对 SB 53 等要求，[[entities/openai|OpenAI]] 2026-05 发布了针对加州和欧盟要求的 Frontier Governance Framework（二手）。企业原有的[[concepts/frontier-safety-frameworks|前沿模型安全框架]]由此变成法定披露义务

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 政策法规（美国州法）
- **张力**：联邦 EO 14365 指示司法部挑战州 AI 法（见[[concepts/us-federal-ai-policy|美国联邦 AI 行政令]]）

## 相关概念

- [[concepts/frontier-safety-frameworks|前沿模型安全框架]]
- [[concepts/us-federal-ai-policy|美国联邦 AI 行政令]]
- [[concepts/eu-ai-act|欧盟《人工智能法》]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/meta-ai|Meta AI]]
- [[entities/xai|xAI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "“Frontier model” means a foundation model that was trained using a quantity of computing power greater than 10^26 integer or floating-point operations." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "a frontier developer shall report any critical safety incident pertaining to one or more of its frontier models to the Office of Emergency Services within 15 days of discovering the critical safety incident." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
