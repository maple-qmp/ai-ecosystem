---
title: CrewAI
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["CrewAI", "crewai", "CrewAI AMP"]
released: "2023-11"
competitors: ["[[entities/langgraph]]", "[[entities/microsoft-agent-framework]]", "[[entities/agno]]", "[[entities/pydantic-ai]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# CrewAI

## 描述

CrewAI Inc. 开源的 Python 多 Agent 框架（MIT，GitHub 约 6.06 万星），不依赖 [[entities/langchain|LangChain]]，自带 agents、tasks、crews、flows、tools 等原语。它有两种互补的模式：Crews 让多个角色化 Agent 自主协作完成任务，Flows 提供事件驱动的精确控制，可以在流程里嵌入单次 LLM 调用或整个 Crew。2025-10 发布 1.0，2026 年保持高频小版本（到 2026-11 已是 1.15.35），加入了会话式 Flow 的 chat API 和可插拔的 Flow 后端。商业产品 CrewAI AMP Suite 提供托管部署、可观测性、治理和企业支持，平台 Studio 自 2026-07 起支持无代码 Flows。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（各模型厂商 API）
- **竞争 / 替代**：[[entities/langgraph|LangGraph]]、[[entities/microsoft-agent-framework|Microsoft Agent Framework]]、[[entities/agno|Agno]]、[[entities/pydantic-ai|Pydantic AI]]

## 时间线

- 2023-11-14 crewai 0.1.0 上传 PyPI
- 2025-10-20 1.0.0
- 2026-06 前后 会话式 Flow 的 chat API、可插拔 Flow 后端（更新日志）
- 2026-07 平台 Studio 开始推出无代码 Flows
- 2026-11-03 1.15.35（PyPI）

## 相关实体

- [[entities/langgraph|LangGraph]]
- [[entities/langchain|LangChain]]
- [[entities/microsoft-agent-framework|Microsoft Agent Framework]]

## 相关概念

- [[concepts/python-agent-development|Python Agent 开发]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "It gives developers autonomous agent collaboration through Crews and precise, event-driven control through Flows." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "CrewAI is a standalone Python framework with its own primitives for agents, tasks, crews, flows, tools, and orchestration." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
