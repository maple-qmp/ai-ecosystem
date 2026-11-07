---
title: 可灵 Kling
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["可灵", "Kling", "Kling AI", "可灵 AI", "Kling 3.0", "Kling 4.0"]
org: "[[entities/kuaishou|快手]]"
released: "2024-06"
open_weights: false
competitors: ["[[entities/seedance]]", "[[entities/veo]]", "[[entities/sora]]", "[[entities/flux]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-07
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# 可灵 Kling

## 描述

[[entities/kuaishou|快手]]自研的视频生成模型家族。2024-06 首先在快手旗下的剪辑 App 快影里开放测试，同年 7 月推出全球网页版，是最早面向公众开放的中国视频模型之一。架构是扩散 Transformer（DiT），配合自研的 3D VAE 做时空联合压缩。它迭代很快：1.6（2024-12）、2.0（2025-04）、2.1（2025-05）、2.5 Turbo（2025-09）、3.0（2026-02，15 秒，带原生音频与多语言对白），以及 4.0（2026-10-15）。4.0 单次最长 30 秒，Omni Reference 最多组合 15 个参考素材和 10 张关键帧，并支持 4K 10-bit HDR 和双声道音频。可灵也是商业化最快的视频模型之一：据报道 2026 Q1 年化收入约 5 亿美元；快手 2026-05 起筹划将其分拆独立、赴港上市，2026-07 一轮融资估值约 180 亿美元（二手）。因遵守中国审查规定，它不生成政治等敏感内容。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，视频生成）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/seedance|Seedance / 即梦]]（国内直接对手）、[[entities/veo|Veo]] / Gemini Omni、[[entities/flux|FLUX 3 Video]]、[[entities/sora|Sora]]（已停用）、[[entities/minimax|MiniMax]] 的海螺视频

## 时间线

- 2024-06 在快影 App 中开放测试
- 2024-07 全球网页版
- 2024-12 Kling 1.6
- 2025-04 Kling 2.0
- 2025-05 Kling 2.1（720p Standard / 1080p Professional）
- 2025-09-23 Kling 2.5 Turbo（单一来源）
- 2026-02-05 Kling 3.0：15 秒、原生音频
- 2026 Q1 年化收入约 5 亿美元（二手）
- 2026-05 快手提出分拆可灵、目标港股上市（二手）
- 2026-07 融资估值约 180 亿美元（二手）
- 2026-09-28 Kling 4.0 Flash 向年费用户开放预览
- 2026-10-15 Kling 4.0 正式上线：30 秒、15 个参考素材 + 10 张关键帧、4K HDR

## 相关实体

- [[entities/kuaishou|快手]]
- [[entities/seedance|Seedance / 即梦]]
- [[entities/veo|Veo]]
- [[entities/sora|Sora]]
- [[entities/minimax|MiniMax]]
- [[entities/runway|Runway]]（应用侧竞品）

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Kuaishou Technology ... today announced that Kling 4.0, the new-generation video generation model of Kling AI, officially launched on October 15." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（快手新闻稿）
- "native generation of up to 30 seconds in a single pass, supporting long takes and continuous storytelling with a director's mindset throughout; and Omni Reference, which supports combinations of up to 15 reference assets and up to 10 keyframe inputs" — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（快手新闻稿）
