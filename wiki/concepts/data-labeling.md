---
title: 数据标注
type: concept
tags: [method]
layer: L1
aliases: ["Data Labeling", "Data Annotation", "数据标注", "人类数据", "专家数据"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-07
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# 数据标注

## 定义

由人为模型训练产出标签、示范回答、偏好比较和反馈的工作，是监督微调与 RLHF 的数据来源。在 LLM 时代，它从低价众包转向高价的领域专家数据：医生、科学家、律师、程序员按小时为实验室写示范、打分、指导强化学习。

## 关键特征

- **专家化**：[[entities/mercor|Mercor]] 撮合 3 万多名领域专家，按小时收撮合费；[[entities/scale-ai|Scale AI]] 2025 年把 GenAI 数据业务收缩为代码、语言、专家、实验、音频五个方向
- **大额资本**：2025-06 [[entities/meta-ai|Meta]] 投资 Scale AI，Scale 称估值超过 290 亿美元（Reuters 报道为约 143 亿美元、49% 股份）；2025 年 [[entities/surge-ai|Surge AI]] 传出 150 亿–250 亿美元估值的融资洽谈，Mercor 估值 100 亿美元（二手报道）
- **格局变化**：报道称 Surge 2024 年收入（超过 10 亿美元）已高于 Scale（约 8.7 亿美元）
- **与合成数据的关系**：[[concepts/synthetic-data|合成数据]]降低了对人工标注的依赖（Nemotron-4-340B 对齐数据 98% 以上为合成），但仍保留约 2 万条人工标注，用于微调和奖励模型训练
- **风险**：外包规模大、涉及个人信息和客户的训练机密。例如 Mercor 2026-03 因开源工具 [[entities/litellm|LiteLLM]] 被入侵而泄露数据，[[entities/meta-ai|Meta]] 随后无限期暂停了与它的合同；Surge AI 2025 年被集体诉讼指控把标注员错误归类为独立承包人
- **规模**：Surge AI 2025 年合作的标注员约 100 万人，客户覆盖 Anthropic、OpenAI、Google、Meta 等主要实验室

## 应用

- 监督微调（SFT）的示范数据
- RLHF / 偏好数据与奖励模型训练
- 评测集与红队数据

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]]
- **下游**：L3 的后训练（SFT、RLHF）

## 相关概念

- [[concepts/synthetic-data|合成数据]]

## 相关实体

- [[entities/scale-ai|Scale AI]]
- [[entities/surge-ai|Surge AI]]
- [[entities/mercor|Mercor]]
- [[entities/meta-ai|Meta AI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Mercor started off as an AI-driven hiring platform but quickly pivoted to providing companies with specialized domain experts to perform AI model training — such as scientists, doctors, and lawyers — and charging an hourly finder’s fee and matching rate for their work." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Scale AI, Inc. (“Scale” or the “Company”), the humanity-first AI company, today announced a significant new investment from Meta Platforms, Inc. (Nasdaq: META) that values Scale at over $29 billion." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
