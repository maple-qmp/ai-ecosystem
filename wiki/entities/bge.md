---
title: BGE
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["BGE", "BAAI General Embedding", "BGE-M3", "bge-large", "BGE-VL", "FlagEmbedding"]
org: "[[entities/baai|北京智源人工智能研究院（BAAI）]]"
released: "2023-08"
open_weights: true
competitors: ["[[entities/qwen3-embedding]]", "[[entities/openai-embeddings]]", "[[entities/voyage-embeddings]]", "[[entities/cohere-embed]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# BGE

## 描述

[[entities/baai|北京智源人工智能研究院（BAAI）]]的开放权重[[concepts/embedding|嵌入]]模型家族（BAAI General Embedding），代码和工具在 FlagEmbedding 仓库，MIT 许可。2023-08 首批 bge-large-* 发布时自称在 MTEB 和 C-MTEB 排第一，同月接入 LangChain，C-MTEB 中文嵌入评测（31 个数据集）也出自同一团队。BGE-M3（2024-01-30）把多语言（100 多种）、多粒度（最长 8192）和稠密、词汇、多向量三种检索合在一个模型里，是开源 [[concepts/rag|RAG]] 管线的常用默认。之后陆续推出基于 LLM 的重排模型、以 Gemma 2 为基座的多语言模型、多模态的 BGE-VL（2025-03）、代码检索的 bge-code-v1（2025-05），以及以 Qwen3-8B 为基座、面向推理密集检索的 bge-reasoner-embed（2025-09）。截至 2026-11，Hugging Face 上没有更新的 BGE 模型。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，嵌入与重排）
- **上游依赖**：部分型号以 Gemma 2、MiniCPM、[[entities/qwen|Qwen3]] 等 LLM 为基座
- **竞争 / 替代**：[[entities/qwen3-embedding|Qwen3-Embedding]]、[[entities/openai-embeddings|OpenAI text-embedding]]、[[entities/voyage-embeddings|Voyage]]、[[entities/cohere-embed|Cohere Embed]]

## 时间线

- 2023-08-01 C-MTEB 中文嵌入评测
- 2023-08-02 bge-large-* 发布
- 2023-08-09 接入 LangChain
- 2023-09-15 技术报告与训练数据 MTP 公开
- 2024-01-30 BGE-M3
- 2024-03-18 LLM 基座重排模型；Visualized-BGE
- 2024-07-26 bge-multilingual-gemma2、bge-en-icl
- 2025-03-06 BGE-VL 多模态嵌入
- 2025-05 bge-code-v1、BGE-VL-v1.5、BGE-VL-Screenshot
- 2025-09-22 bge-reasoner-embed-qwen3-8b

## 相关实体

- [[entities/baai|北京智源人工智能研究院（BAAI）]]
- [[entities/langchain|LangChain]]
- [[entities/qwen3-embedding|Qwen3-Embedding]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/embedding|嵌入（Embedding）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Release `bge-large-*`(short for BAAI General Embedding) Models, rank 1st on MTEB and C-MTEB benchmark!" — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（FlagOpen/FlagEmbedding README，2023-08-02 条目，原文加粗与表情已去掉）
