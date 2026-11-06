---
title: Microsoft Agent Framework
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Microsoft Agent Framework", "MAF", "agent-framework", "AutoGen", "Semantic Kernel"]
org: "[[entities/microsoft]]"
released: "2025-10"
competitors: ["[[entities/langgraph]]", "[[entities/crewai]]", "[[entities/google-adk]]", "[[entities/openai-agents-sdk]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# Microsoft Agent Framework

## 描述

[[entities/microsoft|Microsoft]] 开源的多语言 Agent 框架（MIT，GitHub 约 1.46 万星），由 Semantic Kernel 的企业级基础（连接器、中间件、过滤器）和 AutoGen 的多 Agent 编排模式合并而成，支持 .NET 与 Python，Go 版放在单独仓库。1.0 于 2026-04-03 发布，稳定部分包括单 Agent 抽象、对 Foundry、Azure OpenAI、OpenAI、Anthropic、Amazon Bedrock、Gemini、Ollama 的一方连接器、中间件、可插拔记忆、带检查点的图式工作流，以及顺序、并发、handoff、群聊、Magentic-One 五种多 Agent 编排。DevUI 本地调试器、Foundry 托管 Agent、AG-UI 适配器、Skills 和 Agent Harness 仍为预览。它支持 [[concepts/model-context-protocol|MCP]] 和 [[concepts/agent2agent-protocol|A2A]]，但 A2A 1.0 支持尚未完成。前身 AutoGen 的仓库已归档、不再维护；Semantic Kernel 仍在发布，官方建议新项目改用本框架。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（各模型厂商 API，与 [[entities/azure|Azure]] / Microsoft Foundry 深度集成）
- **竞争 / 替代**：[[entities/langgraph|LangGraph]]、[[entities/crewai|CrewAI]]、[[entities/google-adk|Google ADK]]、[[entities/openai-agents-sdk|OpenAI Agents SDK]]

## 时间线

- 2023 Semantic Kernel、AutoGen 先后开源
- 2025-01-09 autogen-agentchat 0.4.0（AutoGen 重写版）
- 2025-09-30 autogen-agentchat 0.7.5，AutoGen 的最后一个版本
- 2025-10-01 agent-framework 首个 beta 上传 PyPI
- 2026-04-03 1.0 正式版（.NET 与 Python），PyPI 1.0.0 上传于 2026-04-02
- 2026-10-30 1.24.0（PyPI）
- 2026-11-05 Semantic Kernel Python 1.47.0，仍在维护

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/azure|Azure]]
- [[entities/chatkit|ChatKit]]（AG-UI 适配器之一）
- [[entities/claude-agent-sdk|Claude Agent SDK]]（预览版 harness 之一）
- [[entities/github-copilot|GitHub Copilot]]

## 相关概念

- [[concepts/python-agent-development|Python Agent 开发]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "This is the production-ready release: stable APIs, and a commitment to long-term support." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "The graph-based workflow engine for composing agents and functions into deterministic, repeatable processes is now stable." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "Microsoft Agent Framework (MAF) is the enterprise‑ready successor to AutoGen." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
