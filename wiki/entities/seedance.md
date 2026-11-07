---
title: Seedance / 即梦
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Seedance", "Seedance 2.0", "Seedance 2.5", "即梦", "即梦 AI", "Jimeng", "Dreamina", "Seedream", "Seedream 5.0 Pro"]
org: "[[entities/bytedance|字节跳动]]"
released: "2025-06"
open_weights: false
competitors: ["[[entities/kling]]", "[[entities/veo]]", "[[entities/sora]]", "[[entities/flux]]", "[[entities/gpt-image]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-07
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/bytedance-doubao-survey-2026-11]]"]
---

# Seedance / 即梦

## 描述

[[entities/bytedance|字节跳动]] Seed 团队的视觉生成模型：Seedance 生成视频，Seedream 生成图像，两者都通过创作平台即梦（海外版 Dreamina，属 CapCut）、[[entities/doubao|豆包]] App 和火山引擎 API 提供，不开放权重。Seedance 1.0（2025-06）支持中英双语的文生视频和图生视频；2.0（2026-02）能生成带原生音频的多镜头视频，因画面逼真而走红，但也能生成酷似真人演员和知名 IP 的片段（如布拉德·皮特与汤姆·克鲁斯打斗），引来美国电影协会谴责、迪士尼 2026-02-13 的停止侵权函和美国参议员要求关停的公开信。字节回应会加强防护，并一度暂停海外发布。2026-07 的 Seedance 2.5 是音视频联合生成模型，单次 30 秒，最多支持 50 个多模态参考，可做局部编辑，长视频模式可延长到 3 分钟。图像侧，Seedream 4.0（2025-09）把文生图、编辑和多图组合统一到一个模型；截至 2026-11 官网列出的最新版是带推理的 Seedream 5.0 Pro。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，视频与图像生成）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/kling|可灵 Kling]]（国内直接对手）、[[entities/veo|Veo]] / Gemini Omni、[[entities/flux|FLUX 3]]、[[entities/sora|Sora]]（已停用）；图像侧对 [[entities/gpt-image|GPT Image]]、[[entities/flux|FLUX]]

## 时间线

- 2025-06 Seedance 1.0 技术报告，接入豆包与即梦
- 2025-06-11 FORCE 大会：Seedance 1.0 Pro
- 2025-09 Seedream 4.0 技术报告
- 2025-12-18 FORCE 大会：Seedance 1.5 Pro
- 2026-02 Seedance 2.0 上线（豆包调研记为 02-14 与 Seed 2.0 同日发布；但迪士尼 02-13 已发函，说明 2.0 此前已可用，确切日期待核实）
- 2026-02-13 迪士尼发停止侵权函；派拉蒙 Skydance 指其“公然侵权”
- 2026-02-16 字节回应将加强知识产权防护
- 2026-03-16 美国参议员 Blackburn、Welch 致信字节 CEO 梁汝波要求关停 Seedance
- 2026-03 中旬暂停海外发布（The Information 报道转述）；03-26 报道称已悄然全球上线
- 2026-07 Seedance 2.5：30 秒、50 个参考、局部编辑、3 分钟长视频 beta
- 2026-11 官网列出 Seedream 5.0 Pro（发布日期未标）

## 相关实体

- [[entities/bytedance|字节跳动]]
- [[entities/doubao|豆包]]
- [[entities/kling|可灵 Kling]]
- [[entities/kuaishou|快手]]
- [[entities/runway|Runway]]（应用侧竞品）

## 相关概念

- [[concepts/diffusion-model|扩散模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "On February 13, 2026, The Walt Disney Company sent ByteDance a cease and desist letter alleging that the model had been trained with Disney works without any compensation." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Wikipedia）
- "Seedance 2.5 is a next-generation audio-video joint generation model, built for 30-second storytelling with precise reference control and powerful editing capabilities." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（ByteDance Seed 官网）
