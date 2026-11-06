---
title: Sora
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Sora", "Sora 2", "sora-2", "OpenAI Sora"]
org: "[[entities/openai|OpenAI]]"
released: "2024-12"
open_weights: false
competitors: ["[[entities/veo]]", "[[entities/kling]]", "[[entities/seedance]]"]
depends_on: []
status: deprecated
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]"]
---

# Sora

## 描述

[[entities/openai|OpenAI]] 已停用的视频生成模型和社交应用。OpenAI 称它是扩散 Transformer：在潜空间里对 3D“补丁”去噪，技术上改编自 DALL·E 3。2024-02-15 以研究预览公布，2024-12-09 向 ChatGPT 付费用户开放。2025-09-30 的 Sora 2 加入同步声音，并配了一个类似 TikTok 的社交应用；10 月以 sora-2 进入 API。2025-12 迪士尼宣布投资 OpenAI 10 亿美元，并授权在 Sora 2 中使用 200 多个角色。2026-03-24 OpenAI 宣布整体退出：应用 2026-04-26 关闭，Videos API 和全部 Sora 2 模型 2026-09-24 下线，官方没有给出替代方案。OpenAI 没有说明原因；报道指向算力和成本，用户峰值约 100 万、后降到 50 万以下，每天运营成本约 100 万美元。在 Artificial Analysis 榜上，Sora 2 Pro 排在 [[entities/seedance|Seedance 2.0]]、[[entities/kling|Kling 3.0]] 等之后。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，视频生成，已停用）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/veo|Veo]]、[[entities/kling|可灵 Kling]]、[[entities/seedance|Seedance / 即梦]]

## 时间线

- 2024-02-15 公布 Sora（研究预览）
- 2024-12-09 向 ChatGPT Plus / Pro 用户开放（美国、加拿大）
- 2025-09-30 Sora 2 与 Sora iOS 应用（Android 两个月后）
- 2025-10-06 DevDay：sora-2 进入 API
- 2025-12-11 迪士尼宣布投资 10 亿美元，授权 Sora 2 使用其角色
- 2026-03-12 Sora API 扩展：角色参考、最长 20 秒、sora-2-pro 1080p
- 2026-03-24 宣布停止 Sora 应用与 API，迪士尼合作随之结束
- 2026-04-26 Sora 应用关闭
- 2026-09-24 Videos API 与 Sora 2 模型下线

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt-image|GPT Image]]
- [[entities/veo|Veo]]
- [[entities/kling|可灵 Kling]]
- [[entities/seedance|Seedance / 即梦]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Sora is a discontinued text-to-video model and social media app developed by OpenAI." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wikipedia）
- "According to OpenAI, Sora is a diffusion transformer, a denoising latent diffusion model with one transformer as its denoiser." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wikipedia）
- "On March 24th, 2026, we notified developers using the Videos API and Sora 2 video generation model aliases and snapshots of their deprecation and removal from the API on September 24, 2026." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（OpenAI 弃用表）
