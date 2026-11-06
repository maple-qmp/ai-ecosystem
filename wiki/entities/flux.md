---
title: FLUX
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["FLUX", "Flux", "FLUX.1", "FLUX.2", "FLUX 3", "FLUX Kontext", "FLUX.2 klein", "FLUX 3 Video"]
org: "[[entities/black-forest-labs|Black Forest Labs]]"
released: "2024-08"
open_weights: true
competitors: ["[[entities/stable-diffusion]]", "[[entities/gpt-image]]", "[[entities/imagen]]", "[[entities/seedance]]", "[[entities/kling]]", "[[entities/veo]]"]
depends_on: ["[[entities/pytorch]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# FLUX

## 描述

[[entities/black-forest-labs|Black Forest Labs]] 的视觉生成模型家族，团队是 Latent Diffusion / [[entities/stable-diffusion|Stable Diffusion]] 的原作者。它采用开放与闭源分档：每代都有 Apache-2.0 的小模型（FLUX.1 [schnell]、FLUX.2 [klein] 4B、FLUX 3 Image Klein），[dev] 档开放权重但只许非商用，Pro / Flex / Max 只走 API。FLUX.1（2024-08）是 12B 的 rectified flow transformer，之后出了 Tools、Kontext（图文混合编辑）、Krea 等变体，被 Grok、Mistral Le Chat 和 Adobe Photoshop 接入。FLUX.2 [dev]（2025-11-25）是 32B 参数，支持多参考图编辑。FLUX 3（2026-07-23 起）不再只做图像，而是一个同时学习图像、视频和音频的统一多模态 flow 模型，分出 Video（带音频，最长 20 秒）、Image、Action（机器人动作预测）等产品，并计划开放 FLUX 3 Dev 权重。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重 + API，图像、视频与音频生成）
- **上游依赖**：[[entities/pytorch|PyTorch]]；量化版与 [[entities/hugging-face|Hugging Face]] diffusers 合作；2025-01 起与 [[entities/nvidia|NVIDIA]] 合作
- **竞争 / 替代**：图像侧 [[entities/stable-diffusion|Stable Diffusion]]、[[entities/gpt-image|GPT Image]]、[[entities/imagen|Imagen]]（及 Gemini 的 Nano Banana）、字节 Seedream；视频侧 [[entities/kling|可灵]]、[[entities/seedance|Seedance]]、[[entities/veo|Veo]] / Gemini Omni

## 时间线

- 2024-08-01 FLUX.1（pro / dev / schnell），与 Black Forest Labs 一同亮相；同月接入 Grok（2024-12 Grok 换成自研 Aurora）
- 2024-11-18 Mistral Le Chat 接入 FLUX Pro；11-21 FLUX.1 Tools（Fill / Depth / Canny / Redux）
- 2025-05-29 FLUX.1 Kontext（图文混合的上下文编辑）
- 2025-07-31 FLUX.1 Krea Dev
- 2025-09 Adobe Photoshop（beta）生成式填充可选 Kontext Pro
- 2025-11-25 FLUX.2（pro / flex / dev），[dev] 32B
- 2026-01-15 FLUX.2 [klein] 4B / 9B
- 2026-07-23 FLUX 3 发布并进入早期访问：图像、视频、音频统一模型
- 2026-08-04 FLUX 3 Video；08-20 视频 2K / 4K 超分
- 2026-09-23 FLUX 3 Action（与 mimic robotics 合作）
- 2026-10-15 FLUX 3 Image Klein，5.6B 开放权重

## 相关实体

- [[entities/black-forest-labs|Black Forest Labs]]
- [[entities/stable-diffusion|Stable Diffusion]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/grok|Grok]]（2024-08 至 12 月用 FLUX 出图）
- [[entities/mistral-ai|Mistral AI]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]（flow matching）
- [[concepts/lora|LoRA]]
- [[concepts/kv-cache|KV Cache]]（klein 9B KV 用 KV 缓存加速多参考图编辑）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "`FLUX.2 [dev]` is a 32B parameter flow matching transformer model capable of generating and editing (multiple) images." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（black-forest-labs/flux2 README）
- "FLUX.2 [klein] is our fastest model family — generating and editing (multiple) images in under a second without sacrificing quality." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（black-forest-labs/flux2 README）
- "FLUX 3 is our new multimodal foundation model. It jointly learns from images, videos, and audio within a unified architecture" — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（BFL FLUX 3 公告）
