---
title: Agent Harness
type: concept
tags: [term]
layer: L4
aliases: ["Agent Harness", "Agent 运行框架", "harness"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/langchain-ecosystem-survey-2026-11]]", "[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# Agent Harness

## 定义

包裹在模型外面、让 [[concepts/ai-agent|AI Agent]] 能完成长时多步任务的一整套默认运行环境：工具调用循环之外，还预置规划、文件、上下文管理、子 Agent 和记忆等能力。它比“编排框架”高一层：编排框架提供搭积木的原语，harness 提供已经搭好、可直接用的 Agent。

## 关键特征

- **任务规划**：先拆解成待办列表，再逐项执行
- **文件系统**：中间结果写入文件，不全塞进上下文
- **上下文管理**：对话过长时摘要、裁剪
- **子 Agent 委派**：把子任务交给隔离上下文的子 Agent
- **技能与记忆**：按需加载技能文件（如 AGENTS.md、skills），跨会话保存记忆
- **人工审批**：敏感操作前暂停，等人确认

## 应用

- 编程 Agent（[[entities/claude-code|Claude Code]]、[[entities/mastra-code|Mastra Code]] 等）
- 深度研究、长时自动化任务

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 以 LangChain 生态为例，从低到高是三层：[[entities/langgraph|LangGraph]]（编排运行时）→ [[entities/langchain|LangChain]]（Agent API 与中间件）→ [[entities/deep-agents|Deep Agents]]（harness）
- [[entities/mastra|Mastra]] 把 harness 作为框架内的一个模块：Harness 负责超出单次请求的持久执行（目标、定时、后台任务），其中托管长时可交互会话的部分 2026-10 以 Agent Controller 名义 GA（由 Harness 更名）；上下文管理则用 [[concepts/observational-memory|Observational Memory]] 取代压缩

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/observational-memory|Observational Memory]]

## 相关实体

- [[entities/deep-agents|Deep Agents]]
- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]
- [[entities/claude-code|Claude Code]]
- [[entities/mastra|Mastra]]
- [[entities/mastra-code|Mastra Code]]

## 我的判断

## 来源摘录

- "Deep Agents is the agent harness for complex, multi-step work." — [[sources/langchain-ecosystem-survey-2026-11|LangChain 生态深度调研]]
- "Each user gets a session with its own threads, mode, model, approvals, memory and subagents." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
