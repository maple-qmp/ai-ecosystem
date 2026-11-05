---
title: Milvus
type: entity
tags: [project]
kind: infra
layer: L1
aliases: ["Milvus", "milvus-io/milvus", "Milvus Lite"]
org: "[[entities/zilliz]]"
released: "2019"
competitors: ["[[entities/qdrant]]", "[[entities/weaviate]]", "[[entities/pinecone]]", "[[entities/chroma]]", "[[entities/pgvector]]"]
depends_on: ["[[entities/cuda]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Milvus

## 描述

开源的分布式[[concepts/vector-database|向量数据库]]，用 Go 和 C++ 编写，K8s 原生、计算与存储分离，可水平扩展到数十亿向量。它支持 HNSW、IVF、FLAT、SCANN、DiskANN 等索引及量化变体，GPU 索引用 NVIDIA 的 CAGRA（cuVS），并原生支持 BM25 全文检索和 SPLADE、BGE-M3 等稀疏嵌入，稠密与稀疏向量可放进同一个 collection 做混合检索。部署形态从 `pip install` 即用的 Milvus Lite、单机 Standalone 到分布式集群；托管版是 [[entities/zilliz|Zilliz]] Cloud。项目属于 LF AI & Data Foundation，Apache 2.0 协议，Zilliz 是主要贡献者。2026 年发布的 3.0 改为“湖原生”架构，可以直接在对象存储上建索引和检索。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库
- **上游依赖**：[[entities/cuda|CUDA]]（GPU 索引，可选）
- **竞争 / 替代**：[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/pinecone|Pinecone]]、[[entities/chroma|Chroma]]、[[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 有 `langchain-milvus` 集成包

## 时间线

- 2019-06-16 Python SDK pymilvus 首个版本 0.1.0（PyPI）
- 2026-07 发布 Milvus 3.0：湖原生架构、向量原生批处理算子（去重、聚类）、体积约 1/3 的稀疏索引、新存储引擎 Loon（各来源日期为 07-16 / 07-29 / 07-31，说法不一）
- 2026-09-18 pymilvus 3.0.2

## 相关实体

- [[entities/zilliz|Zilliz]]
- [[entities/qdrant|Qdrant]]
- [[entities/weaviate|Weaviate]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Milvus is a high-performance vector database built for scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "The Milvus open-source project is under LF AI & Data Foundation, distributed with Apache 2.0 License, with Zilliz as its major contributor." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Milvus also natively supports full text search with BM25 as well as learned sparse embeddings such as SPLADE and BGE-M3." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
