---
title: Mastra
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Mastra", "Mastra 框架", "@mastra/core"]
org: "[[entities/mastra-inc]]"
released: "2025-02"
competitors: ["[[entities/langchain]]", "[[entities/langgraph]]", "[[entities/vercel-ai-sdk]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# Mastra

## 描述

[[entities/mastra-inc|Mastra 公司]]开发的开源 TypeScript Agent 框架（npm 核心包 `@mastra/core`），把 Agent、工作流、记忆、RAG、评测、可观测性、本地 Studio 和服务器适配器放进同一个框架。2026-01-21 发布 1.0 稳定版，当时每周 npm 下载 30 万+；生产用户举例 Replit、PayPal、Sanity。协议以 Apache-2.0 为主，`ee/` 目录下的企业功能使用 Mastra Enterprise License（开发测试免费，生产需授权）。早期借用 [[entities/vercel-ai-sdk|AI SDK]] 做模型调用，后改为自带模型路由，用 `provider/model` 字符串接入 40+ 厂商。托管部署和观测由商业产品 [[entities/mastra-platform|Mastra Platform]] 提供，但框架可自托管，用 Express、Hono、[[entities/nextjs|Next.js]] 等适配器部署。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架
- **上游依赖**：—（各模型厂商 API、存储与向量库适配器）
- **下游**：[[entities/mastra-code|Mastra Code]]、[[entities/mastra-factory|Mastra Factory]] 都用它构建
- **竞争 / 替代**：[[entities/langchain|LangChain]] / [[entities/langgraph|LangGraph]]（JS 版）、[[entities/vercel-ai-sdk|AI SDK]]（更底层）、[[entities/openai-agents-sdk|OpenAI Agents SDK]]、CrewAI、VoltAgent

## 主要原语

- **Agents**：工具（Zod schema）、结构化输出、人工审批、护栏（提示注入、PII 脱敏、内容审核）、processors
- **Workflows**：类型化多步流程，支持分支、并行、循环、suspend / resume、快照、时间旅行、定时
- **Harness / Agent Controller**：超出单次请求的持久执行；Agent Controller 托管长时、可交互的 Agent 会话（见 [[concepts/agent-harness|Agent Harness]]）
- **Memory**：消息历史、语义召回、working memory、[[concepts/observational-memory|Observational Memory]]
- **Knowledge 与 RAG**：带作用域和权限的托管内容；分块、嵌入、检索、向量库、GraphRAG（见 [[concepts/rag|RAG]]）
- **子 Agent、Skills、Channels、Signals**：委派、可复用能力、消息平台接入、事件流与跨进程信号
- **Sandboxes / Workspaces**：文件系统、搜索、shell、computer use、LSP
- **Connections**：[[concepts/model-context-protocol|MCP]]（可当客户端，也可把 Agent 和工具发布为 MCP 服务器）、A2A、ACP
- **Evals 与 Observability**：scorers（内置、规则、自定义，可接 CI 与 Vitest）、层级追踪、指标，可导出到外部平台
- **Server、Studio、Auth、Voice**：服务器适配器与客户端 SDK、本地可视化调试界面、多种鉴权、语音（STT / TTS / 语音到语音）

## 时间线

- 2025-02 首次在 Hacker News 公开介绍
- 2025-02 至 2026-01 陆续加入原生模型路由（600+ 模型）、护栏、scorers、带单次调用成本的 AI 追踪、memory processors、`.network()` 多 Agent 路由、Express / Hono 适配器；Playground 一度移除，后改名 Studio 回归
- 2026-01-21 1.0 稳定版：每周 npm 下载 30 万+、GitHub 1.94 万星
- 2026-02-09 发布 [[concepts/observational-memory|Observational Memory]]
- 2026-10-06 Agent Controller GA（由 Harness 更名）
- 2026-10-21 `@mastra/mcp` 2.0：只支持 MCP 2026-07-28 规范（无状态，去掉 SSE、roots、sampling）
- 2026-10-23 支持 MCP Events
- 2026-11 GitHub 约 2.93 万星、3100 fork

## 相关实体

- [[entities/mastra-inc|Mastra 公司]]
- [[entities/mastra-platform|Mastra Platform]]
- [[entities/mastra-code|Mastra Code]]
- [[entities/mastra-factory|Mastra Factory]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/observational-memory|Observational Memory]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Mastra is the modern TypeScript framework for AI-powered applications and agents." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
- "Today, we released Mastra 1.0 in stable, so we wanted to come back and talk about what's changed." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
- "It's now Apache 2.0 licensed and runs in prod at companies like Replit, PayPal, and Sanity." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
- "Mastra now supports the MCP 2026-07-28 specification with `@mastra/mcp` ^2.0.0." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
