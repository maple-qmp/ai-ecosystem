---
title: Muse
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Muse", "Meta Muse", "Muse Spark", "Muse Spark Open"]
org: "[[entities/meta-ai|Meta AI]]"
released: "2026-04"
open_weights: false
competitors: ["[[entities/gpt]]", "[[entities/gemini]]", "[[entities/qwen]]"]
depends_on: ["[[entities/pytorch]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/open-weight-flagships-survey-2026-11]]"]
---

# Muse

## 描述

Meta Superintelligence Labs 的模型家族，2026-04 发布的 Muse Spark 取代 [[entities/llama|Llama]]，驱动 Meta 各产品里的聊天机器人。二手报道称 Muse Spark 是 Meta 第一个不开放权重的前沿模型，只通过应用和 API 提供。2026-10 Meta 又以 “Muse Spark Open” 的名义放出一个 816B 总参数、42B 激活的 [[concepts/mixture-of-experts|MoE]] 开放权重版，使用自定义的 Muse Model License，并上架 Hugging Face、SageMaker、Google Cloud Model Garden 和 Microsoft Foundry。开放版的名称、版本号和参数各报道说法不一，尚未用一手来源核对，所以本页 `open_weights` 按主力模型记为 false。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（主力闭源，另有开放权重版）
- **上游依赖**：[[entities/pytorch|PyTorch]]
- **竞争 / 替代**：[[entities/gpt|GPT]]、[[entities/gemini|Gemini]]；开放权重版对标 [[entities/qwen|Qwen]]、[[entities/deepseek-v|DeepSeek-V]]

## 时间线

- 2026-04 Muse Spark 发布（二手报道为 04-08），取代 Llama
- 2026-10 Muse Spark Open 开放权重（二手报道，待核实）

## 相关实体

- [[entities/meta-ai|Meta AI]]
- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "In April 2026, Meta Superintelligence Labs released Muse Spark as a replacement for Llama powering chatbots on various Meta services." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（Wikipedia）
