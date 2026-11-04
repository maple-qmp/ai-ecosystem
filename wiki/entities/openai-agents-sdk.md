---
title: OpenAI Agents SDK
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["OpenAI Agents SDK", "Agents SDK", "openai-agents"]
org: "[[entities/openai]]"
released: "2025-03"
competitors: ["[[entities/langgraph]]", "[[entities/vercel-ai-sdk]]", "[[entities/mastra]]", "[[entities/google-adk]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# OpenAI Agents SDK

## 描述

[[entities/openai|OpenAI]] 开源的轻量 [[concepts/ai-agent|AI Agent]] 框架，有 Python（`openai-agents`）和 TypeScript（`@openai/agents`）两个版本，均为 MIT 协议，前身是教学项目 Swarm。核心原语是 Agent、工具、Handoff（把对话交给另一个 Agent）、Guardrail 和 Session，外加流式输出、人工审批、语音 Agent 和追踪。2026 年加入沙箱 Agent，给模型一个可读写文件、执行命令的持久工作区。官方的区分是：Agents SDK 跑在你的应用里，Agents API 是 OpenAI 云端托管的 harness。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架
- **上游依赖**：—（默认调 OpenAI Responses API，可换）
- **竞争 / 替代**：[[entities/langgraph|LangGraph]]、[[entities/vercel-ai-sdk|AI SDK]]、[[entities/mastra|Mastra]]、[[entities/google-adk|Google ADK]]、[[entities/deep-agents|Deep Agents]]

## 脱离 OpenAI 使用

可以脱离，但有两处默认值要改，且一部分能力会丢。

- **换模型**：有 OpenAI 兼容端点的服务，用 `set_default_openai_client` 全局替换客户端；不支持 Responses API 的服务改用 `OpenAIChatCompletionsModel`；按运行切换用自定义 `ModelProvider`；也可装 `openai-agents[litellm]` 或 `openai-agents[any-llm]` 接上百家模型（官方标注 beta、尽力支持）。本地可接 [[entities/gpt-oss|gpt-oss]]
- **关追踪**：追踪默认上传到 OpenAI，没有 OpenAI key 会报 401。用 `set_tracing_disabled(True)`、环境变量 `OPENAI_AGENTS_DISABLE_TRACING=1` 或 `RunConfig.tracing_disabled` 关掉；或用 `set_trace_processors()` 替换成 Langfuse、Logfire、[[entities/langsmith|LangSmith]]、Arize Phoenix、Braintrust、Datadog 等 30 多种处理器
- **会丢的能力**：WebSearchTool、FileSearchTool、CodeInterpreterTool、HostedMCPTool、ImageGenerationTool 等托管工具只在 OpenAI 的 Responses 模型上可用；需要自己用函数工具或本地 MCP 服务器替代
- **沙箱**：`UnixLocalSandboxClient`（本地，Linux 上不做系统级隔离）和 Docker 不依赖任何云；另有 E2B、Modal、Daytona、Cloudflare、Vercel、Runloop、Blaxel 等第三方沙箱扩展
- **会话与持久化**：Redis、SQLAlchemy、MongoDB、Dapr、S3、加密会话；`temporal` 扩展做持久执行

## 时间线

- 2024-10 发布教学项目 Swarm
- 2025-03 发布 Agents SDK（Python），取代 Swarm
- 2025-05 发布 TypeScript 版
- 2025-10 ChatKit 发布，官方推荐用 Agents SDK 实现其自托管后端
- 2026-10 Python v0.24.0、TypeScript 0.21.0

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/chatkit|ChatKit]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/langsmith|LangSmith]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Agents SDK runs in your application; the Agents API runs a managed harness in OpenAI's service." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
- "LiteLLM support is included on a best-effort, beta basis." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
- "You can globally disable tracing by setting the env var `OPENAI_AGENTS_DISABLE_TRACING=1`" — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
