---
title: Google ADK
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Google ADK", "Agent Development Kit", "ADK for Java", "adk-java"]
competitors: ["[[entities/spring-ai]]", "[[entities/langchain4j]]", "[[entities/koog]]", "[[entities/langgraph]]"]
depends_on: ["[[entities/a2a-java-sdk]]", "[[entities/gemini]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# Google ADK

## 描述

Google 开源的 Agent Development Kit，有 Python、Java、Go、TypeScript、Kotlin 多个语言版本；Python 版是领先实现，新功能通常先在 Python 出现，再移植到 Java。本页侧重 Java 版：ADK for Java 1.0.0 于 2026-03-30 发布，引入 `App` 顶层容器和 Plugin 架构，加入事件压缩、基于 `ToolConfirmation` 的人工审批，以及基于 Firestore、Vertex AI 的会话与记忆服务。它通过官方 [[entities/a2a-java-sdk|A2A Java SDK]] 原生支持 [[concepts/agent2agent-protocol|A2A]]。部分工具（Google Maps 接地、URL 读取）依赖 [[entities/gemini|Gemini]]。到 2026-11 Java 版已更新到 1.14.0。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（Agent 框架层，见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：[[entities/a2a-java-sdk|A2A Java SDK]]、[[entities/gemini|Gemini]] 与 Google Cloud（Vertex AI、Firestore、GCS）
- **竞争 / 替代**：[[entities/spring-ai|Spring AI]]、[[entities/langchain4j|LangChain4j]]、[[entities/koog|Koog]]、[[entities/langgraph|LangGraph]]

## Java 1.0 的主要能力

- **App 与 Plugin**：`App` 持有根 Agent、全局设置和插件；内置 `LoggingPlugin`、`ContextFilterPlugin`、`GlobalInstructionPlugin`
- **事件压缩**：`eventsCompactionConfig()` 保留近期事件滑动窗口，较早历史做摘要
- **人工审批**：工具通过 `ToolConfirmation` 暂停执行、等待批准后继续
- **工具**：`GoogleMapsTool`、`UrlContextTool`、`ContainerCodeExecutor`、`VertexAiCodeExecutor`、`ComputerUseTool`
- **服务**：Session（内存 / Vertex AI / Firestore）、Memory（内存 / Firestore）、Artifact（内存 / GCS）
- **A2A**：`RemoteA2AAgent` 把远程 Agent 当本地 Agent 用；本地 Agent 可经 `AgentExecutor` 暴露为 A2A 服务

## 时间线

- 2026-03-30 ADK for Java 1.0.0
- 2026-09 前后 ADK for Kotlin 1.0
- 2026-11-02 Java 版 1.14.0（Maven Central）

## 相关实体

- [[entities/gemini|Gemini]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/a2a-java-sdk|A2A Java SDK]]

## 相关概念

- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/java-agent-development|Java Agent 开发]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The App class is the new top-level container for an agentic application." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "The ADK has migrated to use the official A2A Java SDK Client." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
