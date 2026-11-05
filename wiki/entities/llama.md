---
title: Llama
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Llama", "LLaMA", "Llama 2", "Llama 3", "Llama 4"]
org: "[[entities/meta-ai|Meta AI]]"
released: "2023-02"
open_weights: true
competitors: ["[[entities/qwen]]", "[[entities/deepseek-v]]", "[[entities/mistral-models]]"]
depends_on: ["[[entities/pytorch]]"]
status: deprecated
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/open-weight-flagships-survey-2026-11]]"]
---

# Llama

## 描述

[[entities/meta-ai|Meta]] 在 2023-02 到 2025-04 间发布的开放权重模型家族，共四代，是开源 LLM 生态的重要起点：大量社区微调（[[concepts/lora|LoRA]]）、[[entities/llama-cpp|llama.cpp]] 等本地部署工具，以及早期的 [[entities/qwen|Qwen]] 都建立在 Llama 之上。Llama 1 只给研究者，权重随即被泄露；Llama 2 起允许部分商用，但许可证附有月活门槛和可接受使用政策，FSF 认定其为非自由许可，也不满足 OSI 的开源 AI 定义。Llama 4（2025-04）改为 [[concepts/mixture-of-experts|MoE]] 与原生多模态，但因在 LMArena 上提交未发布的“实验聊天版”而引发争议，最大的 Behemoth 只预告未发布。2026-04 起 Meta 改用闭源的 [[entities/muse|Muse]] 驱动自家产品，Llama 不再更新。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，已停更）
- **上游依赖**：[[entities/pytorch|PyTorch]]
- **竞争 / 替代**：[[entities/qwen|Qwen]]、[[entities/deepseek-v|DeepSeek-V]]、[[entities/mistral-models|Mistral 模型]]；Meta 内部的继任者是 [[entities/muse|Muse]]

## 主要版本

- **LLaMA**（2023-02）：研究许可
- **Llama 2**（2023-07）：与微软合作，允许部分商用；含 Code Llama
- **Llama 3 / 3.1**（2024-04 / 07）：8B、70B、405B
- **Llama 4**（2025-04-05）：Scout 109B 总参数 / 17B 激活（16 专家，10M 上下文）、Maverick 400B / 17B（128 专家，1M 上下文）；知识截止 2024-08

## 时间线

- 2023-02-24 LLaMA 发布
- 2023-03-03 权重在 BitTorrent 泄露
- 2023-07-18 Llama 2
- 2024-04-18 Llama 3，同时推出 Meta AI 助手
- 2024-07-23 Llama 3.1（含 405B）
- 2024-11 允许美国政府和军方承包商使用
- 2025-01 FSF 认定 Llama 3.1 许可证为非自由软件许可
- 2025-04-05 Llama 4 Scout / Maverick
- 2026-04 被 Muse Spark 取代

## 相关实体

- [[entities/meta-ai|Meta AI]]
- [[entities/muse|Muse]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/qwen|Qwen]]
- [[entities/vllm|vLLM]]

## 相关概念

- [[concepts/lora|LoRA]]
- [[concepts/quantization|量化]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "In April 2026, Meta Superintelligence Labs released Muse Spark as a replacement for Llama powering chatbots on various Meta services." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（Wikipedia）
