---
title: LlamaIndex
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["LlamaIndex", "llama-index", "LlamaAgents", "LlamaIndex Workflows", "LlamaParse", "LlamaCloud"]
released: "2022-11"
competitors: ["[[entities/langchain]]", "[[entities/langgraph]]", "[[entities/crewai]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# LlamaIndex

## 描述

LlamaIndex Inc.（GitHub 组织 run-llama）的开源 LLM 应用框架（MIT，约 5.28 万星），早期以 [[concepts/rag|RAG]] 数据框架闻名，由 `llama-index-core` 加 300 多个模型、嵌入、[[concepts/vector-database|向量库]]集成包组成。2026 年公司战略转向文档处理：主要精力放在 LlamaParse（Agentic OCR、解析、抽取、索引平台）上，2026-02 起 LlamaCloud 在文档和官网统一改名为 LlamaParse，开源框架继续可用。Agent 部分是事件驱动、异步、基于 step 的 Agent Workflows（`llama-index-workflows`），已拆到独立仓库 llama-agents，以 LlamaAgents 的名义定位为面向文档的 Agent 框架，到 2026-10 已更新到 2.26.1。框架主包仍停在 0.14.x，2026-09 之后没有新版本。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（各模型厂商 API、向量数据库）
- **竞争 / 替代**：[[entities/langchain|LangChain]]、[[entities/langgraph|LangGraph]]、[[entities/crewai|CrewAI]]

## 时间线

- 2022-11 仓库创建
- 2025-06-25 llama-index-workflows 1.0.0
- 2025-08-29 Workflows 2.0.0
- 2025-09-08 llama-index 0.14.0
- 2026-01 Agent Workflows 加入 ACP 集成（文件系统与 bash 工具、MCP 服务器、持久记忆）
- 2026-02 LlamaCloud 改名 LlamaParse
- 2026-09-21 llama-index 0.14.25
- 2026-10-21 llama-index-workflows 2.26.1

## 相关实体

- [[entities/langchain|LangChain]]
- [[entities/pinecone|Pinecone]]
- [[entities/qdrant|Qdrant]]

## 相关概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/vector-database|向量数据库]]
- [[concepts/python-agent-development|Python Agent 开发]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The current focus of LlamaIndex is to build the best AI-powered engine for document parsing and extraction." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "An open-source framework for building and shipping document-centric agents in Python." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
