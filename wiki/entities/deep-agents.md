---
title: Deep Agents
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Deep Agents", "deepagents", "Managed Deep Agents"]
org: "[[entities/langchain-inc]]"
released: "2025"
competitors: ["[[entities/claude-code]]"]
depends_on: ["[[entities/langchain]]", "[[entities/langgraph]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/langchain-ecosystem-survey-2026-11]]"]
---

# Deep Agents

## 描述

[[entities/langchain-inc|LangChain 公司]]的开源 [[concepts/agent-harness|Agent harness]]（`deepagents` 包），面向复杂、长时、多步任务，建立在 [[entities/langchain|LangChain]] 与 [[entities/langgraph|LangGraph]] 之上。它把有效 Agent 常见的模式打包成默认能力：任务规划、虚拟文件系统（存放中间文件）、上下文管理、子 Agent 委派、持久记忆、技能加载、敏感操作的人工审批。设计思路与 [[entities/claude-code|Claude Code]] 这类编程 Agent 的 harness 相近。托管版本 Managed Deep Agents 运行在 [[entities/langsmith|LangSmith]] 上，一条命令即可部署。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（harness）
- **上游依赖**：[[entities/langchain|LangChain]]、[[entities/langgraph|LangGraph]]
- **竞争 / 替代**：Claude Agent SDK（[[entities/claude-code|Claude Code]] 的 harness）、OpenAI Agents SDK

## 时间线

- 2025 发布开源 `deepagents`
- 2026-05-14 v0.6：代码解释器式的程序化工具调用、类型化流式输出、React / Vue / Svelte / Angular 前端流式支持、`DeltaChannel`（更省空间的 checkpoint 存储）；同日发布 Managed Deep Agents
- 2026-08 v0.7：简化基础 harness，在相近效果下基础输入 token 减少 65%
- 2026-08-07 Managed Deep Agents 公开测试（LangSmith Cloud 美国区，CLI 优先）
- 2026-09 Managed Deep Agents v0.8：内置 Parallel 网页搜索
- 2026-10 Managed Deep Agents v0.9：按次配置、Slack 集成、用户级记忆与工具、定时任务

## 相关实体

- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]
- [[entities/langsmith|LangSmith]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Deep Agents is the agent harness for complex, multi-step work." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "This release simplifies the base harness, resulting in 65% fewer base input tokens at comparable performance." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "Today, Managed Deep Agents is available in public beta." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
