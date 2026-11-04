---
title: L4-开发工具与Agent
type: map
layer: L4
created: 2026-11-04
updated: 2026-11-04
---

# L4-开发工具与Agent

> SDK、Agent 框架、RAG、评测、可观测性、协议

← 返回 [[overview|生态总览]]

## 手工整理

### 框架

- [[entities/langchain|LangChain]]
  - [[entities/langgraph|LangGraph]]
  - [[entities/deep-agents|Deep Agents]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/workflow-devkit|Workflow DevKit]]
- [[entities/mastra|Mastra]]

### Java / JVM

- [[concepts/java-agent-development|Java Agent 开发]]（总览与选型）
- [[entities/spring-ai|Spring AI]]
  - [[entities/embabel|Embabel]]
  - [[entities/spring-ai-alibaba|Spring AI Alibaba]]
- [[entities/langchain4j|LangChain4j]]
- [[entities/google-adk|Google ADK]]
- [[entities/koog|Koog]]
- [[entities/agentscope|AgentScope]]
- [[entities/mcp-java-sdk|MCP Java SDK]]
- [[entities/a2a-java-sdk|A2A Java SDK]]

### 可观测性与平台

- [[entities/langsmith|LangSmith]]
- [[entities/mastra-platform|Mastra Platform]]

### Web 框架与构建工具

- [[entities/nextjs|Next.js]]
- [[entities/turborepo|Turborepo]]

### 概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]
  - [[concepts/agent-harness|Agent Harness]]
  - [[concepts/observational-memory|Observational Memory]]
  - [[concepts/goal-oriented-action-planning|目标导向行动规划（GOAP）]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
  - [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]]
  - [[concepts/multi-round-trip-requests|多轮往返请求（MRTR）]]
  - [[concepts/mcp-extensions|MCP 扩展]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]

## 自动列表（Dataview）

```dataview
TABLE WITHOUT ID file.link AS 条目, kind AS 类型, org AS 所属, released AS 发布, choice(reviewed, "✅", "⏳") AS 已核实
FROM "wiki/entities" OR "wiki/concepts"
WHERE layer = "L4"
SORT kind ASC, file.name ASC
```
