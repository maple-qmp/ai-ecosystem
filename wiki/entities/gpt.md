---
title: GPT
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["GPT", "GPT 系列", "ChatGPT 模型", "GPT-4o", "GPT-5", "GPT-5.5", "GPT-6 Astra", "o1", "o3"]
org: "[[entities/openai|OpenAI]]"
released: "2018"
open_weights: false
competitors: ["[[entities/claude]]", "[[entities/gemini]]", "[[entities/grok]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/openai-developers-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]", "[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# GPT

## 描述

[[entities/openai|OpenAI]] 的闭源模型家族，从 2018 年的 GPT-1 发展到 2026-09 的 GPT-6 Astra，驱动 ChatGPT、Codex 和 OpenAI API。2024-09 起另有 o 系列[[concepts/reasoning-model|推理模型]]；GPT-5（2025-08）把快速模型、推理模型和实时路由器合成一个系统，o 系列从此并入主线。GPT-5.6（2026-07）起按档位起名：Sol 是主力，Terra 偏快速与 computer use，Luna 是低价大批量档；GPT-6 起旗舰叫 Astra。当前旗舰上下文 1.05M、最大输出 128K。开放权重的只有 [[entities/gpt-oss|gpt-oss]]（2025-08）。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/claude|Claude]]、[[entities/gemini|Gemini]]、[[entities/grok|Grok]]

## 当前阵容（2026-11，官方模型页）

- **GPT-6 Astra**（`gpt-6-astra`）：旗舰，$10 / $50 每百万 token
- **GPT-6.1 Sol**：接近 Astra 的能力，$2 / $10
- **GPT-6.1 Terra**：快速，偏视觉推理、computer use 和写作，$1 / $5
- **GPT-6 Luna**：低价大批量，$0.10 / $0.50
- 专用：GPT-5.6 Cyber（授权安全研究）、GPT-Rosalind（生命科学，限准入组织）、GPT-Image 2.x、GPT-Realtime 2.x、GPT-Live 1、GPT-Transcribe

## 时间线

- 2018-06 GPT-1
- 2019-02 GPT-2（1.5B），分阶段发布
- 2020-05 GPT-3（175B）
- 2022-11-30 ChatGPT（GPT-3.5）
- 2023-03-14 GPT-4
- 2024-05-13 GPT-4o（文本、图像、音频）
- 2024-09-12 o1-preview，第一代推理模型
- 2025-02-27 GPT-4.5 研究预览（代号 Orion）
- 2025-04 GPT-4.1；o3 与 o4-mini
- 2025-08-05 开放权重的 [[entities/gpt-oss|gpt-oss]]
- 2025-08-07 GPT-5（含 mini / nano），自动路由；ChatGPT 下架 GPT-4o 引发抗议后为付费用户恢复
- 2025-11-13 GPT-5.1；2025-12-11 GPT-5.2
- 2026-02-13 ChatGPT 正式下线 GPT-4o
- 2026-03-05 GPT-5.4
- 2026-04-23 GPT-5.5 与 GPT-5.5 Pro
- 2026-07-09 GPT-5.6 家族（Sol / Terra / Luna）
- 2026-08-07 GPT-5.6 Cyber，需单独审批
- 2026-08-26 o3 从 ChatGPT 退役
- 2026-09-03 GPT-6 Astra，先给审批用户，次日公开
- 2026-09-22 GPT-6 Sol / Luna；09-29 GPT-6.1 Sol；10-26 GPT-6.1 Terra

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/tiktoken|tiktoken]]
- [[entities/gpt-image|GPT Image]]、[[entities/sora|Sora]]、[[entities/whisper|Whisper]]（图像、视频、语音线）
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/claude|Claude]]
- [[entities/gemini|Gemini]]
- [[entities/grok|Grok]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/scaling-laws|规模定律]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/harmony-response-format|Harmony 响应格式]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Our most capable model for the most demanding work." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（OpenAI 模型页对 GPT-6 Astra 的描述）
- "GPT-5 is a system that contains a fast, high-throughput model, a deeper reasoning model, and a real-time router that decides which model to use based on conversation type, complexity, tool needs, and explicit user intent." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（Wikipedia）
