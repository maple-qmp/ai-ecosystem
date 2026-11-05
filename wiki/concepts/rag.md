---
title: 检索增强生成（RAG）
type: concept
tags: [method]
layer: L4
aliases: ["RAG", "Retrieval-Augmented Generation", "检索增强生成"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]", "[[sources/langchain-ecosystem-survey-2026-11]]", "[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# 检索增强生成（RAG）

## 定义

在生成前先从外部知识库检索相关内容并放进上下文，让模型基于最新或私有资料作答。方法由 Lewis、Perez、Kiela 等在 NeurIPS 2020 论文「Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks」中提出（论文收录在 [[entities/meta-ai|Meta AI]] 的研究页）：参数化记忆是预训练的 seq2seq 模型，非参数化记忆是 Wikipedia 的稠密向量索引，用预训练的神经检索器访问。论文报告它在三项开放域问答任务上达到 SOTA，生成的语言也比纯参数化基线更具体、多样、符合事实。

## 关键特征

- **两种记忆**：模型权重里的参数化知识，加上可以随时更新的外部索引，所以能接入私有数据并降低幻觉
- **核心环节**：切分、嵌入、检索、重排、拼接上下文
- **检索层**：通常用[[concepts/vector-database|向量数据库]]存嵌入，并叠加 BM25 / 稀疏向量做混合检索、按元数据过滤。[[entities/weaviate|Weaviate]] 把检索、RAG 与重排放进同一个查询接口；[[entities/milvus|Milvus]] 的官方教程覆盖 RAG、混合检索和多模态 RAG
- **框架支持**：[[entities/langchain|LangChain]] 早期以文档加载器和 RAG 组件闻名，向量库集成以独立包发布；[[entities/mastra|Mastra]] 内置分块、嵌入、检索、向量库和 GraphRAG

## 应用

- 企业知识库问答
- 文档助手
- Agent 的知识检索与长期记忆

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- **下层依赖**：[[maps/L1-数据|L1-数据]] 的向量库与语料

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/observational-memory|观察式记忆]]

## 相关实体

- [[entities/langchain|LangChain]]
- [[entities/mastra|Mastra]]
- [[entities/meta-ai|Meta AI]]
- [[entities/milvus|Milvus]]
- [[entities/weaviate|Weaviate]]

## 我的判断

## 来源摘录

- "Weaviate is a cloud-native vector database that stores both objects and vectors, enabling semantic search at scale." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
