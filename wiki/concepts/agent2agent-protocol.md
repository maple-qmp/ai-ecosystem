---
title: Agent2Agent 协议（A2A）
type: concept
tags: [standard]
layer: L4
aliases: ["Agent2Agent 协议（A2A）", "Agent2Agent", "A2A", "A2A 协议"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# Agent2Agent 协议（A2A）

## 定义

让不同框架、不同语言写成的 Agent 互相发现、委派任务和交换结果的开放协议，由 Linux Foundation 托管。它和 [[concepts/model-context-protocol|MCP]] 互补：MCP 管 Agent 怎样接工具和上下文，A2A 管 Agent 和 Agent 之间怎样通信。规范 1.0.0 已定稿，官方 Java 实现是 [[entities/a2a-java-sdk|A2A Java SDK]]。

## 关键特征

- **Agent Card**：描述 Agent 能力的元数据，可注册到服务中心（如 Nacos）供发现
- **多种传输**：Java SDK 同等支持 JSON-RPC、gRPC、HTTP+JSON/REST
- **跨 SDK 合规**：A2A Java SDK 附带基于 Quarkus 的 ITK，可校验 Python、TypeScript 等 SDK 的协议一致性
- **治理**：Linux Foundation 托管，强调厂商中立

## 应用

- [[entities/google-adk|Google ADK for Java]]：`RemoteA2AAgent` 把远程 Agent 当本地 Agent 用，本地 Agent 经 `AgentExecutor` 对外暴露
- [[entities/langchain4j|LangChain4j]]：`langchain4j-agentic-a2a` 模块
- [[entities/spring-ai-alibaba|Spring AI Alibaba]] 与 [[entities/agentscope|AgentScope Java]]：A2A + Nacos 注册与发现
- [[entities/mastra|Mastra]] 在 Connections 中也支持 A2A

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 协议
- 与 [[concepts/model-context-protocol|MCP]] 并列为 Agent 生态的两类基础协议

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/java-agent-development|Java Agent 开发]]

## 相关实体

- [[entities/a2a-java-sdk|A2A Java SDK]]
- [[entities/google-adk|Google ADK]]
- [[entities/langchain4j|LangChain4j]]
- [[entities/spring-ai-alibaba|Spring AI Alibaba]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The ADK has migrated to use the official A2A Java SDK Client." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
