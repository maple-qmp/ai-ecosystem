---
title: Grok
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Grok", "Grok 4", "Grok 4.5", "Grok Code Fast"]
org: "[[entities/xai|xAI（SpaceX Super Intelligence）]]"
released: "2023-11"
open_weights: false
competitors: ["[[entities/gpt]]", "[[entities/claude]]", "[[entities/gemini]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/frontier-closed-models-survey-2026-11]]"]
---

# Grok

## 描述

[[entities/xai|xAI]]（2026-10 起名为 SpaceX Super Intelligence）的模型家族，2023-11 随同名聊天机器人发布，深度集成在 X 社交网络中，也用于 Tesla 的 Optimus 机器人。Grok-1 曾开放权重，Grok 2.5（2025-08）以 source-available 许可放出、商用受可接受使用政策限制，此后的主力模型都闭源。Grok 3 起加入 Think 推理模式，Grok 4 有多智能体的 Heavy 版，另有专做 Agent 编码的 Grok Code Fast。Grok 4.5（2026-07）起与 [[entities/cursor|Cursor]] 共同开发，先在 Grok Build 和 Cursor 编辑器上线。Musk 2026 年在诉讼中承认 Grok 部分蒸馏自 OpenAI 模型。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源为主）
- **上游依赖**：xAI 自建的 Colossus 集群（[[entities/nvidia|NVIDIA]] GPU）
- **竞争 / 替代**：[[entities/gpt|GPT]]、[[entities/claude|Claude]]、[[entities/gemini|Gemini]]

## 时间线

- 2023-11 Grok-1 向 X Premium 用户预览
- 2024-03 Grok-1 开放权重；03-29 Grok-1.5（128K 上下文）
- 2024-08-14 Grok-2 / Grok-2 mini
- 2025-02-17 Grok 3，含 Think 模式；04 月开放 API
- 2025-07-09 Grok 4 与 Grok 4 Heavy
- 2025-08 Grok 2.5 以 source-available 许可放出；08-28 Grok Code Fast 1
- 2025-09 Grok 4 Fast
- 2025-11-17 Grok 4.1
- 2026-01-12 美国国防部宣布把 Grok 接入内部网络
- 2026-07-08 Grok 4.5，与 Cursor 共同开发，欧盟延后上线
- 2026-07-14 研究者披露 Grok Build 会上传用户整个代码仓库（含历史和密钥）
- 2026-08-12 Grok 4.6；09-21 Grok 4.7

## 相关实体

- [[entities/xai|xAI（SpaceX Super Intelligence）]]
- [[entities/cursor|Cursor]]
- [[entities/gpt|GPT]]
- [[entities/claude|Claude]]
- [[entities/gemini|Gemini]]

## 相关概念

- [[concepts/reasoning-model|推理模型]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Starting with Grok 4.5, the models are co-developed with incoming SpaceXSI subsidiary Cursor." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（Wikipedia）
