---
title: LangChain
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["LangChain", "LangChain.js", "langchain"]
org: "[[entities/langchain-inc]]"
released: "2022-10"
competitors: ["[[entities/vercel-ai-sdk]]"]
depends_on: ["[[entities/langgraph]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/langchain-ecosystem-survey-2026-11]]"]
---

# LangChain

## 描述

[[entities/langchain-inc|LangChain 公司]]维护的开源 LLM 应用与 Agent 开发框架，MIT 协议，有 Python 和 JavaScript/TypeScript（LangChain.js）两个实现，GitHub 主仓库约 14.9 万星。2022-10 由 Harrison Chase 发布，早期以“链”（chain）、提示模板、文档加载器和 [[concepts/rag|RAG]] 组件闻名，2023 年推出声明式组合语法 LCEL。2025-10-22 发布 1.0，定位改为构建在 [[entities/langgraph|LangGraph]] 运行时之上的高层 Agent API：核心是 `create_agent` 和中间件。模型、嵌入、工具、[[concepts/vector-database|向量库]]等集成以独立包发布（如 `langchain-openai`、`langchain-anthropic`），可接入 [[entities/gpt|GPT]]、[[entities/claude|Claude]] 等模型。

## 1.0 的主要变化

- **`create_agent`**：标准的“模型 + 工具”循环，底层由 LangGraph 运行，取代 `langgraph.prebuilt` 里的 `create_react_agent`
- **中间件（middleware）**：在 Agent 循环的每一步（调用模型前后、调用工具前后）挂钩子；内置人工审批、对话摘要、PII 脱敏，也可自定义
- **标准内容块（standard content blocks）**：跨厂商统一推理过程、引用、工具调用等输出格式
- **瘦身**：链、旧 Agent 等遗留功能移入 `langchain-classic`；要求 Python 3.10+
- **稳定性承诺**：2.0 之前无破坏性变更

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架
- **上游依赖**：[[entities/langgraph|LangGraph]]（1.0 起 Agent 运行时）、各模型厂商 API
- **下游**：[[entities/deep-agents|Deep Agents]] 建立在 LangChain 之上；追踪与评测通常接 [[entities/langsmith|LangSmith]]
- **竞争 / 替代**：[[entities/vercel-ai-sdk|AI SDK]]、LlamaIndex、CrewAI、OpenAI Agents SDK、Mastra

## 时间线

- 2022-10 Harrison Chase 以开源项目形式发布
- 2023-04 成立公司（见 [[entities/langchain-inc|LangChain 公司]]）
- 2023 Q3 推出 LCEL（LangChain Expression Language）
- 2023-10 推出 LangServe，把 LCEL 链部署为 API
- 2024 推出 [[entities/langgraph|LangGraph]]
- 2025-10-22 LangChain 1.0 与 LangGraph 1.0 同日发布
- 2026-10 v1.4.0 通过 `langchain.mcp` 命名空间支持 FastMCP（[[concepts/model-context-protocol|MCP]]）

## 相关实体

- [[entities/langchain-inc|LangChain 公司]]
- [[entities/langgraph|LangGraph]]
- [[entities/deep-agents|Deep Agents]]
- [[entities/langsmith|LangSmith]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/claude|Claude]]
- [[entities/gpt|GPT]]

## 相关概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/vector-database|向量数据库]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The new `create_agent` function uses LangGraph under the hood to run this loop." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "Middleware defines a set of hooks that allow you to customize behavior in the agent loop" — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "Legacy functionality moves to `langchain-classic` for backwards compatibility." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "LangChain now supports FastMCP through the `langchain.mcp` namespace." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
