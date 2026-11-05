---
title: Cohere Embed
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Cohere Embed", "Embed 4", "embed-v4.0", "Embed Multimodal v4"]
org: "[[entities/cohere|Cohere]]"
released: "2025-04"
open_weights: false
competitors: ["[[entities/openai-embeddings]]", "[[entities/voyage-embeddings]]", "[[entities/qwen3-embedding]]", "[[entities/bge]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Cohere Embed

## 描述

[[entities/cohere|Cohere]] 面向企业检索的[[concepts/embedding|嵌入]]模型家族。当前版本 Embed 4（2025-04）能把同一请求里的图像和文本编成一个统一的嵌入，上下文 128K，输出 256 / 512 / 1024 / 1536 四种维度（Matryoshka 式可截短），上线时同时进入 Cohere 平台、AWS SageMaker 和 Azure AI Foundry，2025-10 上架 Amazon Bedrock，价格约 $0.12 / 百万输入 token（二手）。截至 2026-11 未见 Embed 5 或新的 Cohere 嵌入模型。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，多模态嵌入）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/voyage-embeddings|Voyage]]、[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/bge|BGE]]

## 时间线

- 2025-04 Embed 4（Embed Multimodal v4）
- 2025-10 上架 Amazon Bedrock

## 相关实体

- [[entities/cohere|Cohere]]
- [[entities/voyage-embeddings|Voyage]]
- [[entities/openai-embeddings|OpenAI text-embedding]]

## 相关概念

- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

（本次只读到 Cohere changelog 的搜索摘要，暂无逐字摘录；见 [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]）
