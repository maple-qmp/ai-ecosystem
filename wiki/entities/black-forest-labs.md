---
title: Black Forest Labs
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["Black Forest Labs", "BFL", "黑森林实验室"]
released: "2024-08"
competitors: ["[[entities/stability-ai]]", "[[entities/openai]]", "[[entities/google-deepmind]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Black Forest Labs

## 描述

德国弗赖堡的视觉生成实验室，2024 年由 Robin Rombach（CEO）、Andreas Blattmann、Patrick Esser 和另外 7 人创立。三位创始人曾在 LMU 慕尼黑 Björn Ommer 组做出 Latent Diffusion，后来在 [[entities/stability-ai|Stability AI]] 工作，Stability 2023 年陷入财务困境后离开。产品是 [[entities/flux|FLUX]] 模型家族：一部分开放权重，最强档只走 API（bfl.ai）。2024-08-01 公开亮相时拿到 a16z 领投的 3100 万美元种子轮；2025-12 完成 3 亿美元 B 轮，估值 32.5 亿美元（报道口径；Wikipedia 写年底融资 4.5 亿美元），投资方包括 Salesforce Ventures、a16z、[[entities/nvidia|NVIDIA]]、Adobe、Canva 等，投资方大多也是客户。2026 年它从图像扩展到视频、音频和机器人动作预测（FLUX 3），但仍自称研究实验室；2026-06 约 70 人，8 月约 100 人，其中约 30 人在旧金山。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室（L2 视觉生成模型）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/stability-ai|Stability AI]]、[[entities/openai|OpenAI]]（GPT Image）、[[entities/google-deepmind|Google DeepMind]]（Nano Banana、Veo / Omni）

## 时间线

- 2024-08-01 公开亮相，发布 FLUX.1，3100 万美元种子轮
- 2025-01 与 NVIDIA 合作；推出 FLUX Pro 微调 API
- 2025-05-29 FLUX.1 Kontext 与 BFL Playground
- 2025-11-25 FLUX.2
- 2025-12-01 3 亿美元 B 轮，估值 32.5 亿美元（二手）
- 2026-06 Martin Scorsese 出任顾问，引发创作者与美术指导工会反对
- 2026-07-23 FLUX 3 多模态模型进入早期访问
- 2026-10-15 FLUX 3 Image Klein（5.6B 开放权重）

## 相关实体

- [[entities/flux|FLUX]]
- [[entities/stability-ai|Stability AI]]
- [[entities/nvidia|NVIDIA]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "This repo contains minimal inference code to run image generation & editing with our FLUX.2 open-weight models." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（black-forest-labs/flux2 README）
