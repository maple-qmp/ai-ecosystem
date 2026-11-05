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
updated: 2026-11-05
sources: ["[[sources/ai-policy-survey-2026-11]]"]
---

# 加州 SB 53

## 定义

美国第一部专门针对前沿 AI 模型开发者的州法，全称《前沿人工智能透明度法》（Transparency in Frontier Artificial Intelligence Act，TFAIA）。2025-09-29 由州长签署（Chapter 138, Statutes of 2025），2026-01-01 起施行。核心是透明度与事件报告：要求大型前沿开发者公开自己的前沿 AI 安全框架，发布透明度报告，并在 15 天内报告关键安全事件。

## 关键特征

- **门槛**：“前沿模型”指训练算力超过 10^26 次整数或浮点运算的基础模型；“大型前沿开发者”指连同关联方上一年总收入超过 5 亿美元的前沿开发者
- **灾难性风险**：可预见且实质性地促成单次事件中 50 人以上死亡或重伤、或 10 亿美元以上财产损失的风险
- **前沿 AI 框架**：大型前沿开发者须编写、执行、遵守并在官网显著公开，说明如何评估和缓解灾难性风险
- **透明度报告**：发布新的或经实质修改的前沿模型时发布；大型开发者还需附灾难性风险评估摘要，并定期向加州紧急服务办公室（OES）提交内部使用风险评估摘要（二手）
- **事件报告**：发现关键安全事件后 15 天内向 OES 报告
- **吹哨人保护**与内部匿名举报渠道
- **罚则**：违规按严重程度处以每次不超过 100 万美元的民事罚款

## 纽约 RAISE Act

- 2025-12 州长 Hochul 附条件签署，2026-03-27 签署章节修正案向 SB 53 靠拢，2027-01-01 生效；同样以 10^26 运算和 5 亿美元收入为门槛；执法机构为纽约金融服务局内新设的办公室；民事罚款降为 100 万 / 300 万美元（二手）

## 应用

- 实际受约束的是少数大型前沿实验室；[[entities/anthropic|Anthropic]] 以公开的 Frontier Compliance Framework 应对 SB 53 等要求，企业原有的[[concepts/frontier-safety-frameworks|前沿模型安全框架]]由此变成法定披露义务

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 政策法规（美国州法）
- **张力**：联邦 EO 14365 试图抑制州 AI 法（见[[concepts/us-federal-ai-policy|美国联邦 AI 行政令]]）

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
