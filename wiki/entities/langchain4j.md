---
title: LangChain4j
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["LangChain4j", "LangChain for Java", "quarkus-langchain4j"]
competitors: ["[[entities/spring-ai]]", "[[entities/google-adk]]", "[[entities/koog]]", "[[entities/embabel]]"]
depends_on: ["[[entities/a2a-java-sdk]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# LangChain4j

## 描述

开源 Java LLM 应用与 Agent 库（Apache-2.0，GitHub 约 1.34 万星），统一接入 20+ 模型厂商和 30+ 嵌入存储，提供声明式 AI Service、工具调用（含 [[concepts/model-context-protocol|MCP]]）、RAG、护栏、skills 和观测指标，并与 Quarkus、Spring Boot 集成。名字虽然来自 [[entities/langchain|LangChain]]，但 README 明确说它是为 Java 设计的，不是 Python 版的移植。`langchain4j-agentic` 模块把 Agent 声明成 Java 接口，用 AgenticScope 共享状态，再组合成顺序、循环、条件、并行工作流，或交给 supervisor Agent 路由。核心库已是正式版（1.23.0），但 agentic 模块在 Maven Central 上仍以 `-beta` 版本号发布。Quarkus 一侧由 Quarkiverse 的 quarkus-langchain4j 提供集成，含 `quarkus-langchain4j-agentic`。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：[[entities/a2a-java-sdk|A2A Java SDK]]（agentic-a2a 模块）、各模型厂商 API
- **竞争 / 替代**：[[entities/spring-ai|Spring AI]]、[[entities/google-adk|Google ADK for Java]]、[[entities/koog|Koog]]、[[entities/embabel|Embabel]]

## 主要模块

- **AI Service**：用接口 + 注解声明 LLM 能力，框架生成实现
- **Agentic**：`langchain4j-agentic`、`langchain4j-agentic-patterns`（voting、Confidence Cascade 等模式）、`langchain4j-agentic-mcp`、`langchain4j-agentic-a2a`
- **MCP**：`langchain4j-mcp`、`langchain4j-mcp-docker`
- **RAG**：`langchain4j-easy-rag` 等，见 [[concepts/rag|RAG]]
- **测试**：`langchain4j-test`（1.23.0 起含 LLM 评审与断言）

## 时间线

- 2026-02 维护者在讨论区表示 agentic 模块的 beta 标签只因 API 仍有小改动，计划晚春 / 初夏去掉
- 2026 年中 1.17.x 前后，约每月一个小版本；Quarkus 博客介绍 1.15.0 的 voting 模式
- 2026-08-19 `quarkus-langchain4j-agentic` 发布新版
- 2026-10-28 1.23.0：Ollama decision models、Confidence Cascade 模式、汇总单次 AI Service 调用的观测事件、decision agents
- 2026-11-02 多条维护线同日补丁（1.19.5、1.11.12、1.5.4）；agentic 仍为 1.23.0-beta33

## 相关实体

- [[entities/spring-ai|Spring AI]]
- [[entities/langchain|LangChain]]
- [[entities/a2a-java-sdk|A2A Java SDK]]
- [[entities/mcp-java-sdk|MCP Java SDK]]

## 相关概念

- [[concepts/java-agent-development|Java Agent 开发]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The goal of LangChain4j is to simplify integrating LLMs into Java applications." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "Despite the name, LangChain4j is not a Java port of LangChain (Python) — it is built for Java, not ported to it." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
