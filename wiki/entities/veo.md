---
title: Veo
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Veo", "Veo 3", "Veo 3.1", "Google Veo"]
org: "[[entities/google-deepmind|Google DeepMind]]"
released: "2024-05"
open_weights: false
competitors: ["[[entities/sora]]", "[[entities/kling]]", "[[entities/seedance]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Veo

## 描述

[[entities/google-deepmind|Google DeepMind]] 的视频生成模型家族，通过 Gemini API、Vertex AI、Gemini App 和 AI 电影制作工具 Flow 提供。Veo 3（2025-05-20 Google I/O）第一次原生生成对白、音效和环境声，此后原生音频成为视频模型的标配。Veo 3.1（2025-10-15）改进了音频、提示词遵循和镜头间角色一致性；2026-04 加了最便宜的 Veo 3.1 Lite 预览，Veo 2 / 3.0 于 2026-06-30 在 Gemini API 关闭。截至 2026-11 Veo 3.1 仍是最新版本：2026-05 的 Google I/O 没有发 Veo 4，而是推出统一的 Gemini Omni（Omni Flash 可生成 3～10 秒 720p 视频，见 [[entities/gemini|Gemini]]）。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，视频生成）
- **上游依赖**：Google TPU（本库尚无页面）
- **竞争 / 替代**：[[entities/sora|Sora]]（已停止）、[[entities/kling|可灵 Kling]]、[[entities/seedance|Seedance / 即梦]]；Google 内部有 Gemini Omni

## 时间线

- 2024-05-14 Google I/O：首代 Veo（1080p）
- 2024-12-16 Veo 2（4K），经 VideoFX 限量预览
- 2025-05-20 Google I/O：Veo 3（原生音频）、Flow 工具
- 2025-10-15 Veo 3.1，进入 Gemini API、Vertex AI、Gemini App、Flow；Flow 累计生成超 2.75 亿条视频
- 2026-04-01 Veo 3.1 Lite 预览
- 2026-05-19 Google I/O 未发布 Veo 4，改推 Gemini Omni
- 2026-06-30 Veo 2.0 / 3.0 在 Gemini API 关闭；同日 Gemini Omni Flash 公测

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

（本次未能直接读取 Google 官方页面，暂无逐字摘录；事实来自 Gemini API changelog 搜索摘要与二手报道，见 [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]）
