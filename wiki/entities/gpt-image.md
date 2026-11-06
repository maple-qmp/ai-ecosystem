---
title: GPT Image（含 DALL·E）
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["GPT Image", "gpt-image-1", "gpt-image-2", "GPT-Image-2.5", "GPT-Image-2.6", "ChatGPT Images", "DALL·E", "DALL-E", "DALL-E 3"]
org: "[[entities/openai|OpenAI]]"
released: "2021-01"
open_weights: false
competitors: ["[[entities/imagen]]", "[[entities/flux]]", "[[entities/stable-diffusion]]", "[[entities/seedance]]"]
depends_on: ["[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]"]
---

# GPT Image（含 DALL·E）

## 描述

[[entities/openai|OpenAI]] 的图像生成与编辑模型线。前身是[[concepts/diffusion-model|扩散模型]] DALL·E（2021-01）、DALL·E 2（2022）和 DALL·E 3（2023-10 接入 ChatGPT）。2025-03-25 起改由 GPT-4o 原生出图，此后的 GPT Image 是**自回归**模型，图像生成成了 [[entities/gpt|GPT]] 多模态能力的一部分；上线首周有 1.3 亿用户生成了 7 亿多张图，“吉卜力风”刷屏。之后迭代很快：gpt-image-1（2025-04 进 API）、1.5（2025-12-16）、gpt-image-2（2026-04-21，出图前先推理）、2.5（2026-09-08）、2.6（2026-11-04）。从 2.5 起每代分 Sunburst（细节）和 Flare（快速）两档，2.6 还能生成 SVG 和动图 GIF。旧版本淘汰也快：DALL·E 2 / 3 于 2026-05-12、gpt-image-1 于 2026-10-23 从 API 下线，gpt-image-1-mini 与 1.5 将于 2026-12-01 下线。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，图像生成）
- **上游依赖**：[[entities/gpt|GPT]]（GPT-4o 起原生出图）
- **竞争 / 替代**：[[entities/imagen|Imagen]] 的后继 Nano Banana（见 [[entities/gemini|Gemini]]）、[[entities/flux|FLUX]]、[[entities/stable-diffusion|Stable Diffusion]]、字节 Seedream（见 [[entities/seedance|Seedance / 即梦]]）

## 时间线

- 2021-01 DALL·E
- 2022 DALL·E 2
- 2023-10 DALL·E 3 接入 ChatGPT，11 月进 API
- 2025-03-25 GPT-4o 图像生成，ChatGPT 中取代 DALL·E 3
- 2025-04-23 gpt-image-1 进入 API
- 2025-10-06 gpt-image-1-mini（DevDay）
- 2025-11-14 通知 DALL·E 2 / 3 将于 2026-05-12 从 API 移除
- 2025-12-16 GPT Image 1.5，作为“ChatGPT Images”向全部用户推出
- 2026-04-21 gpt-image-2（引入推理）；次日宣布 gpt-image-1 于 10-23 下线
- 2026-05-12 DALL·E 2 / 3 从 API 下线
- 2026-06-02 宣布 gpt-image-1-mini、gpt-image-1.5 于 2026-12-01 下线
- 2026-09-08 GPT-Image-2.5 Sunburst / Flare
- 2026-10-23 gpt-image-1 下线
- 2026-11-04 GPT-Image-2.6 Sunburst / Flare（SVG、动图 GIF）

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/sora|Sora]]
- [[entities/imagen|Imagen]]
- [[entities/microsoft|Microsoft]]（Bing Image Creator / Copilot 用 DALL·E 3）

## 相关概念

- [[concepts/diffusion-model|扩散模型]]（DALL·E 2 / 3；GPT Image 不是）
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Unlike the diffusion predecessors of DALL-E 2 and DALL-E 3 models, GPT Image models are autoregressive with several new capabilities including image-to-image transformation, advanced photorealism and detailed instruction following." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wikipedia）
