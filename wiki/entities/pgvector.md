---
title: pgvector
type: entity
tags: [project]
kind: infra
layer: L1
aliases: ["pgvector", "PGVector", "pgvector/pgvector"]
released: "2021-04"
competitors: ["[[entities/milvus]]", "[[entities/qdrant]]", "[[entities/weaviate]]", "[[entities/pinecone]]", "[[entities/chroma]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# pgvector

## 描述

PostgreSQL 的开源向量相似度检索扩展（支持 Postgres 13+），思路是把向量和其余业务数据存在同一个库里，直接继承 Postgres 的 ACID、时间点恢复和 JOIN。它支持精确与近似最近邻检索，向量类型有单精度 `vector`、半精度 `halfvec`、二值 `bit` 和稀疏 `sparsevec`，距离有 L2、内积、余弦、L1、Hamming、Jaccard；索引有 HNSW 和 IVFFlat，HNSW 下 `vector` 最多 2,000 维、`halfvec` 4,000 维。它是“传统数据库加向量插件”路线的代表，可通过 Docker、Homebrew、APT、conda-forge 等安装，Postgres.app 和许多托管 Postgres 服务都预装了它。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库（数据库扩展）
- **上游依赖**：PostgreSQL
- **竞争 / 替代**：专用向量库 [[entities/milvus|Milvus]]、[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/pinecone|Pinecone]]、[[entities/chroma|Chroma]]
- **下游**：[[entities/langchain|LangChain]] 的 `langchain-postgres` 集成包

## 时间线

- 2021-04-20 0.1.0
- 2023-08-28 0.5.0，加入 HNSW 索引
- 2024-01-29 0.6.0
- 2024-04-29 0.7.0
- 2024-10-30 0.8.0
- 2026-10-01 0.8.7（0.9.0 开发中）

## 相关实体

- [[entities/milvus|Milvus]]
- [[entities/qdrant|Qdrant]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Open-source vector similarity search for Postgres" — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Store your vectors with the rest of your data." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
