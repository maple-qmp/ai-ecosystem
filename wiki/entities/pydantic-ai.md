---
title: Pydantic AI
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Pydantic AI", "pydantic-ai", "Pydantic AI Harness"]
released: "2024-05"
competitors: ["[[entities/openai-agents-sdk]]", "[[entities/langgraph]]", "[[entities/crewai]]", "[[entities/agno]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# Pydantic AI

## 描述

Pydantic 团队开源的 Python Agent 框架（MIT，GitHub 约 2.10 万星），自称“Python AI SDK”：提供类型化、可扩展的 Agent 循环，模型用字符串切换并可设置回退模型。配套产品有 Pydantic Evals（评测最终输出和工具调用轨迹）、Pydantic Graph、Pydantic Logfire（可观测性）和 Pydantic AI Gateway。V1 于 2025-09 发布，带 API 稳定承诺、工具调用人工审批和基于 Temporal 的持久执行。V2 于 2026-06-23 发布，核心组合单元改为 capability（打包指令、工具、生命周期钩子和模型设置，可序列化），并把记忆、护栏、上下文管理、文件系统、shell、Code Mode 等放进独立包 Pydantic AI Harness，见 [[concepts/agent-harness|Agent Harness]]。V2 的 `openai:` 前缀默认走 Responses API，Bedrock、Groq、Mistral 等提供方改为可选安装。发布节奏很快，到 2026-11-04 已是 2.66.0。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（各模型厂商 API）
- **竞争 / 替代**：[[entities/openai-agents-sdk|OpenAI Agents SDK]]、[[entities/langgraph|LangGraph]]、[[entities/crewai|CrewAI]]、[[entities/agno|Agno]]

## 时间线

- 2024-05 PyPI 占位包；2024-06 仓库创建
- 2025-09-05 1.0.0：API 稳定承诺、人工审批、Temporal 持久执行
- 2026-06-23 2.0.0：capability 与 Pydantic AI Harness；大版本间无破坏窗口从 6 个月缩短到 3 个月
- 2026-11-04 2.66.0（PyPI）

## 相关实体

- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/langgraph|LangGraph]]

## 相关概念

- [[concepts/python-agent-development|Python Agent 开发]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "How Python does AI. Agents, realtime voice, image generation, embeddings. Every model, every interface, typed end to end." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "Pydantic AI v2 is here, and your agents have never been more capable." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
