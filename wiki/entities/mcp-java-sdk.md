---
title: MCP Java SDK
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["MCP Java SDK", "modelcontextprotocol/java-sdk", "io.modelcontextprotocol.sdk"]
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

# MCP Java SDK

## 描述

[[concepts/model-context-protocol|Model Context Protocol（MCP）]]官方的 Java SDK，用来编写 MCP 服务器和客户端，与 [[entities/spring-ai|Spring AI]] 团队合作维护（GitHub 约 3800 星）。核心模块 `mcp-core` 提供 STDIO、JDK HttpClient、Servlet 三种参考传输和 JSON 绑定接口，JSON 实现分 Jackson 2 与 Jackson 3 两个模块。从 2.0 起，WebClient、WebFlux、WebMVC 等 Spring 传输从 SDK 移到 Spring AI，注解和 Boot starter 也由 Spring AI 提供。2.0.0 对应 MCP 规范 2025-11-25，随 Spring AI 2.0 发布；截至 2026-11 尚未支持 [[concepts/mcp-request-flow|2026-07-28 无状态规范]]。Spring AI 之外，[[entities/langchain4j|LangChain4j]]、[[entities/embabel|Embabel]]、[[entities/koog|Koog]] 等框架也都接入 MCP。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 协议 SDK（见 [[concepts/java-agent-development|Java Agent 开发]]）
- **下游**：[[entities/spring-ai|Spring AI]]（及构建在其上的框架）
- **同层**：[[entities/a2a-java-sdk|A2A Java SDK]]（Agent 间通信，互补）

## 模块

- `mcp-bom`：依赖版本
- `mcp-core`：参考实现（STDIO、JDK HttpClient、Servlet）与 JSON 绑定接口
- `mcp-json-jackson2` / `mcp-json-jackson3`
- `mcp`：core + Jackson 3 便捷包
- `mcp-test`：共享集成测试

## 时间线

- 2025-02-14 Spring 博客发布 MCP Java SDK 介绍文章
- 1.1.x 时期 Spring AI 1.1 固定使用 0.18.3
- 2026-06 2.0.0 随 Spring AI 2.0 GA（规范 2025-11-25，有 SDK 层破坏性变更）
- 2026-11 最新正式版 2.1.0，预发布 2.2.0-M2（Maven Central，2026-11-02）

## 相关实体

- [[entities/spring-ai|Spring AI]]
- [[entities/a2a-java-sdk|A2A Java SDK]]
- [[entities/langchain4j|LangChain4j]]

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]]
- [[concepts/java-agent-development|Java Agent 开发]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The official Java SDK for Model Context Protocol servers and clients. Maintained in collaboration with Spring AI" — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
