---
title: Python Agent 框架调研（2026-11）
type: source
tags: [notes]
source_note: "[[Python-Agent框架调研-2026-11]]"
url: https://devblogs.microsoft.com/agent-framework/microsoft-agent-framework-version-1-0/
created: 2026-11-06
updated: 2026-11-06
sources:
  - "[[concepts/python-agent-development]]"
  - "[[entities/microsoft-agent-framework]]"
  - "[[entities/crewai]]"
  - "[[entities/llamaindex]]"
  - "[[entities/pydantic-ai]]"
  - "[[entities/dspy]]"
  - "[[entities/smolagents]]"
  - "[[entities/agno]]"
  - "[[entities/langgraph]]"
  - "[[entities/google-adk]]"
---

# Python Agent 框架调研（2026-11）

## Summary

梳理 Python 上开发 AI Agent 的主要框架，总结见 [[concepts/python-agent-development|Python Agent 开发]]。可分四类：大厂全家桶（[[entities/microsoft-agent-framework|Microsoft Agent Framework]]、[[entities/google-adk|Google ADK]]、[[entities/openai-agents-sdk|OpenAI Agents SDK]]）、独立通用框架（[[entities/langgraph|LangGraph]]、[[entities/crewai|CrewAI]]、[[entities/pydantic-ai|Pydantic AI]]、[[entities/agno|Agno]]）、文档中心框架（[[entities/llamaindex|LlamaIndex]]）、研究取向或极简框架（[[entities/dspy|DSPy]]、[[entities/smolagents|smolagents]]）。2025 下半年到 2026 年主要框架都进入 1.0 以上，共同趋势是图式工作流和 Harness 化。版本号核对自 PyPI，星数和协议来自 GitHub API（2026-11-06）。

## Key Points

- **Microsoft Agent Framework 1.0**（2026-04-03）：合并 Semantic Kernel 与 AutoGen，支持 .NET 与 Python；图式工作流稳定，DevUI、Agent Harness 仍为预览；AutoGen 仓库已归档；最新 1.24.0
- **CrewAI**：独立于 LangChain，Crews（自主协作）+ Flows（事件驱动控制）；1.0 于 2025-10，最新 1.15.35；商业版 CrewAI AMP Suite
- **LlamaIndex**：重心转向 LlamaParse 文档平台，LlamaCloud 2026-02 改名 LlamaParse；Agent Workflows 拆到 llama-agents 仓库，最新 2.26.1；主包仍在 0.14.x
- **Pydantic AI V2**（2026-06-23）：capability 成为核心组合单元，新增 Pydantic AI Harness；`openai:` 默认走 Responses API；最新 2.66.0
- **DSPy**：“编程而非提示”，用优化器（GEPA 等）自动优化提示与权重；3.0 于 2025-08，2026 年发布 3.2–3.4，已与 LiteLLM 解耦
- **smolagents**（[[entities/hugging-face|Hugging Face]]）：CodeAgent 把动作写成 Python 代码；1.26.0（2026-05-29）后没有新版本
- **Agno**：从框架扩展为自管理 Agent 平台 AgentOS，可用 Agno、[[entities/claude-agent-sdk|Claude Agent SDK]] 或 Codex SDK 构建 Agent；最新 3.1.12
- **Google ADK Python 2.0**（2026-05-19）：改为图式 Workflow Runtime，新增 Task API；最新 2.13.0
- **LangGraph**：PyPI 上 1.0.0 于 2025-10-17，最新 1.2.20

## Mentioned Pages

- [[concepts/python-agent-development|Python Agent 开发]]
- [[entities/microsoft-agent-framework|Microsoft Agent Framework]]
- [[entities/crewai|CrewAI]]
- [[entities/llamaindex|LlamaIndex]]
- [[entities/pydantic-ai|Pydantic AI]]
- [[entities/dspy|DSPy]]
- [[entities/smolagents|smolagents]]
- [[entities/agno|Agno]]
- [[entities/langgraph|LangGraph]]
- [[entities/google-adk|Google ADK]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/microsoft|Microsoft]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/java-agent-development|Java Agent 开发]]
