---
title: Gemini
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Gemini", "Google Gemini", "Gemini Pro", "Gemini Flash", "Gemini 4 Argon", "Nano Banana"]
org: "[[entities/google-deepmind|Google DeepMind]]"
released: "2023-12"
open_weights: false
competitors: ["[[entities/claude]]", "[[entities/gpt]]", "[[entities/grok]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/frontier-closed-models-survey-2026-11]]"]
---

# Gemini

## 描述

[[entities/google-deepmind|Google DeepMind]] 的原生多模态闭源模型家族，2023-12-06 发布，接替 PaLM 2，在 Google TPU 上训练和推理。档位有 Pro（旗舰）、Flash（性价比）、Flash-Lite（最便宜）和 Deep Think 深度推理模式；同一品牌下还有 Nano Banana（图像生成与编辑）、Live（实时语音）、TTS、Omni（视频生成）、Embedding 和 Robotics ER 等分支。1.5 代起改为 [[concepts/mixture-of-experts|MoE]] 并支持 1M 上下文；2.0 之后没有再发表技术白皮书。当前旗舰 Gemini 4 Argon 2026-10-13 正式开放，Flash 主力是 Gemini 3.8 Flash。开放权重的小模型另以 Gemma 发布（2024-02 起，最新 Gemma 4）。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源）
- **上游依赖**：Google TPU（本库尚无页面）
- **竞争 / 替代**：[[entities/claude|Claude]]、[[entities/gpt|GPT]]、[[entities/grok|Grok]]

## 当前阵容（2026-11，Gemini API 模型页）

- **Gemini 4 Argon**（`gemini-4-argon`）：旗舰推理模型，1M 上下文，长输出可达 1M token
- **Gemini 3.8 Flash**：长时间运行的编码、Agent 与企业工作流；3.6 Flash、3.5 Flash-Lite、3.1 Flash-Lite 仍在
- **Nano Banana 2.1 / 2 / Pro**：图像生成与编辑
- **Gemini Omni Flash**：视频生成与编辑，带原生音频
- Gemini 2.5 Pro / Flash 已弃用，2026-12-01 起请求自动转发到 3.8 Flash 和 3.5 Flash-Lite

## 时间线

- 2023-05-10 Google I/O 预告
- 2023-12-06 Gemini 1.0（Ultra / Pro / Nano）
- 2024-02 Gemini 1.5（MoE、1M 上下文）；Bard 改名 Gemini；开放权重的 Gemma
- 2024-05-14 1.5 Flash；1.5 Pro 上下文扩到 2M
- 2024-12-11 Gemini 2.0 Flash 实验版
- 2025-03-25 Gemini 2.5 Pro 实验版，登顶 LMArena
- 2025-06 2.5 Pro / Flash 稳定版；Gemini CLI 开源
- 2025-08-26 Nano Banana（2.5 Flash Image）
- 2025-11-18 Gemini 3 Pro 预览
- 2025-12-17 Gemini 3 Flash 预览
- 2026-02-19 Gemini 3.1 Pro 预览
- 2026-04-02 Gemma 4
- 2026-05-19 3.5 Flash GA，之后 3.6（07）、3.7（08）、3.8 Flash（09-02）
- 2026-09-30 Gemini 4 Argon 发布，先给受信网络防御方（二手报道）
- 2026-10-13 Gemini 4 Argon GA
- 2026-11-02 2.5 Pro / Flash 弃用

## 相关实体

- [[entities/google-deepmind|Google DeepMind]]
- [[entities/google-adk|Google ADK]]
- [[entities/claude|Claude]]
- [[entities/gpt|GPT]]
- [[entities/grok|Grok]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Our flagship reasoning model with a shared 1M context window and long decodes up to 1M tokens." — [[sources/frontier-closed-models-survey-2026-11|前沿闭源模型调研]]（Gemini API 模型页对 Gemini 4 Argon 的描述）
