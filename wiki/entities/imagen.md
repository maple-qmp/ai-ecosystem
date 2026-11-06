---
title: Imagen
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Imagen", "Imagen 3", "Imagen 4", "Google Imagen"]
org: "[[entities/google-deepmind|Google DeepMind]]"
released: "2022-05"
open_weights: false
competitors: ["[[entities/gpt-image]]", "[[entities/flux]]", "[[entities/stable-diffusion]]"]
depends_on: []
status: deprecated
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Imagen

## 描述

Google 已停用的文生图模型系列，最初由 Google Brain 开发（2023-04 并入 DeepMind）。2022-05 以论文形式公布，用 T5 编码提示词，再用级联[[concepts/diffusion-model|扩散模型]]从 64×64 逐级放大到 1024×1024，和同期的 [[entities/stable-diffusion|Stable Diffusion]] 一样依赖冻结的大型文本编码器。之后发布 Imagen 2（2023-12）、Imagen 3（2024-08）和 Imagen 4（2025-05-20 Google I/O，最高 2K）。Google 的图像生成主力后来转到 [[entities/gemini|Gemini]] 原生出图的 Nano Banana 系列（2025-08 起），Imagen 4 于 2026-06-15 宣布弃用、2026-08-17 在 Gemini API 关闭。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，图像生成，已停用）
- **上游依赖**：Google TPU（本库尚无页面）
- **竞争 / 替代**：[[entities/gpt-image|GPT Image]]、[[entities/flux|FLUX]]、[[entities/stable-diffusion|Stable Diffusion]]；后继是 Gemini 的 Nano Banana

## 时间线

- 2022-05 Imagen 论文（arXiv 2205.11487）
- 2023-12 Imagen 2（文字与 logo 生成）
- 2024-08 Imagen 3
- 2025-05-20 Google I/O：Imagen 4，与 [[entities/veo|Veo]] 3、Flow 同场
- 2025-08-14 Imagen 4 Ultra / Standard / Fast 在 Gemini API GA
- 2025-08 Nano Banana（Gemini 2.5 Flash Image）上线
- 2026-05-28 Nano Banana 2 与 Nano Banana Pro GA
- 2026-06-15 宣布 Imagen 4 弃用
- 2026-08-17 Imagen 4 在 Gemini API 关闭
- 2026-10-06 Nano Banana 2.1 GA

## 相关实体

- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gemini|Gemini]]
- [[entities/veo|Veo]]
- [[entities/gpt-image|GPT Image]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Imagen is a discontinued series of text-to-image models developed by Google DeepMind." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wikipedia）
- "Similar to Google's Imagen, this model uses a frozen CLIP ViT-L/14 text encoder to condition the model on text prompts." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（CompVis/stable-diffusion README，原文链接已去掉）
