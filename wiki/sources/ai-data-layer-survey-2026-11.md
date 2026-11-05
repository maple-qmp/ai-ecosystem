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

2026 年的三条主线：一是向量库往“检索 / 知识基础设施”扩展并开始洗牌，混合检索（稠密 + 稀疏 / BM25）、量化、对象存储成为标配，Milvus 3.0 改为湖原生，Qdrant 完成 5000 万美元 B 轮，Pinecone 换 CEO、推出 Nexus 并开源 Postgres 扩展 pg_pinecone，Chroma 并入 Replit、关停 Chroma Cloud；二是数据标注从众包转向高价专家数据，[[entities/meta-ai|Meta]] 投资 Scale AI（估值超过 290 亿美元），Surge AI、Mercor 估值随之上升，Mercor 又因数据泄露被 Meta 暂停合同；三是开放数据平台本身被并购，报道称 [[entities/nvidia|NVIDIA]] 同意以约 129 亿美元收购 Hugging Face（尚无官方公告）。

## Key Points

- **资料可靠性**：第一轮只有 GitHub README / CHANGELOG 与 PyPI 元数据是一手；网络放开后的第二轮又对照 Hugging Face 数据集卡片、arXiv 摘要、Nature 原文、Common Crawl 官网、Zilliz / Qdrant / Pinecone / Scale AI / Chroma 官方公告和 TechCrunch 原文逐条核实（素材第七节）。仍为二手的有：Zilliz 与 Weaviate 融资、Pinecone 出售传闻、Scale 裁员与 49% / 143 亿美元、Surge AI 全部、Mercor 200 亿美元洽谈、NVIDIA 收购 HF
- **Milvus**：Go + C++，K8s 原生，HNSW / IVF / DiskANN / GPU CAGRA，BM25 与稀疏嵌入；LF AI & Data 项目、Apache 2.0；3.0（2026-07-16）湖原生，存储引擎 Loon 用 Vortex 列式格式
- **Qdrant**：Rust，负载过滤、稠密 / 稀疏 / 多向量、量化最多省 97% 内存、Qdrant Edge；2026-03 B 轮 5000 万美元
- **pgvector**：Postgres 扩展，HNSW（0.5.0 起）+ IVFFlat，`vector` / `halfvec` / `bit` / `sparsevec`；0.8.7（2026-10-01）
- **Pinecone**：托管服务；2025-09-08 Ash Ashutosh 接任 CEO、传探索出售；2026 年 Nexus GA（08-06）、全文检索 GA（09-09）、BYOC GA（09-23）、开源 pg_pinecone（10-27）
- **Weaviate / Chroma**：Weaviate 导入时自动向量化，检索、RAG、重排在同一查询接口；Chroma 核心 API 只有 4 个函数，2026-10 宣布并入 Replit，Chroma Cloud 于 2026-12-07 停写、12-22 停读，开源版继续 Apache 2.0
- **语料**：Common Crawl 2008 年起累计超过 10 PB；FineWeb 首发 15 万亿 token / 96 个快照，v1.4.0（2025-07）超过 18.5 万亿 token，FineWeb-Edu 1.3 万亿 token，FineWeb 2 约 20 TB、1,868 个语言—文字组合；The Pile 825 GiB、22 个子集，Books3 于 2023 年被 DMCA 下架；Dolma 3 万亿 token，Dolma 3 预训练混合 5.93 万亿 token、清洗池 9.31 万亿 token
- **合成数据**：Cosmopedia 250 亿 token；Nemotron-4-340B 对齐数据超过 98% 为合成；Nature 2024 论文警告“模型崩溃”
- **数据公司**：Meta 投资 Scale AI（2025-06-12，估值超过 290 亿美元）后 Scale 裁员 14%；Surge AI 2024 年收入超过 10 亿美元，洽谈 150 亿–250 亿美元估值，约 100 万标注员；Mercor 2025-10 估值 100 亿美元，2026-03 因 LiteLLM 被入侵泄露数据
- **Hugging Face**：报道称 NVIDIA 2026-09 同意以约 129 亿美元收购，截至 2026-11-05 无官方公告
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
