---
title: LangGraph
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["LangGraph", "LangGraph.js"]
org: "[[entities/langchain-inc]]"
released: "2024"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/langchain-ecosystem-survey-2026-11]]"]
---

# LangGraph

## 描述

[[entities/langchain-inc|LangChain 公司]]的底层 Agent 编排框架，把 Agent 或工作流建模为由节点和边构成的状态图，开源，提供 Python 与 JS 实现。核心能力是持久状态、内置持久化（checkpoint）、可中断恢复的长时运行，以及人工介入（human-in-the-loop）控制。2025-10-22 与 [[entities/langchain|LangChain]] 同日发布 1.0，并成为 LangChain 1.0 `create_agent` 的底层运行时；[[entities/deep-agents|Deep Agents]] 同样运行在它之上。它的托管部署服务原名 LangGraph Platform，2025-10 并入 [[entities/langsmith|LangSmith]]，改称 LangSmith Deployment。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（运行时）
- **下游**：[[entities/langchain|LangChain]]、[[entities/deep-agents|Deep Agents]]
- **竞争 / 替代**：[[entities/workflow-devkit|Workflow DevKit]]（持久化工作流）、CrewAI、Microsoft Agent Framework、OpenAI Agents SDK

## 时间线

- 2024 发布
- 2025-05-14 LangGraph Platform GA（托管长时、有状态 Agent）
- 2025-10 LangGraph Platform 更名 LangSmith Deployment，LangGraph Studio 更名 LangSmith Studio
- 2025-10-22 LangGraph 1.0：唯一明显变更是弃用 `langgraph.prebuilt`，其中的 `create_react_agent` 改由 `langchain.agents.create_agent` 取代；承诺 2.0 前无破坏性变更

## 相关实体

- [[entities/langchain|LangChain]]
- [[entities/deep-agents|Deep Agents]]
- [[entities/langsmith|LangSmith]]
- [[entities/workflow-devkit|Workflow DevKit]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "LangChain agents are built on LangGraph, so you're not locked in." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "These 1.0 releases mark our commitment to stability for our open source libraries and no breaking changes until 2.0." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
