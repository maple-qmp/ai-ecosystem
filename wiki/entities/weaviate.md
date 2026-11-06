---
title: Weaviate
type: entity
tags: [project]
kind: infra
layer: L1
aliases: ["Weaviate", "weaviate/weaviate", "Weaviate Cloud"]
competitors: ["[[entities/milvus]]", "[[entities/qdrant]]", "[[entities/pinecone]]", "[[entities/chroma]]", "[[entities/pgvector]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Weaviate

## 描述

用 Go 编写的开源云原生[[concepts/vector-database|向量数据库]]，同名公司总部在阿姆斯特丹。它同时存储对象和向量，把向量相似度检索、关键词过滤、[[concepts/rag|RAG]] 和重排放进同一个查询接口。特色是“导入即向量化”：可以在导入时调用集成的模型提供方（OpenAI、Cohere、Hugging Face 等）自动生成嵌入，也可以导入预先算好的向量。生产特性有多租户、复制和 RBAC；部署方式有 Docker、Kubernetes、Weaviate Cloud 以及 AWS / GCP 市场。2023-04 完成 5000 万美元 B 轮，Index Ventures 领投（二手报道）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库
- **上游依赖**：嵌入模型提供方（可选，导入时自动向量化）
- **竞争 / 替代**：[[entities/milvus|Milvus]]、[[entities/qdrant|Qdrant]]、[[entities/pinecone|Pinecone]]、[[entities/chroma|Chroma]]、[[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 的 `langchain-weaviate` 集成包

## 时间线

- 2019-11-04 Python 客户端 weaviate-client 首个版本（PyPI）
- 2023-04 B 轮 5000 万美元，Index Ventures 领投、Battery Ventures 参投（二手报道；另有单一来源称 2025-10 有 C 轮，未能证实）
- 2026-10-26 weaviate-client 4.24.1；README 示例镜像为 1.36.0

## 相关实体

- [[entities/milvus|Milvus]]
- [[entities/qdrant|Qdrant]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Weaviate is a cloud-native vector database that stores both objects and vectors, enabling semantic search at scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
