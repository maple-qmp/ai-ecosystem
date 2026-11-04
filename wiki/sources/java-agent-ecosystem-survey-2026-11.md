---
title: Java Agent 开发生态调研（2026-11）
type: source
tags: [notes]
source_note: "[[Java-Agent开发生态调研-2026-11]]"
url: https://spring.io/blog/2026/06/12/spring-ai-2-0-0-GA-available-now/
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[concepts/java-agent-development]]"
  - "[[entities/spring-ai]]"
  - "[[entities/langchain4j]]"
  - "[[entities/embabel]]"
  - "[[entities/google-adk]]"
  - "[[entities/koog]]"
  - "[[entities/jetbrains]]"
  - "[[entities/agentscope]]"
  - "[[entities/spring-ai-alibaba]]"
  - "[[entities/mcp-java-sdk]]"
  - "[[entities/a2a-java-sdk]]"
  - "[[concepts/agent2agent-protocol]]"
  - "[[concepts/goal-oriented-action-planning]]"
  - "[[concepts/model-context-protocol]]"
  - "[[concepts/agent-harness]]"
---

# Java Agent 开发生态调研（2026-11）

## Summary

梳理在 JVM（Java / Kotlin）上开发 AI Agent 的主要项目，总结见 [[concepts/java-agent-development|Java Agent 开发]]。生态可分三层：底层是协议 SDK（[[entities/mcp-java-sdk|MCP Java SDK]]、[[entities/a2a-java-sdk|A2A Java SDK]]）；中间是 LLM 应用框架（[[entities/spring-ai|Spring AI]]、[[entities/langchain4j|LangChain4j]]）；上层是 Agent 框架（[[entities/embabel|Embabel]]、LangChain4j Agentic、[[entities/google-adk|Google ADK for Java]]、[[entities/koog|Koog]]、[[entities/agentscope|AgentScope Java]]、[[entities/spring-ai-alibaba|Spring AI Alibaba]]）。2026 年这些项目大多进入 1.0 / 2.0 稳定版。版本号核对自 Maven Central（2026-11-04）。

## Key Points

- **Spring AI 2.0 GA**（2026-06-12）：基线 Spring Boot 4.0 / 4.1；工具循环移入 Advisor 链；内置 MCP Java SDK 2.0（规范 2025-11-25），Streamable HTTP 取代 SSE。计划 2026-11 推出实验项目 Spring AI Agents，2027 年中并入 3.0
- **LangChain4j**：不是 Python LangChain 的移植；1.23.0（2026-10-28）；`langchain4j-agentic` 仍为 beta
- **Embabel**：Rod Johnson 联合创建，构建在 Spring AI 之上，用 [[concepts/goal-oriented-action-planning|GOAP]] 在运行时规划动作；1.0 约 2026-07，最新 1.5.4
- **Google ADK for Java 1.0**（2026-03-30）：App + Plugin 架构、事件压缩、`ToolConfirmation` 人工审批、原生 [[concepts/agent2agent-protocol|A2A]]；最新 1.14.0
- **Koog 1.0**（2026-05，[[entities/jetbrains|JetBrains]]）：1 年 API 稳定承诺，Java API 2026-03 推出，多平台；最新 1.3.0
- **AgentScope Java 2.0**：HarnessAgent 内核 + 托管 Service，阿里内部 13+ 业务单元使用
- **Spring AI Alibaba**：Agent Framework / Graph / Spring AI 三层，A2A + Nacos
- **A2A Java SDK 1.0.0.Final**（2026-06-10）：对齐 A2A 规范 1.0.0，三种传输，groupId 改为 `org.a2aproject.sdk`；最新 1.5.0.Final
- **MCP Java SDK**：最新正式版 2.1.0；尚未支持 [[concepts/model-context-protocol|MCP]] 2026-07-28 规范

## Mentioned Pages

- [[concepts/java-agent-development|Java Agent 开发]]
- [[entities/spring-ai|Spring AI]]
- [[entities/langchain4j|LangChain4j]]
- [[entities/embabel|Embabel]]
- [[entities/google-adk|Google ADK]]
- [[entities/koog|Koog]]
- [[entities/jetbrains|JetBrains]]
- [[entities/agentscope|AgentScope]]
- [[entities/spring-ai-alibaba|Spring AI Alibaba]]
- [[entities/mcp-java-sdk|MCP Java SDK]]
- [[entities/a2a-java-sdk|A2A Java SDK]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/langchain|LangChain]]
- [[entities/langgraph|LangGraph]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/goal-oriented-action-planning|目标导向行动规划（GOAP）]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/ai-agent|AI Agent]]
