---
title: Cohere Embed
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Cohere Embed", "Embed 4", "Embed 5", "embed-v4.0", "embed-v5.0-pro", "embed-v5.0-fast", "Embed Multimodal v4", "Cohere Rerank"]
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
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# Cohere Embed

## 描述

[[entities/cohere|Cohere]] 面向企业检索的[[concepts/embedding|嵌入]]模型家族，与 Rerank 重排模型配套。Embed 4（2025-04-15）能把同一请求里的图像和文本编成统一的嵌入，上下文 128K，输出 256 / 512 / 1024 / 1536 四种维度（Matryoshka 式可截短），上线时进入 Cohere 平台、AWS SageMaker 和 Azure AI Foundry，2025-10 上架 Amazon Bedrock。Embed 5（2026-09-30）分 embed-v5.0-pro（离线建索引、质量优先）和 embed-v5.0-fast（交互检索、Agent 循环）两档，两档共用同一向量空间，所以可以用 Pro 建索引、用 Fast 编码查询；它接受文本、图像和图文混合输入（如 PDF 页面），官方称在视觉内容丰富的文档和金融等企业数据上明显强于 Embed 4。配套的 Rerank 5 于 2026-10-21 发布，两者 2026-11-04 上架 OpenRouter，也可以通过 Microsoft Foundry 和 Cohere Model Vault 私有部署。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（闭源，多模态嵌入与重排）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/voyage-embeddings|Voyage]]、[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/bge|BGE]]、Gemini Embedding 2（见 [[entities/gemini|Gemini]]）

## 时间线

- 2025-04-15 Embed 4（Embed Multimodal v4）
- 2025-10 Embed 4 上架 Amazon Bedrock
- 2026-09-30 Embed 5（Pro / Fast）
- 2026-10-21 Rerank 5（Pro / Fast）
- 2026-11-04 Embed 5 与 Rerank 5 上架 OpenRouter

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

- "We’re thrilled to announce the release of Embed 4, the most recent entrant into the Embed family of enterprise-focused large language models (LLMs)." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Cohere changelog，2025-04-15）
- "We’re pleased to announce the release of Embed 5, Cohere’s most powerful embeddings family yet." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Cohere changelog，2026-09-30）
