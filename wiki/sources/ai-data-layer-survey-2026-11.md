---
title: AI 数据层调研（2026-11）
type: source
tags: [notes]
source_note: "[[AI数据层调研-2026-11]]"
url: https://github.com/milvus-io/milvus
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/milvus]]"
  - "[[entities/zilliz]]"
  - "[[entities/qdrant]]"
  - "[[entities/pgvector]]"
  - "[[entities/pinecone]]"
  - "[[entities/weaviate]]"
  - "[[entities/chroma]]"
  - "[[entities/common-crawl]]"
  - "[[entities/fineweb]]"
  - "[[entities/the-pile]]"
  - "[[entities/dolma]]"
  - "[[entities/scale-ai]]"
  - "[[entities/surge-ai]]"
  - "[[entities/mercor]]"
  - "[[entities/hugging-face]]"
  - "[[entities/meta-ai]]"
  - "[[entities/langchain]]"
  - "[[concepts/synthetic-data]]"
  - "[[concepts/data-labeling]]"
  - "[[concepts/vector-database]]"
  - "[[concepts/rag]]"
---

# AI 数据层调研（2026-11）

## Summary

梳理 L1 数据层的四块。向量库收录开源的 [[entities/milvus|Milvus]]（[[entities/zilliz|Zilliz]]）、[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/chroma|Chroma]]，Postgres 扩展 [[entities/pgvector|pgvector]]，以及闭源托管的 [[entities/pinecone|Pinecone]]，并据此核实改写 [[concepts/vector-database|向量数据库]]和 [[concepts/rag|RAG]] 两个概念页。预训练语料收录原始网页档案 [[entities/common-crawl|Common Crawl]]，以及在它之上过滤得到的 [[entities/fineweb|FineWeb]]（[[entities/hugging-face|Hugging Face]]）、[[entities/the-pile|The Pile]]（EleutherAI）、[[entities/dolma|Dolma]]（Ai2）。另外新建[[concepts/synthetic-data|合成数据]]和[[concepts/data-labeling|数据标注]]两个概念页，以及三家人类数据公司 [[entities/scale-ai|Scale AI]]、[[entities/surge-ai|Surge AI]]、[[entities/mercor|Mercor]]。

2026 年的两条主线：一是向量库往“检索基础设施”收拢，混合检索（稠密 + 稀疏 / BM25）、量化、对象存储成为标配，Milvus 3.0 改为湖原生，Qdrant 完成 5000 万美元 B 轮，Pinecone 换 CEO 并传出售；二是数据标注从众包转向高价专家数据，[[entities/meta-ai|Meta]] 以约 143 亿美元入股 Scale AI 49%，Surge AI、Mercor 的估值随之上升。

## Key Points

- **资料可靠性**：GitHub README / CHANGELOG 与 PyPI 元数据为一手；融资、公司、论文数字来自新闻与搜索摘要。huggingface.co、arxiv.org、commoncrawl.org 及各公司官网在调研会话中被网络策略拦截，未逐字核对，已在素材中标注「二手报道」
- **Milvus**：Go + C++，K8s 原生，HNSW / IVF / DiskANN / GPU CAGRA，BM25 与稀疏嵌入；LF AI & Data 项目、Apache 2.0；3.0（2026-07）湖原生
- **Qdrant**：Rust，负载过滤、稠密 / 稀疏 / 多向量、量化最多省 97% 内存、Qdrant Edge；2026-03 B 轮 5000 万美元
- **pgvector**：Postgres 扩展，HNSW（0.5.0 起）+ IVFFlat，`vector` / `halfvec` / `bit` / `sparsevec`；0.8.7（2026-10-01）
- **Pinecone**：闭源托管；2025-09 Edo Liberty 卸任 CEO、传探索出售；2026 年推出 Dedicated Read Nodes 与 Pinecone Nexus
- **Weaviate / Chroma**：Weaviate 导入时自动向量化，检索、RAG、重排在同一查询接口；Chroma 核心 API 只有 4 个函数，进程内即用
- **语料**：Common Crawl 2008 年起累计超过 10 PB；FineWeb 15 万亿 token / 96 个快照，FineWeb-Edu 1.3 万亿 token，FineWeb 2 覆盖 1000 多种语言；The Pile 由 22 个子集组成，Books3 于 2023 年被 DMCA 下架；Dolma 3 万亿 token，Dolma 3 约 6 万亿 token 预训练混合
- **合成数据**：Cosmopedia 250 亿 token；Nemotron-4-340B 对齐数据超过 98% 为合成；Nature 2024 论文警告“模型崩溃”
- **数据公司**：Meta 入股 Scale AI 49%（估值约 290 亿美元）后 Scale 裁员 14%；Surge AI 2024 年收入超过 10 亿美元，洽谈 150 亿–250 亿美元估值；Mercor 2025-10 估值 100 亿美元
- **框架集成**：[[entities/langchain|LangChain]] 为六种向量库都提供独立集成包（`langchain-milvus`、`langchain-qdrant`、`langchain-chroma`、`langchain-pinecone`、`langchain-weaviate`、`langchain-postgres`）

## Mentioned Pages

- [[entities/milvus|Milvus]]
- [[entities/zilliz|Zilliz]]
- [[entities/qdrant|Qdrant]]
- [[entities/pgvector|pgvector]]
- [[entities/pinecone|Pinecone]]
- [[entities/weaviate|Weaviate]]
- [[entities/chroma|Chroma]]
- [[entities/common-crawl|Common Crawl]]
- [[entities/fineweb|FineWeb]]
- [[entities/the-pile|The Pile]]
- [[entities/dolma|Dolma]]
- [[entities/scale-ai|Scale AI]]
- [[entities/surge-ai|Surge AI]]
- [[entities/mercor|Mercor]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/meta-ai|Meta AI]]
- [[entities/nvidia|NVIDIA]]
- [[entities/langchain|LangChain]]
- [[entities/cuda|CUDA]]
- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/synthetic-data|合成数据]]
- [[concepts/data-labeling|数据标注]]
- [[concepts/quantization|量化]]
