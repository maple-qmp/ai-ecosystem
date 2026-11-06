---
title: Voyage
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Voyage", "Voyage AI 嵌入模型", "voyage-4", "voyage-4-large", "voyage-4-nano", "voyage-multimodal-3.5"]
org: "[[entities/voyage-ai|Voyage AI]]"
released: ""
open_weights: false
competitors: ["[[entities/openai-embeddings]]", "[[entities/cohere-embed]]", "[[entities/qwen3-embedding]]", "[[entities/bge]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Voyage

## 描述

[[entities/voyage-ai|Voyage AI]] 的[[concepts/embedding|嵌入]]与重排模型家族。2025-02 Voyage AI 被 MongoDB 收购，模型随后并入 MongoDB Atlas 的自动嵌入和 Vector Search。此前已有 voyage-3、voyage-3-large、voyage-3.5 等版本。2026-01-15 发布的 Voyage 4 系列有五个模型：通用的 voyage-4、精度最高的 voyage-4-large、低价低延迟的 voyage-4-lite、供本地开发且开放权重的 voyage-4-nano，以及多模态的 voyage-multimodal-3.5。其中 voyage-4-large 用了 MoE 架构（见[[concepts/mixture-of-experts|混合专家（MoE）]]）。MongoDB 称它在 RTEB 检索榜排第一（厂商说法）。它代表了“嵌入模型并入数据库”的路线，见[[concepts/vector-database|向量数据库]]。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源为主，nano 开放权重；嵌入与重排）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/cohere-embed|Cohere Embed]]、[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/bge|BGE]]、Gemini Embedding（见 [[entities/gemini|Gemini]]）

## 时间线

- 2025-02-24 MongoDB 宣布收购 Voyage AI
- 2026-01-15 Voyage 4 系列 GA（voyage-4 / large / lite / nano、voyage-multimodal-3.5），接入 Atlas

## 相关实体

- [[entities/voyage-ai|Voyage AI]]
- [[entities/cohere-embed|Cohere Embed]]
- [[entities/openai-embeddings|OpenAI text-embedding]]

## 相关概念

- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "NEW YORK—February 24, 2025—MongoDB, Inc. (NASDAQ: MDB), the leading database for modern applications, today announced it has acquired Voyage AI, a pioneer in state-of-the-art embedding and reranking models that power next-generation AI applications." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（MongoDB 新闻稿）
