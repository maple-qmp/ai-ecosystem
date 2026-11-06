---
title: OpenAI text-embedding
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["OpenAI text-embedding", "text-embedding-3-large", "text-embedding-3-small", "text-embedding-ada-002", "OpenAI Embeddings"]
org: "[[entities/openai|OpenAI]]"
released: "2024-01"
open_weights: false
competitors: ["[[entities/qwen3-embedding]]", "[[entities/bge]]", "[[entities/voyage-embeddings]]", "[[entities/cohere-embed]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# OpenAI text-embedding

## 描述

[[entities/openai|OpenAI]] 的文本[[concepts/embedding|嵌入]]模型，通过 Embeddings API 提供，是 [[concepts/rag|RAG]] 和[[concepts/vector-database|向量数据库]]教程里最常见的默认选项。2024-01-25 发布接替 text-embedding-ada-002 的 text-embedding-3-small 和 text-embedding-3-large：large 最高 3072 维，两者都可以按需截短维度。截至 2026-11，OpenAI 官方模型页列出的嵌入模型仍只有 text-embedding-3-large、3-small 和 ada-002，没有新一代；3-large 约 $0.13 / 百万 token（二手）。在多语言榜单上，开放权重的 [[entities/qwen3-embedding|Qwen3-Embedding]] 和专做嵌入的 [[entities/voyage-embeddings|Voyage]]、[[entities/cohere-embed|Cohere Embed]] 都已追平或超过它；它也只支持文本，而对手 2026 年的主线是多模态嵌入。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，文本嵌入）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/bge|BGE]]、[[entities/voyage-embeddings|Voyage]]、[[entities/cohere-embed|Cohere Embed]]、Gemini Embedding（见 [[entities/gemini|Gemini]]）

## 时间线

- 2024-01-25 text-embedding-3-small / 3-large（最高 3072 维，可截短），接替 ada-002
- 2026-11 官方模型页仍以 3-large 为“最强嵌入模型”，无新一代

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/qwen3-embedding|Qwen3-Embedding]]
- [[entities/cohere-embed|Cohere Embed]]
- [[entities/voyage-embeddings|Voyage]]

## 相关概念

- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "text-embedding-3-large Most capable embedding model" — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（OpenAI 官方模型页）
