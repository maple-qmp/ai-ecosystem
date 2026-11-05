---
title: Chroma
type: entity
tags: [project]
kind: infra
layer: L1
aliases: ["Chroma", "ChromaDB", "chromadb", "Chroma Cloud"]
released: "2023-02"
competitors: ["[[entities/milvus]]", "[[entities/qdrant]]", "[[entities/weaviate]]", "[[entities/pinecone]]", "[[entities/pgvector]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Chroma

## 描述

开源的嵌入 / [[concepts/vector-database|向量数据库]]，Apache 2.0 协议，自称“the open-source data infrastructure for AI”。它以上手简单著称：`pip install chromadb` 或 `npm install chromadb` 后即可在进程内使用，核心 API 只有 4 个函数，`add` 时会自动完成分词、嵌入和建索引，也可以自带嵌入；需要时用 `chroma run` 切换成客户端—服务端模式。托管版 Chroma Cloud 提供 serverless 的向量、混合和全文检索。同名公司 2022 年成立于旧金山，CEO Jeff Huber，2023-04 完成 1800 万美元种子轮（二手报道）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库
- **竞争 / 替代**：[[entities/milvus|Milvus]]、[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/pinecone|Pinecone]]、[[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 的 `langchain-chroma` 集成包

## 时间线

- 2023-02-09 chromadb 首次发布到 PyPI
- 2023-04-06 种子轮 1800 万美元，Quiet Capital 领投（二手报道）
- 2026-05-05 chromadb 1.5.9（PyPI 上的最新版；README 称每周一发布新版本）

## 相关实体

- [[entities/qdrant|Qdrant]]
- [[entities/pinecone|Pinecone]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Chroma - the open-source data infrastructure for AI." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "The core API is only 4 functions" — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
