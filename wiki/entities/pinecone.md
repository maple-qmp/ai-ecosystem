---
title: Pinecone
type: entity
tags: [product]
kind: infra
layer: L1
aliases: ["Pinecone", "Pinecone Systems", "Pinecone Nexus", "pg_pinecone"]
competitors: ["[[entities/milvus]]", "[[entities/qdrant]]", "[[entities/weaviate]]", "[[entities/chroma]]", "[[entities/pgvector]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Pinecone

## 描述

全托管的[[concepts/vector-database|向量数据库]]服务，同名公司 Pinecone Systems 总部在旧金山，由 Edo Liberty 创立。数据库本身不开源，托管服务基于 serverless 架构。2026 年它把产品重心放在“给 AI 提供知识”：面向企业 Agent 的知识引擎 Pinecone Nexus（08 月 GA）、全文检索（09 月 GA）、部署在客户自有云内的 BYOC（09 月 GA），以及 10 月发布的 pg_pinecone，这是一个 Apache 2.0 开源的 Postgres 扩展，把 Pinecone 自己的检索引擎带进 Postgres，与 [[entities/pgvector|pgvector]] 同属 Postgres 扩展路线。2023-04 B 轮 1 亿美元、投后估值 7.5 亿美元，由 Andreessen Horowitz 领投。2025-09 创始人把 CEO 一职交给 Ash Ashutosh，自己改任首席科学家；同期有报道称公司在探索出售，截至 2026-11 未见成交（出售为二手报道）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库（托管服务）
- **竞争 / 替代**：开源的 [[entities/milvus|Milvus]]（[[entities/zilliz|Zilliz]] Cloud）、[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/chroma|Chroma]]，以及 Postgres 上的 [[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 的 `langchain-pinecone` 集成包；Nexus 面向企业 [[concepts/ai-agent|AI Agent]]

## 时间线

- 2023-04-27 B 轮 1 亿美元，投后估值 7.5 亿美元，Andreessen Horowitz 领投，ICONIQ Growth、Menlo Ventures、Wing Venture Capital 参投，累计 1.38 亿美元；当时客户约 1,500 家（TechCrunch）
- 2024-05-03 PyPI 上 `pinecone` 包首个版本 4.0.0
- 2025-09-08 Edo Liberty 宣布 Ash Ashutosh 出任 CEO，自己改任首席科学家（Pinecone 博客）；同期 The Information、Calcalist 报道公司探索出售，潜在买家包括 Oracle、IBM、MongoDB、Snowflake（二手报道）
- 2026-04 Dedicated Read Nodes GA（二手报道）
- 2026-05 首个亚洲 serverless 区域（新加坡），同年还新增 AWS 法兰克福区域（新闻稿）
- 2026-08-06 Pinecone Nexus GA
- 2026-09-09 全文检索 GA
- 2026-09-23 BYOC GA
- 2026-10-27 发布 pg_pinecone（Apache 2.0 开源的 Postgres 扩展）
- 2026-11-03 Python SDK 10.3.0

## 相关实体

- [[entities/pgvector|pgvector]]
- [[entities/chroma|Chroma]]
- [[entities/milvus|Milvus]]
- [[entities/qdrant|Qdrant]]
- [[entities/weaviate|Weaviate]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "I'm thrilled to share that Ash Ashutosh is joining Pinecone as our new CEO!" — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "pg_pinecone is an open-source (Apache 2.0) Postgres extension for search on the data you already store, built on the search engine Pinecone runs at scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
