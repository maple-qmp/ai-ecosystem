---
title: AI SDK
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["AI SDK", "Vercel AI SDK"]
org: "[[entities/vercel]]"
released: "2023-06"
competitors: ["[[entities/langchain]]", "[[entities/mastra]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/vercel-oss-dependency-survey-2026-11]]", "[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# AI SDK

## 描述

[[entities/vercel|Vercel]] 维护的 TypeScript LLM 开发库（npm 包 `ai`），Apache-2.0 协议。核心层（AI SDK Core）统一了文本生成、结构化输出、工具调用、流式和 Agent 循环的接口，通过 `@ai-sdk/*` provider 包对接 [[entities/openai|OpenAI]]、[[entities/anthropic|Anthropic]]、Google 等模型厂商；UI 层提供 React、Vue、Svelte、Angular 的聊天 hooks。代码本身可在任何 Node / 边缘运行时使用，不需要部署在 Vercel。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架
- **上游依赖**：—（各模型厂商 API）
- **竞争 / 替代**：[[entities/langchain|LangChain]]、[[entities/mastra|Mastra]]（早期借用 AI SDK 做模型调用，后改为自带模型路由）、OpenAI Agents SDK

## 脱离 Vercel 使用

唯一的默认绑定：AI Gateway 是默认全局 provider，`"openai/gpt-…"` 这类 `creator/model-name` 字符串会自动经 Vercel AI Gateway 转发，并需要 Gateway 的 API key。脱离方式有两种：

- 直接传 provider 实例，例如 `openai('…')`（来自 `@ai-sdk/openai`）
- 给 `globalThis.AI_SDK_DEFAULT_PROVIDER` 赋值其他 provider（常放在 `instrumentation.ts` 的 `register()` 里），让字符串写法改走自选厂商

`@ai-sdk/gateway` 包本身是 Vercel 服务客户端。OpenAI 兼容接口（如自建 [[entities/vllm|vLLM]]）可通过 `@ai-sdk/openai-compatible` 接入。

## 时间线

- 2023-06 发布
- 2025 AI SDK 5，引入 AI Gateway 作为默认全局 provider
- 2025 AI SDK 6，加入 Agent 抽象

## 相关实体

- [[entities/vercel|Vercel]]
- [[entities/nextjs|Next.js]]
- [[entities/workflow-devkit|Workflow DevKit]]
- [[entities/langchain|LangChain]]
- [[entities/mastra|Mastra]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

