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
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Imagen

## 描述

Google 的文生图[[concepts/diffusion-model|扩散模型]]家族，2022-05 以论文形式公布，和同期的 [[entities/stable-diffusion|Stable Diffusion]] 一样用冻结的大型文本编码器做条件。Imagen 4 于 2025-05 Google I/O 与 Veo 3 和 Flow 一同发布，通过 Gemini API 和 Vertex AI 提供。之后 Google 的图像生成主力转到 [[entities/gemini|Gemini]] 原生出图的 Nano Banana 系列（2025-08 起）。2026-06 Gemini API 宣布 Imagen 4 弃用，2026-08-17 关闭，所以本页标为 deprecated。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，图像生成，已弃用）
- **上游依赖**：Google TPU（本库尚无页面）
- **竞争 / 替代**：[[entities/gpt-image|GPT Image]]、[[entities/flux|FLUX]]、[[entities/stable-diffusion|Stable Diffusion]]；后继是 Gemini 的 Nano Banana

## 时间线

- 2022-05 Imagen 论文（arXiv 2205.11487）
- 2025-05 Google I/O：Imagen 4，与 [[entities/veo|Veo]] 3、Flow 同场
- 2025-08 Nano Banana（Gemini 2.5 Flash Image）上线，与 Imagen 4 并列
- 2026-06 Gemini API 宣布 Imagen 4（generate / ultra / fast）弃用
- 2026-08-17 Imagen 4 在 Gemini API 关闭

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

- "Similar to Google's Imagen, this model uses a frozen CLIP ViT-L/14 text encoder to condition the model on text prompts." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（CompVis/stable-diffusion README，原文链接已去掉）
