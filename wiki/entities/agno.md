---
title: Agno
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Agno", "AgentOS", "Phidata"]
released: "2025-01"
competitors: ["[[entities/crewai]]", "[[entities/langgraph]]", "[[entities/pydantic-ai]]", "[[entities/mastra]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# Agno

## 描述

开源的 Python Agent 框架与平台（Apache-2.0，GitHub 约 4.31 万星）。2026 年它的定位从框架扩展为“自管理 Agent 平台”：可以用 Agno 自己的 SDK、[[entities/claude-agent-sdk|Claude Agent SDK]] 或 Codex SDK 构建 Agent，组合成 teams 与 workflows；AgentOS 把 Agent 作为持久服务运行，自带 REST API 和 MCP 服务器、鉴权、基于角色的权限、恢复与重放、人工审批、调度和持久执行；Company OS 让 Agent 承担职责、处理项目任务和例行工作。平台部署在用户自己的云上，数据存在 PostgreSQL。PyPI 上 1.0 于 2025-01、2.0 于 2025-09 发布，到 2026-10-29 已是 3.1.12。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架 / 平台（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（各模型厂商 API，可包装 Claude Agent SDK、Codex SDK）
- **竞争 / 替代**：[[entities/crewai|CrewAI]]、[[entities/langgraph|LangGraph]]、[[entities/pydantic-ai|Pydantic AI]]、[[entities/mastra|Mastra]]（TypeScript）

## 时间线

- 2022-05 仓库创建（前身 Phidata，改名说法未经一手核实）
- 2025-01-30 agno 1.0.0
- 2025-09-09 2.0.0
- 2026-10-29 3.1.12（PyPI）

## 相关实体

- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/codex-app-server|Codex App Server / SDK]]
- [[entities/mastra|Mastra]]

## 相关概念

- [[concepts/python-agent-development|Python Agent 开发]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Agno is a self-managing agent platform. Build agents for your company, product, or customers. Run them as durable services on AgentOS." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
