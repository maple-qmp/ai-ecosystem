---
title: Seedance / 即梦
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Seedance", "Seedance 2.0", "即梦", "即梦 AI", "Jimeng", "Dreamina", "Seedream"]
org: "[[entities/bytedance|字节跳动]]"
released: "2025-06"
open_weights: false
competitors: ["[[entities/kling]]", "[[entities/veo]]", "[[entities/sora]]", "[[entities/gpt-image]]", "[[entities/flux]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/bytedance-doubao-survey-2026-11]]"]
---

# Seedance / 即梦

## 描述

[[entities/bytedance|字节跳动]] Seed 团队的视觉生成模型：Seedance 做视频，Seedream 做图像，两者都通过创作平台即梦（海外版 Dreamina，属 CapCut）、[[entities/doubao|豆包]] App 和火山引擎 API 提供，不开放权重。Seedance 1.0（2025-06）支持中英双语的文生视频和图生视频，技术报告称在 NVIDIA L20 上 41.4 秒生成 5 秒 1080p 视频；之后在火山引擎 FORCE 大会上发布 1.0 Pro、1.5 Pro 和 2.0。Seedance 2.0（2026-02-14）能在 60 秒内生成带原生音频的多镜头视频，但因能生成酷似真人演员和知名 IP 的片段，2026-03 收到迪士尼和派拉蒙旗下 Skydance 的停止侵权函，字节一度暂停海外发布并加防护。Seedream 4.0（2025-09）把文生图、图像编辑和多图组合统一到一个模型里，原生输出 1K～4K。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，视频与图像生成）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/kling|可灵 Kling]]（国内直接对手）、[[entities/veo|Veo]]、[[entities/sora|Sora]]（已停止）；图像侧对 [[entities/gpt-image|GPT Image]]、[[entities/flux|FLUX]]

## 时间线

- 2025-06 Seedance 1.0 技术报告，接入豆包与即梦
- 2025-06-11 FORCE 大会：Seedance 1.0 Pro
- 2025-09 Seedream 4.0 技术报告
- 2025-12-18 FORCE 大会：Seedance 1.5 Pro
- 2026-02-14 Seedance 2.0（与 Seed 2.0 同日）
- 2026-03 迪士尼、Skydance 发停止侵权函；3 月中旬暂停海外发布（The Information 报道转述）
- 2026-03-26 报道称已悄然全球上线（范围未核实）

## 相关实体

- [[entities/bytedance|字节跳动]]
- [[entities/doubao|豆包]]
- [[entities/kling|可灵 Kling]]
- [[entities/kuaishou|快手]]

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

（本次未能直接读取 arXiv 与字节官方页面原文，暂无逐字摘录；事实来自搜索摘要与二手报道，见 [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]）
