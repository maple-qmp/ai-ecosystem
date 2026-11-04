---
title: Spring AI
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Spring AI", "spring-ai"]
released: "2025-05"
competitors: ["[[entities/langchain4j]]", "[[entities/google-adk]]", "[[entities/koog]]"]
depends_on: ["[[entities/mcp-java-sdk]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# Spring AI

## 描述

Spring 官方的 LLM 应用框架，由 Broadcom 旗下的 Spring 团队维护，提供 ChatClient、Advisor 链、工具调用、结构化输出、对话记忆、向量存储与 RAG、可观测性等，以 Spring Boot starter 的方式接入。2.0.0 于 2026-06-12 GA，基线升到 Spring Boot 4.0 / 4.1 与 Spring Framework 7.0，改用 Jackson 3 和 JSpecify 空安全注解。2.0 把工具调用循环移进 Advisor 链，核心只保留 OpenAI、Anthropic、Amazon Bedrock、Google GenAI、Mistral AI、DeepSeek、Ollama 等厂商，其余集成交给厂商自己维护。它和 [[entities/mcp-java-sdk|MCP Java SDK]] 团队合作维护，Spring 相关的 MCP 传输和注解都在 Spring AI 里。[[entities/embabel|Embabel]] 和 [[entities/spring-ai-alibaba|Spring AI Alibaba]] 都构建在它之上。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（LLM 应用框架层，见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：[[entities/mcp-java-sdk|MCP Java SDK]]、Spring Boot、各模型厂商 API
- **下游**：[[entities/embabel|Embabel]]、[[entities/spring-ai-alibaba|Spring AI Alibaba]]
- **竞争 / 替代**：[[entities/langchain4j|LangChain4j]]、[[entities/google-adk|Google ADK for Java]]、[[entities/koog|Koog]]

## 2.0 的主要变化

- **Advisor 化的工具循环**：`ToolCallingAdvisor` 自动注册；`ToolSearchToolCallingAdvisor` 按需逐步暴露工具，避免一次把所有工具塞进上下文；`StructuredOutputValidationAdvisor` 在结构化输出校验失败时自动重试
- **MCP**：内置 MCP Java SDK 2.0.0（对应规范 2025-11-25）；`@McpTool`、`@McpResource`、`@McpPrompt` 注解并入；Streamable HTTP 为默认传输，SSE 弃用，STDIO 保留；OAuth 2.0 / API key 安全由社区项目提供
- **社区扩展**：spring-ai-session（事件溯源会话记忆）、spring-ai-agent-utils（Agent Skills、文件与 shell 工具）
- **兼容线**：1.1.x 继续面向 Spring Boot 3.5.x，MCP SDK 固定在 0.18.3

## 时间线

- 2025-02-14 Spring 博客发布 MCP Java SDK 介绍文章
- 2026-03 2.0.0-M3 / M4 与 1.1.x、1.0.x 维护版并行发布
- 2026-06-06 2.0.0-RC1
- 2026-06-12 2.0.0 GA
- 2026-09-25 2.1.0-M1：新增 `OpenAiResponsesChatModel`（对接 OpenAI `/v1/responses`）；宣布 Spring AI Agents 计划
- 2026-10 2.1.0-RC1；最新正式版 2.0.2（Maven Central，2026-11-04）
- 计划 2026-11 以 Spring Projects Experimental 独立项目发布 Spring AI Agents，2027 年中并入 Spring AI 3.0（截至 2026-11-04 未见发布）

## 相关实体

- [[entities/mcp-java-sdk|MCP Java SDK]]
- [[entities/embabel|Embabel]]
- [[entities/spring-ai-alibaba|Spring AI Alibaba]]
- [[entities/langchain4j|LangChain4j]]

## 相关概念

- [[concepts/java-agent-development|Java Agent 开发]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Spring AI 2.0 has been designed to be used with Spring Boot 4.0 / 4.1 and Spring Framework 7.0" — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "Spring AI 2.0 lifts the tool loop into the advisor chain as a first-class, composable component." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "Streamable HTTP is now the default, replacing the deprecated SSE transport." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "with the plan to merge it into Spring AI 3.0 mid next year." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
