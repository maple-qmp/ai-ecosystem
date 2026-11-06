---
title: 嵌入（Embedding）
type: concept
tags: [method]
layer: L2
aliases: ["嵌入", "Embedding", "向量嵌入", "文本嵌入", "嵌入模型", "Text Embedding", "Reranker", "重排模型"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# 嵌入（Embedding）

## 定义

把文本、图像等输入映射成固定长度的向量，使语义相近的内容在向量空间里距离也近。做这件事的模型叫嵌入模型，它是语义搜索、[[concepts/rag|检索增强生成（RAG）]]和[[concepts/vector-database|向量数据库]]的上游。

## 关键特征

- **维度可调**：主流模型支持 Matryoshka 式截短（MRL），同一向量取前 256～4096 维都可用，例如 [[entities/openai-embeddings|OpenAI text-embedding-3-large]] 最高 3072 维、[[entities/qwen3-embedding|Qwen3-Embedding-8B]] 4096 维、[[entities/cohere-embed|Cohere Embed 4]] 256～1536 维；Cohere Embed 5 的 Pro / Fast 两档共用一个向量空间，可以用大模型建索引、用小模型编码查询
- **嵌入 + 重排**：检索先用嵌入模型召回，再用重排模型（cross-encoder）精排；Qwen3、BGE、Voyage、Cohere（Embed 5 / Rerank 5）都成对发布嵌入和重排模型
- **指令感知**：Qwen3-Embedding 等允许按任务写一句指令，官方称一般能提升 1%～5%
- **多模态嵌入**：2025—2026 年的主线是把文本、图像、截图、视频、音频放进同一向量空间：Qwen3-VL-Embedding、BGE-VL、voyage-multimodal-3.5、Cohere Embed 4 / 5、Gemini Embedding 2（2026-03 预览、04-22 GA）
- **向量空间不兼容**：换模型或换代要重算全部向量，例如 Gemini Embedding 2 与 gemini-embedding-001 不兼容；旧模型也会下线，如 Google 的 text-embedding-004 已于 2026-01-14 关闭
- **2026 年的格局**：下半年的新发布集中在闭源厂商（Cohere Embed 5 于 2026-09-30 发布）；开放权重阵营（Qwen、BGE）在 2026 年没有新的通用文本嵌入模型；OpenAI 仍停留在 2024 年的 text-embedding-3
- **评测**：MTEB（多语言）、C-MTEB（中文，BAAI 2023-08 发布）、RTEB（检索）、MMEB（多模态）

## 应用

- [[concepts/rag|RAG]] 的召回环节
- 语义搜索、推荐、聚类与去重
- 跨模态检索（以文搜图、以图搜视频）

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]]（嵌入模型）；下游是 [[maps/L1-数据|L1-数据]] 的向量数据库和 [[maps/L4-开发工具与Agent|L4]] 的 RAG 框架
- 趋势：数据库厂商直接内置嵌入模型，例如 MongoDB 收购 [[entities/voyage-ai|Voyage AI]] 后把模型集成进 Atlas

## 相关概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]
- [[concepts/transformer|Transformer]]

## 相关实体

- [[entities/openai-embeddings|OpenAI text-embedding]]
- [[entities/qwen3-embedding|Qwen3-Embedding]]
- [[entities/bge|BGE]]
- [[entities/voyage-embeddings|Voyage]]
- [[entities/cohere-embed|Cohere Embed]]
- [[entities/gemini|Gemini]]（Gemini Embedding）
- [[entities/langchain|LangChain]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Gemini Embedding 2 is our first natively multimodal embedding model that maps text, images, video, audio and documents into a single embedding space, enabling multimodal retrieval and classification across different types of media — and it’s available now in public preview." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（Google 博客）
- "The 8B size embedding model ranks No.1 in the MTEB multilingual leaderboard (as of June 5, 2025, score 70.58), while the reranking model excels in various text retrieval scenarios." — [[sources/multimodal-embedding-models-survey-2026-11|多模态与嵌入模型调研]]（QwenLM/Qwen3-Embedding README，原文加粗已去掉）
