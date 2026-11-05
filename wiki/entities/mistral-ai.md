---
title: Mistral AI
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["Mistral AI", "Mistral"]
released: "2023-04"
competitors: ["[[entities/meta-ai]]", "[[entities/openai]]", "[[entities/alibaba]]"]
depends_on: ["[[entities/nvidia]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/open-weight-flagships-survey-2026-11]]"]
---

# Mistral AI

## 描述

2023-04 由 Arthur Mensch（前 DeepMind）、Guillaume Lample 和 Timothée Lacroix（均来自 Meta）在巴黎创立的模型公司，产品是 [[entities/mistral-models|Mistral 模型]]系列和聊天应用 Le Chat（2026-05 改名 Mistral Vibe）。2026-09 三星入股后估值约 210 亿欧元（约 247 亿美元），是欧洲估值最高的 AI 公司；ASML 2025-09 投资 13 亿欧元，持股 11%。它是欧盟“数字主权”政策的主要受益者，2026 年起在巴黎和瑞典自建数据中心，最大模型 Mistral Large 4 在自有欧洲机房用 NVIDIA Grace Blackwell 训练。与微软的合作从 2024-02 的小额投资扩展到 2026-07 的数十亿美元基础设施协议。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：[[entities/nvidia|NVIDIA]]
- **竞争 / 替代**：[[entities/meta-ai|Meta AI]]、[[entities/openai|OpenAI]]、[[entities/alibaba|阿里巴巴（通义）]]

## 时间线

- 2023-04 成立
- 2023-06 种子轮 1.05 亿欧元
- 2023-12 第二轮 3.85 亿欧元（a16z 等），估值超 20 亿欧元
- 2024-02 Le Chat 上线；微软投资
- 2024-06 融资 6 亿欧元，估值 58 亿欧元
- 2025-09 ASML 领投，估值 120 亿欧元
- 2026-02 收购 Koyeb；与 Accenture 合作
- 2026-03 融资 8.3 亿美元建数据中心；与 NVIDIA 合作开发开放前沿模型
- 2026-05 收购 Emmi AI；Le Chat 改名 Mistral Vibe
- 2026-07 与微软签数十亿美元欧洲基础设施协议
- 2026-09 三星入股，估值 210 亿欧元
- 2026-10 Mistral Large 4 开放权重

## 相关实体

- [[entities/mistral-models|Mistral 模型]]
- [[entities/meta-ai|Meta AI]]
- [[entities/microsoft|Microsoft]]
- [[entities/nvidia|NVIDIA]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Mistral Large 4 is our largest and most capable model to date: a 1 trillion-parameter natively multimodal Mixture-of-Experts model with 49 billion active parameters per token (52 billion including embeddings and output layers), trained from scratch on 3,800 NVIDIA Grace Blackwell GPUs in Mistral's own datacenters in Europe." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（Mistral Large 4 模型卡）
