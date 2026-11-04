---
title: A2A Java SDK
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["A2A Java SDK", "a2a-java", "org.a2aproject.sdk"]
released: "2025"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# A2A Java SDK

## 描述

[[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]的官方 Java 实现，由 Red Hat 的 Quarkus 与 WildFly 团队和 Google 合作发起，现归 A2A Project 组织维护。1.0.0.Final 于 2026-06-10 发布，是首个 GA 版本，对齐 A2A 规范 1.0.0，相对 0.3.x 完全重设计，此前经历 7 个预发布、17 位贡献者。JSON-RPC、gRPC、HTTP+JSON/REST 三种传输同等支持；参考实现基于 Quarkus，WildFly / Jakarta EE 有社区集成。[[entities/google-adk|Google ADK for Java]] 和 [[entities/langchain4j|LangChain4j]] 的 agentic-a2a 模块都用它。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 协议 SDK（见 [[concepts/java-agent-development|Java Agent 开发]]）
- **下游**：[[entities/google-adk|Google ADK]]、[[entities/langchain4j|LangChain4j]]
- **同层**：[[entities/mcp-java-sdk|MCP Java SDK]]（工具与上下文，互补）

## 时间线

- 2025 Quarkus 博客宣布 A2A 项目推出 Java SDK
- 2026 1.0.0.Alpha1 起对齐 1.0 规范，随后 Beta1、CR1
- 2026-06-10 1.0.0.Final：groupId 由 `io.github.a2asdk` 改为 `org.a2aproject.sdk`，包名同步改；附带跨 SDK 合规测试工具 ITK
- 2026-11-03 1.5.0.Final（Maven Central）

## 相关实体

- [[entities/google-adk|Google ADK]]
- [[entities/langchain4j|LangChain4j]]
- [[entities/mcp-java-sdk|MCP Java SDK]]

## 相关概念

- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/java-agent-development|Java Agent 开发]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "If you’ve been tracking the pre-releases, you can upgrade from CR1 with no breaking changes." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
