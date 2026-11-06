---
title: 向量数据库
type: concept
tags: [term]
layer: L1
aliases: ["Vector Database", "向量库", "Vector Store", "向量存储"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# 向量数据库

## 定义

以向量嵌入为索引、支持近似最近邻（ANN）检索的数据库，是 [[concepts/rag|RAG]] 与语义搜索常用的存储层。文本、图像等非结构化数据先由嵌入模型转成向量，查询时按 L2、内积、余弦等距离找出最相近的若干条，通常还会叠加元数据过滤和关键词检索。

## 关键特征

- **ANN 索引**：HNSW 是各家的共同选项（[[entities/milvus|Milvus]]、[[entities/pgvector|pgvector]] 等）；此外有 IVF / IVFFlat、DiskANN、SCANN、FLAT 暴力检索，以及 GPU 索引（Milvus 用 NVIDIA CAGRA）
- **混合检索**：稠密向量之外支持稀疏向量和 BM25 全文检索，再融合重排。Milvus 原生支持 BM25 和 SPLADE、BGE-M3 等稀疏嵌入，[[entities/qdrant|Qdrant]] 支持稠密、稀疏与多向量（ColBERT 类 late interaction），[[entities/weaviate|Weaviate]] 在一个查询接口里组合向量检索、关键词过滤、RAG 与重排
- **过滤**：按元数据或 JSON 负载过滤，例如 Qdrant 的 `must` / `should` / `must_not` 条件组合
- **[[concepts/quantization|量化]]与分层存储**：用量化降低内存（Qdrant README 称最多降 97%），用 mmap、磁盘索引、冷热分层或对象存储降成本；Milvus 3.0（2026-07）改为“湖原生”，直接在对象存储上建索引和检索
- **两条路线**：专用向量库（Milvus、Qdrant、Weaviate、[[entities/chroma|Chroma]]、闭源托管的 [[entities/pinecone|Pinecone]]），以及在已有数据库上加扩展（pgvector 让向量与业务数据同库，继承 Postgres 的 ACID 和 JOIN）
- **部署形态**：从进程内嵌入（Chroma、Milvus Lite、Qdrant Edge）到分布式集群，再到 serverless 托管（Zilliz Cloud、Qdrant Cloud、Weaviate Cloud、Pinecone）和客户云内托管（Zilliz BYOC、Pinecone BYOC）。托管服务也会消失：Chroma 2026-10 宣布并入 Replit，Chroma Cloud 于 2026-12 关停，开源版继续维护
- **2026 年的趋势**：向量库往“检索 / 知识基础设施”扩展。Milvus 3.0 湖原生，Zilliz Cloud 定位为 Vector Lakebase；Qdrant 主打“可组合向量搜索”；Pinecone 推出面向 Agent 的 Nexus、全文检索，并发布和 pgvector 一样跑在 Postgres 里的开源扩展 pg_pinecone

## 应用

- [[concepts/rag|RAG]] 与企业知识库检索
- 语义搜索、图像搜索
- 推荐系统
- Agent 的长期记忆与知识检索（如 Pinecone Nexus）

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]]
- **上游**：嵌入模型（L2）
- **下游**：应用框架通过集成包接入，例如 [[entities/langchain|LangChain]] 的 `langchain-milvus`、`langchain-qdrant`、`langchain-chroma`、`langchain-pinecone`、`langchain-weaviate`、`langchain-postgres`；[[entities/mastra|Mastra]]、[[entities/spring-ai|Spring AI]] 也内置向量库适配

## 相关概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/quantization|量化]]
- [[concepts/observational-memory|观察式记忆]]

## 相关实体

- [[entities/milvus|Milvus]]
- [[entities/zilliz|Zilliz]]
- [[entities/qdrant|Qdrant]]
- [[entities/pgvector|pgvector]]
- [[entities/pinecone|Pinecone]]
- [[entities/weaviate|Weaviate]]
- [[entities/chroma|Chroma]]
- [[entities/langchain|LangChain]]

## 我的判断

## 来源摘录

- "Milvus is a high-performance vector database built for scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Open-source vector similarity search for Postgres" — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Qdrant (read: quadrant) is a vector similarity search engine and vector database." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "pg_pinecone is an open-source (Apache 2.0) Postgres extension for search on the data you already store, built on the search engine Pinecone runs at scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Weaviate is a cloud-native vector database that stores both objects and vectors, enabling semantic search at scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
