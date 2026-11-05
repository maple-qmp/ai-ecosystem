---
title: Qdrant
type: entity
tags: [project]
kind: infra
layer: L1
aliases: ["Qdrant", "qdrant/qdrant", "Qdrant Cloud", "Qdrant Edge"]
released: "2021"
competitors: ["[[entities/milvus]]", "[[entities/weaviate]]", "[[entities/pinecone]]", "[[entities/chroma]]", "[[entities/pgvector]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Qdrant

## 描述

用 Rust 编写的开源向量相似度搜索引擎和[[concepts/vector-database|向量数据库]]，名字读作 quadrant，同名公司总部在柏林。数据单位是带 JSON 负载（payload）的“点”，强项是负载过滤：关键词、全文、数值范围、地理位置等条件可以用 `should` / `must` / `must_not` 组合。它支持稠密、稀疏和多向量检索（包括 ColBERT 这类 late interaction 模型）、混合检索、内置[[concepts/quantization|量化]]（README 称最多降低 97% 内存）和分布式部署，提供 REST 与 gRPC 接口及 Go、Rust、JS/TS、Python、.NET、Java 官方客户端。托管版 Qdrant Cloud 有免费额度；Qdrant Edge 是嵌入应用进程内运行的轻量版本，面向边缘和离线场景。2026-03 公司完成 5000 万美元 B 轮，并把定位概括为“可组合向量搜索”：稠密、稀疏、过滤、多向量、自定义打分都是查询时自由组合的原语。公告称生产用户包括 Canva、HubSpot、Roche、Bosch、OpenTable 等，全部包累计下载超过 2.5 亿次、GitHub 2.9 万星。2026 年发布的 1.20 版支持不依赖稀疏向量的 BM25 混合检索。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库
- **上游依赖**：—
- **竞争 / 替代**：[[entities/milvus|Milvus]]、[[entities/weaviate|Weaviate]]、[[entities/pinecone|Pinecone]]、[[entities/chroma|Chroma]]、[[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 有 `langchain-qdrant` 集成包；README 还提供一套给编程 Agent 用的 [[concepts/agent-skills|Agent Skills]]

## 时间线

- 2021-02-09 Python 客户端 qdrant-client 首个版本 0.1.0（PyPI）
- 2026-03-12 官方博客宣布 5000 万美元 B 轮，AVP 领投，Bosch Ventures、Unusual Ventures、Spark Capital、42CAP 参投（累计约 8750 万美元为二手报道）
- 2026 发布 Qdrant 1.20（BM25 混合检索无需稀疏向量）；Qdrant Serverless 标为“即将推出”
- 2026-10-22 qdrant-client 1.20.0

## 相关实体

- [[entities/milvus|Milvus]]
- [[entities/weaviate|Weaviate]]
- [[entities/pinecone|Pinecone]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/quantization|量化]]
- [[concepts/agent-skills|Agent Skills]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Today we’re announcing $50 million in Series B funding, led by AVP, with participation from Bosch Ventures, Unusual Ventures, Spark Capital, and 42CAP." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Qdrant (read: quadrant) is a vector similarity search engine and vector database." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Built-in quantization cuts RAM usage by up to 97% and lets you tune the trade-off between search speed and precision." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Qdrant Edge is a lightweight version of Qdrant designed for edge devices and resource-constrained environments." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
