---
title: L4-开发工具与Agent
type: map
layer: L4
created: 2026-11-04
updated: 2026-11-07
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
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/chatkit|ChatKit]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/deepseek-harness|DeepSeek Harness]]
- [[concepts/agent-framework-selection|AI Agent 框架选型]]（8 个框架横向比较与选型建议）

### 编码 Agent

- [[entities/codex-cli|Codex CLI]]
  - [[entities/codex-app-server|Codex App Server / SDK]]
- [[entities/claude-code|Claude Code]]
  - [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/opencode|OpenCode]]
- [[entities/pi-agent|Pi]]

### 常驻自主助理

- [[entities/openclaw|OpenClaw]]
- [[entities/hermes-agent|Hermes Agent]]
- [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]

### Python

- [[concepts/python-agent-development|Python Agent 开发]]（总览与选型）
- [[entities/microsoft-agent-framework|Microsoft Agent Framework]]（含 AutoGen、Semantic Kernel）
- [[entities/crewai|CrewAI]]
- [[entities/llamaindex|LlamaIndex]]
- [[entities/pydantic-ai|Pydantic AI]]
- [[entities/dspy|DSPy]]
- [[entities/smolagents|smolagents]]
- [[entities/agno|Agno]]
- LangGraph、Google ADK、OpenAI Agents SDK 的 Python 版见上方「框架」与下方「Java / JVM」

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

### 低代码 Agent 平台与 LLM 网关

- [[entities/dify|Dify]]
- [[entities/coze|Coze / 扣子]]（含开源 Coze Studio、Coze Loop）
- [[entities/n8n|n8n]]
- [[entities/litellm|LiteLLM]]（LLM 网关）
- [[concepts/computer-use|Computer Use]]
- [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台与 LLM 网关调研]]

### 可观测性与平台

- [[entities/langsmith|LangSmith]]
- [[entities/mastra-platform|Mastra Platform]]
- [[entities/promptfoo|Promptfoo]]（评测与红队）

### Web 框架与构建工具

- [[entities/nextjs|Next.js]]
- [[entities/turborepo|Turborepo]]

### 运行时

- [[concepts/javascript-runtime|JavaScript 运行时]]
- [[entities/bun|Bun]]

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
  - [[concepts/mcp-bundles|MCP Bundles（MCPB）]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/agentic-commerce-protocol|Agentic Commerce Protocol（ACP）]]
- [[concepts/agents-md|AGENTS.md]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/agent-driven-code-migration|Agent 驱动的代码迁移]]

### 上下文、记忆与应用评测专题

- [[concepts/context-engineering|上下文工程]]
- [[concepts/agent-memory|Agent 记忆]]
- [[concepts/context-compaction|上下文压缩]]
- [[concepts/ai-application-evaluation|AI 应用评测]]
- [[concepts/llm-as-judge|LLM 裁判]]
- [[concepts/llm-observability|LLM 可观测性]]
- [[entities/langfuse|Langfuse]]
- [[entities/arize-phoenix|Arize Phoenix]]
- [[concepts/longmemeval|LongMemEval]]（跨层参考）
- [[sources/context-memory-survey-2026-11|上下文工程与记忆专题调研]]
- [[sources/ai-evaluation-observability-survey-2026-11|应用评测与可观测性专题调研]]

## 自动列表（Dataview）

```dataview
TABLE WITHOUT ID file.link AS 条目, kind AS 类型, org AS 所属, released AS 发布, choice(reviewed, "✅", "⏳") AS 已核实
FROM "wiki/entities" OR "wiki/concepts"
WHERE layer = "L4"
SORT kind ASC, file.name ASC
```
