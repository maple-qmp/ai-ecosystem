---
title: GPT Image（含 DALL·E）
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["GPT Image", "gpt-image-1", "gpt-image-2", "ChatGPT Images", "DALL·E", "DALL-E", "DALL-E 3"]
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
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]"]
---

# GPT Image（含 DALL·E）

## 描述

[[entities/openai|OpenAI]] 的图像生成模型线，前身是 DALL·E（2021-01）、DALL·E 2（2022-04）和 DALL·E 3（2023-10，接入 ChatGPT）。2025-03 起改由 GPT-4o 原生出图，API 名为 gpt-image-1，图像生成从独立的[[concepts/diffusion-model|扩散模型]]品牌变成 [[entities/gpt|GPT]] 多模态模型的一项能力。2025-12 ChatGPT 默认换成 GPT Image 1.5，DALL·E 2 / 3 于 2026-05-12 从 API 下线。2026-04-21 的 ChatGPT Images 2.0（gpt-image-2）会在出图前先推理，文字渲染明显更准。全线闭源，只通过 ChatGPT 和 API 提供。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，图像生成）
- **上游依赖**：[[entities/gpt|GPT]]（GPT-4o 起原生出图）
- **竞争 / 替代**：[[entities/imagen|Imagen]] 与 Gemini 的 Nano Banana、[[entities/flux|FLUX]]、[[entities/stable-diffusion|Stable Diffusion]]、字节 Seedream（见 [[entities/seedance|Seedance / 即梦]]）

## 时间线

- 2021-01 DALL·E
- 2022-04 DALL·E 2
- 2023-10 DALL·E 3，集成进 ChatGPT
- 2025-03 GPT-4o 原生图像生成上线 ChatGPT，随后 gpt-image-1 进入 API
- 2025-11-14 通知 DALL·E 2 / 3 将于 2026-05-12 从 API 移除
- 2025-12 ChatGPT 默认图像模型改为 GPT Image 1.5
- 2026-04-21 ChatGPT Images 2.0 / gpt-image-2（出图前推理）
- 2026-05-12 DALL·E 2 / 3 从 API 下线

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/sora|Sora]]
- [[entities/imagen|Imagen]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

（本次未能直接读取 OpenAI 官方页面，暂无逐字摘录；事实来自二手报道，见 [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]）
