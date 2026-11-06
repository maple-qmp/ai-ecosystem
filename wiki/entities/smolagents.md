---
title: smolagents
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["smolagents", "CodeAgent"]
org: "[[entities/hugging-face]]"
released: "2024-12"
competitors: ["[[entities/pydantic-ai]]", "[[entities/openai-agents-sdk]]", "[[entities/langgraph]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# smolagents

## 描述

[[entities/hugging-face|Hugging Face]] 开源的极简 Python Agent 库（Apache-2.0，GitHub 约 3.02 万星），Agent 核心逻辑约 1000 行。它的特色是 CodeAgent：LLM 把每一步动作写成 Python 代码片段，而不是输出工具调用 JSON，README 引用的论文称这样能少用约 30% 的步骤；代码可以放在沙箱里执行。模型、模态、工具都不绑定：可以用本地 transformers 或 [[entities/ollama|Ollama]] 模型、Hub 推理服务或 LiteLLM，工具可以来自 [[concepts/model-context-protocol|MCP]] 服务器、[[entities/langchain|LangChain]] 或 Hub Space。2024-12-31 发布 1.0；2026-05 的 1.25.0 修补了远程执行器漏洞，1.26.0（2026-05-29）移除远程 WasmExecutor，此后到 2026-11 没有新版本。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（Hugging Face Hub、各模型 API）
- **竞争 / 替代**：[[entities/pydantic-ai|Pydantic AI]]、[[entities/openai-agents-sdk|OpenAI Agents SDK]]、[[entities/langgraph|LangGraph]]

## 时间线

- 2024-12 仓库创建，2024-12-27 0.1.0
- 2024-12-31 1.0.0
- 2026-05 1.25.0：修补远程执行器漏洞，去掉 pickle 支持
- 2026-05-29 1.26.0：移除远程 WasmExecutor，WebSearchTool 支持 Exa

## 相关实体

- [[entities/hugging-face|Hugging Face]]
- [[entities/ollama|Ollama]]

## 相关概念

- [[concepts/python-agent-development|Python Agent 开发]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "`smolagents` is a library that enables you to run powerful agents in a few lines of code." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "Our `CodeAgent` works mostly like classical ReAct agents - the exception being that the LLM engine writes its actions as Python code snippets." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
