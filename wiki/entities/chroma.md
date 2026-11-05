---
title: Chroma
type: entity
tags: [project]
kind: infra
layer: L1
aliases: ["Chroma", "ChromaDB", "chromadb", "Chroma Cloud", "Chroma Foundation"]
released: "2023-02"
competitors: ["[[entities/milvus]]", "[[entities/qdrant]]", "[[entities/weaviate]]", "[[entities/pinecone]]", "[[entities/pgvector]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# Chroma

## 描述

开源的嵌入 / [[concepts/vector-database|向量数据库]] ChromaDB，Apache 2.0 协议，以上手简单著称：`pip install chromadb` 或 `npm install chromadb` 后即可在进程内使用，核心 API 只有 4 个函数，`add` 时会自动完成分词、嵌入和建索引；需要时用 `chroma run` 切换成客户端—服务端模式，也有分布式、serverless 的版本。同名公司 2022 年成立于旧金山，CEO Jeff Huber，最初做训练数据的主动学习，ChatGPT 发布后转向给 Agent 提供上下文。2026 年中它推出面向企业的上下文层产品 Foundation：基于 ChromaDB 和自研检索引擎 Context-1，可通过 MCP 接入 [[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex]]、[[entities/cursor|Cursor]]、Slack。2026-10 Chroma 宣布签署最终协议并入 Replit，托管服务 Chroma Cloud 随之关停（12-07 停写、12-22 停读）。开源 ChromaDB 继续以 Apache 2.0 提供，Chroma 把部分私有代码合进了开源仓库，Replit 承诺继续贡献；博客称开源版每月下载 600 万次、GitHub 接近 3 万星。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 向量库
- **竞争 / 替代**：[[entities/milvus|Milvus]]、[[entities/qdrant|Qdrant]]、[[entities/weaviate|Weaviate]]、[[entities/pinecone|Pinecone]]（已发布从 Chroma Cloud 迁移的指南）、[[entities/pgvector|pgvector]]
- **下游**：[[entities/langchain|LangChain]] 的 `langchain-chroma` 集成包

## 时间线

- 2022 公司成立
- 2023-02-09 chromadb 首次发布到 PyPI
- 2023-04-06 种子轮 1800 万美元，Quiet Capital 领投（二手报道）；Replit 的 Michele Catasta 与 Amjad Masad 是早期投资人
- 2026-05-05 chromadb 1.5.9（截至 2026-11-05 PyPI 上的最新版）
- 2026 年中 推出企业上下文层产品 Foundation
- 2026-10-23 宣布签署最终协议并入 Replit，金额未披露（日期据二手报道，与关停时间表一致）
- 2026-12-07 Chroma Cloud 停止写入（计划）
- 2026-12-22 Chroma Cloud 停止读取（计划）

## 相关实体

- [[entities/qdrant|Qdrant]]
- [[entities/pinecone|Pinecone]]
- [[entities/langchain|LangChain]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/vector-database|向量数据库]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/model-context-protocol|MCP]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Today I’m excited to announce that Chroma has signed a definitive agreement to join Replit." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "This transition applies only to the existing Chroma Cloud service. Open-source ChromaDB remains available under the Apache 2.0 license, and Replit will continue contributing to the project." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Chroma - the open-source data infrastructure for AI." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "The core API is only 4 functions" — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
