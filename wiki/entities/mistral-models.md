---
title: Mistral 模型
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Mistral 模型", "Mistral models", "Mixtral", "Mistral Large", "Mistral Large 4", "Magistral", "Ministral"]
org: "[[entities/mistral-ai|Mistral AI]]"
released: "2023-09"
open_weights: true
competitors: ["[[entities/llama]]", "[[entities/qwen]]", "[[entities/deepseek-v]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/open-weight-flagships-survey-2026-11]]"]
---

# Mistral 模型

## 描述

[[entities/mistral-ai|Mistral AI]] 的模型家族，开放权重与商业 API 并行。早期以小而强的 Mistral 7B 和 Mixtral 8x7B（[[concepts/mixture-of-experts|MoE]]）出名；之后形成 Small / Medium / Large 三档，加上推理模型 Magistral、端侧小模型 Ministral，以及语音（Voxtral）、OCR、形式化证明（Leanstral）、安全分类（Shieldstral）、时间序列（Timestral）等专用模型。Mistral Large 3（2025-12）是 675B 总参数 / 41B 激活的 MoE；Mistral Large 4（2026 秋）扩到 1T 总参数 / 49B 激活，原生多模态，支持 160 多种语言（含全部欧盟官方语言），权重自带 DSpark [[concepts/speculative-decoding|投机解码]]草稿头。早期模型多为 Apache 2.0，Large 4 改用自定义的 Mistral Ecosystem Open-Weight License。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重为主）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/deepseek-v|DeepSeek-V]]

## 时间线

- 2023-09 Mistral 7B
- 2023-12 Mixtral 8x7B
- 2025-03-17 Mistral Small 3.1
- 2025-05-07 Mistral Medium 3
- 2025-06-10 Magistral Small（开放）/ Medium，第一代推理模型
- 2025-12-02 Mistral Large 3 与 Ministral 3（3B / 7B / 14B）
- 2026-03 Mistral Medium 3.5（128B）
- 2026-07 Leanstral 1.5、Shieldstral；Medium 3.5 进 Microsoft Foundry
- 2026-09-30 Mistral Large 4 的 Hugging Face 仓库创建；Wikipedia 记的发布日是 10-29

## 相关实体

- [[entities/mistral-ai|Mistral AI]]
- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]
- [[entities/vllm|vLLM]]
- [[entities/llama-cpp|llama.cpp]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/speculative-decoding|投机解码]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Mistral Large 4 is our largest and most capable model to date: a 1 trillion-parameter natively multimodal Mixture-of-Experts model with 49 billion active parameters per token (52 billion including embeddings and output layers), trained from scratch on 3,800 NVIDIA Grace Blackwell GPUs in Mistral's own datacenters in Europe." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（Mistral Large 4 模型卡）
- "This model is licensed under the [Mistral Ecosystem Open-Weight License]" — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（Mistral Large 4 模型卡）
