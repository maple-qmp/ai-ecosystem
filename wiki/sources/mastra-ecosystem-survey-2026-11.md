---
title: Mastra 生态深度调研（2026-11）
type: source
tags: [notes]
source_note: "[[Mastra生态深度调研-2026-11]]"
url: https://github.com/mastra-ai/mastra
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[entities/mastra]]"
  - "[[entities/mastra-inc]]"
  - "[[entities/mastra-platform]]"
  - "[[entities/mastra-code]]"
  - "[[entities/mastra-factory]]"
  - "[[concepts/observational-memory]]"
  - "[[concepts/agent-harness]]"
  - "[[concepts/model-context-protocol]]"
---

# Mastra 生态深度调研（2026-11）

## Summary

梳理 [[entities/mastra-inc|Mastra 公司]]的产品结构。开源侧是 TypeScript Agent 框架 [[entities/mastra|Mastra]]，把 Agent、工作流、记忆、RAG、评测、可观测性、Studio 和服务器适配放进一个框架，2026-01-21 发布 1.0。它的记忆方案 [[concepts/observational-memory|Observational Memory]] 用后台 Agent 把对话压缩成观察日志，取代检索和上下文压缩。商业侧是 2026-04 推出的托管平台 [[entities/mastra-platform|Mastra Platform]]（部署、观测、Studio，积分制计费）。公司还用自家框架做了两款应用：终端编程 Agent [[entities/mastra-code|Mastra Code]] 和软件交付环境 [[entities/mastra-factory|Mastra Factory]]。公司由 Gatsby 原班人马创办，累计融资 3500 万美元。

## Key Points

- **1.0 稳定版**（2026-01-21）：Apache-2.0；当时每周 npm 下载 30 万+、1.94 万星；生产用户含 Replit、PayPal、Sanity
- **模型路由**：早期借用 [[entities/vercel-ai-sdk|AI SDK]]，后改为自带路由，40+ 厂商
- **框架原语**：Agents、Workflows（suspend / resume、时间旅行）、Harness / Agent Controller、Memory、Knowledge、Evals（scorers）、Observability、Studio、Server 适配器、Sandboxes / Workspaces、Voice
- **Agent Controller**（2026-10-06 GA）：长时可交互 Agent 会话运行时，由 Harness 更名而来，最初为 Mastra Code 而建
- **MCP**：`@mastra/mcp` 2.0（2026-10-21）只支持 [[concepts/model-context-protocol|MCP]] 2026-07-28 无状态规范
- **协议**：主体 Apache-2.0，`ee/` 目录为 Mastra Enterprise License
- **平台计费**：Starter 免费按量、Team 250 美元 / 月、Enterprise 定制，费用统一走积分池（含模型 token）
- **融资**：种子轮 1300 万美元（2025-10-08，YC、Gradient 等）→ A 轮 2200 万美元（2026-04-09，Spark Capital 领投），累计 3500 万美元

## Mentioned Pages

- [[entities/mastra-inc|Mastra 公司]]
- [[entities/mastra|Mastra]]
- [[entities/mastra-platform|Mastra Platform]]
- [[entities/mastra-code|Mastra Code]]
- [[entities/mastra-factory|Mastra Factory]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]
- [[entities/langsmith|LangSmith]]
- [[entities/claude-code|Claude Code]]
- [[concepts/observational-memory|Observational Memory]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]
