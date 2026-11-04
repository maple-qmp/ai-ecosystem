---
title: Model Context Protocol（MCP）
type: concept
tags: [standard]
layer: L4
aliases: ["MCP", "模型上下文协议"]
current_version: "2026-07-28"
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[sources/mcp-spec-2026-07-28]]"
  - "[[sources/mastra-ecosystem-survey-2026-11]]"
  - "[[sources/java-agent-ecosystem-survey-2026-11]]"
---

# Model Context Protocol（MCP）

## 定义

[[entities/anthropic|Anthropic]] 于 2024-11 发布的开放协议，基于 JSON-RPC 2.0，统一 AI 应用连接外部工具和数据源的方式，常被比作“AI 的 USB-C”。2025 年起被 OpenAI、Google、Microsoft 等广泛采用。当前协议版本是 **2026-07-28**，从这一版开始 MCP 是**无状态协议**：每个请求都是自包含的。完整流程见 [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]]。

## 关键特征

- **Host—Client—Server 架构**：一个宿主（Host，如 IDE 或桌面助手）管理多个客户端，每个客户端只连一个服务器；服务器看不到完整对话，也看不到其他服务器
- **三类服务端原语**：Tools（模型调用的函数）、Resources（可读取的上下文数据）、Prompts（用户触发的模板）
- **客户端提供的能力**：Elicitation（向用户索取输入）、Sampling 与 Roots（已弃用），通过 [[concepts/multi-round-trip-requests|MRTR]] 交付
- **两种传输**：stdio（本地子进程）和 Streamable HTTP（远程）
- **授权**：远程服务器使用 OAuth 2.1，MCP 服务器作为资源服务器
- **扩展机制**：Tasks、Apps、Skills 等以官方扩展形式演进，见 [[concepts/mcp-extensions|MCP 扩展]]
- **版本号**：格式为 `YYYY-MM-DD`，表示最后一次不兼容变更的日期

## 版本演进

| 版本 | 要点 |
|---|---|
| 2024-11-05 | 首个公开版本，HTTP+SSE 传输 |
| 2025-03-26 | 引入 Streamable HTTP 和 OAuth 2.1 授权，HTTP+SSE 进入弃用 |
| 2025-06-18 | 结构化工具输出、Elicitation、资源链接，移除 JSON-RPC 批处理 |
| 2025-11-25 | 实验性 Tasks、URL 模式 Elicitation、CIMD 客户端注册 |
| **2026-07-28** | **无状态化**：去掉握手和会话，新增 `server/discover`、MRTR、`subscriptions/listen`，Tasks 移为扩展，弃用 Roots / Sampling / Logging，建立特性生命周期政策 |

## 应用

- 给 [[concepts/ai-agent|Agent]] 接入工具与数据
- IDE、桌面助手、编程工具的扩展生态（如 [[entities/claude-code|Claude Code]]）
- 企业网关：统一做鉴权、路由与审计（2026-07-28 的请求头和缓存提示就是为此设计的）
- Agent 框架内置：[[entities/mastra|Mastra]] 的 `@mastra/mcp` 2.0（2026-10-21）只接受 2026-07-28 客户端，去掉 SSE 传输、roots、sampling，暂不支持 tasks
- Java 生态：官方 [[entities/mcp-java-sdk|MCP Java SDK]] 与 [[entities/spring-ai|Spring AI]] 团队合作维护；2.0.0（随 Spring AI 2.0，2026-06）对应 2025-11-25 规范，截至 2026-11 尚未支持 2026-07-28 规范（见 [[concepts/java-agent-development|Java Agent 开发]]）

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- **竞争 / 互补**：与各家模型厂商私有的工具调用（function calling）格式互补；MCP 统一的是“工具从哪来”，不是模型 API

## 相关概念

- [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]]
- [[concepts/multi-round-trip-requests|多轮往返请求（MRTR）]]
- [[concepts/mcp-extensions|MCP 扩展]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/mastra|Mastra]]
- [[entities/mcp-java-sdk|MCP Java SDK]]

## 我的判断

## 来源摘录

- "MCP is a stateless protocol: every request is self-contained and carries its own protocol version and capabilities." — [[sources/mcp-spec-2026-07-28|MCP 规范 2026-07-28]]
- "The new spec removes server sessions, so every request is self-contained." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
