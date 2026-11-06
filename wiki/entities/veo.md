---
title: Veo
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Veo", "Veo 3", "Veo 3.1", "Google Veo", "Google Flow"]
org: "[[entities/google-deepmind|Google DeepMind]]"
released: "2024-05"
open_weights: false
competitors: ["[[entities/sora]]", "[[entities/kling]]", "[[entities/seedance]]", "[[entities/flux]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Veo

## 描述

[[entities/google-deepmind|Google DeepMind]] 的视频生成模型家族，通过 Gemini API、Vertex AI、Gemini App 和 AI 电影制作工具 Flow（2026 改名 Google Flow）提供，单段最长 8 秒。首代 2024-05 在 Google I/O 公布，Veo 2（2024-12）支持 4K。Veo 3（2025-05）第一次原生生成对白、音效和环境声，Hassabis 称视频生成从此告别“默片时代”，原生音频随后成为业界标配。Veo 3.1（2025-10-15）改进了音频、提示词遵循和镜头间角色一致性；2026-03-31 推出最便宜的 Veo 3.1 Lite 预览，Veo 2 / 3.0 于 2026-06-30 在 Gemini API 关闭。截至 2026-11，DeepMind 官网仍以 Veo 3.1 为最新版本，没有 Veo 4。Google 新的视频能力改由统一的 Gemini Omni 提供：2026-06 公测，08-27 GA，11-05 的 Omni 1.2 Flash 可生成 15 秒视频并支持对话式编辑，详见 [[entities/gemini|Gemini]]。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，视频生成）
- **上游依赖**：Google TPU（本库尚无页面）
- **竞争 / 替代**：[[entities/sora|Sora]]（已停用）、[[entities/kling|可灵 Kling]]、[[entities/seedance|Seedance / 即梦]]、[[entities/flux|FLUX 3 Video]]；Google 内部的后继是 Gemini Omni

## 时间线

- 2024-05-14 Google I/O：首代 Veo（1080p）
- 2024-12-16 Veo 2（4K），经 VideoFX 限量预览；2025-04 进 Gemini App
- 2025-05-20 Google I/O：Veo 3（原生音频）、Flow 工具
- 2025-07-17 Veo 3 预览进 Gemini API；09-09 Veo 3 / 3 Fast GA
- 2025-10-15 Veo 3.1 / 3.1 Fast 预览，进入 Gemini API、Vertex AI、Gemini App、Flow；Flow 累计生成超 2.75 亿条视频
- 2026-03-31 Veo 3.1 Lite 预览
- 2026-05-19 Google I/O：未发布 Veo 4；Flow 改名 Google Flow，推出 Google Flow Music
- 2026-06-15 宣布 Veo 2.0 / 3.0 弃用，06-30 关闭；同日 Gemini Omni Flash 公测
- 2026-08-27 Gemini Omni Flash GA；2026-11-05 Gemini Omni 1.2 Flash GA

## 相关实体

- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gemini|Gemini]]
- [[entities/imagen|Imagen]]
- [[entities/sora|Sora]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Veo 3.1 is a new era for video generation. It delivers exceptional results in text-to-video, image-to-video, text-to-audio+video generation, and realistic physics." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Google DeepMind Veo 页）
