---
title: Koog
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Koog", "Koog for Java", "ai.koog"]
org: "[[entities/jetbrains]]"
competitors: ["[[entities/spring-ai]]", "[[entities/langchain4j]]", "[[entities/google-adk]]", "[[entities/embabel]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# Koog

## 描述

[[entities/jetbrains|JetBrains]] 开源的 Agent 框架（Apache-2.0，GitHub 约 4700 星），用 Kotlin 写成，同时提供惯用的 Kotlin 与 Java API，主打可预测、容错、企业级。它基于 Kotlin Multiplatform，目标平台包括 JVM、JS、WasmJS、iOS，可以从后端服务一直用到移动端和浏览器；JVM 上需要 JDK 17+。2026-03 推出 Koog for Java（fluent builder API、线程池执行器、Spring Boot 集成），2026-05 在 KotlinConf 2026 发布 1.0，承诺核心 API 一年内保持稳定。功能包括图式工作流、MCP 工具、ACP（Agent Client Protocol）集成、Agent 状态持久化与断点恢复、内置重试，以及可导出到 W&B Weave、Langfuse 的 OpenTelemetry 追踪。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（Agent 框架层，见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：—（各模型厂商 API）
- **竞争 / 替代**：[[entities/spring-ai|Spring AI]]、[[entities/langchain4j|LangChain4j]]、[[entities/google-adk|Google ADK]]、[[entities/embabel|Embabel]]

## 时间线

- 2026-03 Koog for Java：函数式、图、规划三类工作流策略
- 2026-05 KotlinConf 2026 发布 1.0：稳定核心与 1 年 API 稳定承诺，HTTP 传输解耦，全平台 OpenTelemetry
- 2026-09-23 1.3.0（Maven Central）

## 相关实体

- [[entities/jetbrains|JetBrains]]
- [[entities/spring-ai|Spring AI]]
- [[entities/langchain4j|LangChain4j]]

## 相关概念

- [[concepts/java-agent-development|Java Agent 开发]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Koog is a Kotlin-based framework designed to build and run AI agents entirely in idiomatic Kotlin and Java API." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
