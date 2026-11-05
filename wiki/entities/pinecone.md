---
title: Pinecone
type: entity
tags: [product]
kind: infra
layer: L1
aliases: ["Pinecone", "Pinecone Systems", "Pinecone Nexus"]
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

闭源、全托管的[[concepts/vector-database|向量数据库]]服务，同名公司 Pinecone Systems 由 Edo Liberty 创立，是本层名单里唯一没有开源主仓库的产品。托管服务基于 serverless 架构；2026 年推出专用读节点 Dedicated Read Nodes（04 月 GA）和面向自主 Agent 的知识引擎 Pinecone Nexus，并新增 AWS 法兰克福和新加坡区域，新闻稿自称服务 9,000 多家客户、80 万开发者。2023-04 B 轮 1 亿美元、估值 7.5 亿美元。2025-09 创始人卸任 CEO 改任首席科学家，同期有报道称公司在探索出售，截至 2026-11 未见成交（均为二手报道）。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库（托管服务）
- **竞争 / 替代**：开源的 [[entities/milvus|Milvus]]（[[entities/zilliz|Zilliz]] Cloud）、[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/chroma|Chroma]]，以及 [[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 的 `langchain-pinecone` 集成包

## 时间线

- 2023-04-27 B 轮 1 亿美元，估值 7.5 亿美元（TechCrunch）
- 2024-05-03 PyPI 上 `pinecone` 包首个版本 4.0.0
- 2025-09 Edo Liberty 卸任 CEO 转任首席科学家，前 Google 高管 Ash Ashutosh 接任；同期 The Information、Calcalist 报道公司探索出售，潜在买家包括 Oracle、IBM、MongoDB、Snowflake
- 2026-04 Dedicated Read Nodes GA
- 2026-05 首个亚洲 serverless 区域（新加坡）；同年推出 AWS 法兰克福区域与 Pinecone Nexus
- 2026-11-03 Python SDK 10.3.0

## 相关实体

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

- 一手资料中无 Pinecone 原文（公司官网在调研会话中无法访问），以上事实来自 [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]] 中的二手报道与 PyPI 元数据
