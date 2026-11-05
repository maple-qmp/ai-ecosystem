---
title: FLUX
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["FLUX", "Flux", "FLUX.1", "FLUX.2", "FLUX Kontext", "FLUX.2 klein"]
org: "[[entities/black-forest-labs|Black Forest Labs]]"
released: "2024-08"
open_weights: true
competitors: ["[[entities/stable-diffusion]]", "[[entities/gpt-image]]", "[[entities/imagen]]", "[[entities/seedance]]"]
depends_on: ["[[entities/pytorch]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# FLUX

## 描述

[[entities/black-forest-labs|Black Forest Labs]] 的图像生成与编辑模型家族，团队是 Latent Diffusion / [[entities/stable-diffusion|Stable Diffusion]] 的原作者。它采用开放与闭源分档：FLUX.1 [schnell] 和 FLUX.2 [klein] 4B 用 Apache-2.0，[dev] 档开放权重但只许非商用，Pro / Flex / Max 只走 API。FLUX.1 之后出了 Fill、Canny、Depth、Redux、Kontext（编辑）、Krea 等 [dev] 衍生模型。FLUX.2 [dev]（2025-11-25）是 32B 参数的 flow matching transformer，支持多参考图编辑；FLUX.2 [klein]（2026-01-15）是 4B / 9B 的蒸馏模型，消费级 GPU 上亚秒出图。它是 2025 年以来最常用的开放权重图像模型，第三方称 FLUX.2 [max] 在 2026-08 的 Artificial Analysis 图像榜排第一（二手）。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重 + API，图像生成）
- **上游依赖**：[[entities/pytorch|PyTorch]]；量化版与 [[entities/hugging-face|Hugging Face]] diffusers 合作
- **竞争 / 替代**：[[entities/stable-diffusion|Stable Diffusion]]、[[entities/gpt-image|GPT Image]]、[[entities/imagen|Imagen]]（及 Gemini 的 Nano Banana）、字节的 Seedream（见 [[entities/seedance|Seedance / 即梦]]）

## 时间线

- 2024-08-01 FLUX.1（pro / dev / schnell），与 Black Forest Labs 一同亮相
- 2025-11-25 FLUX.2 [dev]，32B
- 2026-01-15 FLUX.2 [klein] 4B / 9B / 9B KV 及 Base 版
- 2026-08 FLUX.2 [max] 据称居 Artificial Analysis 图像榜首（二手）

## 相关实体

- [[entities/black-forest-labs|Black Forest Labs]]
- [[entities/stable-diffusion|Stable Diffusion]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]
- [[concepts/lora|LoRA]]
- [[concepts/kv-cache|KV Cache]]（klein 9B KV 用 KV 缓存加速多参考图编辑）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "`FLUX.2 [dev]` is a 32B parameter flow matching transformer model capable of generating and editing (multiple) images." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（black-forest-labs/flux2 README）
- "FLUX.2 [klein] is our fastest model family — generating and editing (multiple) images in under a second without sacrificing quality." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（black-forest-labs/flux2 README）
