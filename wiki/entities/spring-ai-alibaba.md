---
title: Spring AI Alibaba
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Spring AI Alibaba", "SAA", "spring-ai-alibaba"]
org: "[[entities/alibaba]]"
competitors: ["[[entities/agentscope]]", "[[entities/langchain4j]]", "[[entities/embabel]]", "[[entities/langgraph]]"]
depends_on: ["[[entities/spring-ai]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]", "[[sources/moonshot-ai-survey-2026-11]]", "[[sources/zhipu-ai-survey-2026-11]]", "[[sources/minimax-survey-2026-11]]"]
---

# Spring AI Alibaba

## 描述

[[entities/alibaba|阿里巴巴]]开源的 Java Agent 框架（Apache-2.0，GitHub 约 1.11 万星），构建在 [[entities/spring-ai|Spring AI]] 之上，面向 Agent、工作流与多 Agent 应用。结构分三层：最上面是 Agent Framework（ReactAgent，顺序、并行、路由、循环等预置模式，上下文工程，人工介入）；中间是 Graph 运行时（持久化、编排、流式，可直接用来写更灵活的多 Agent 流程，图可导出为 PlantUML / Mermaid）；最底下是 Spring AI。另有 Admin 平台（可视化开发、观测、评测、MCP 管理，可导出成独立 Java 项目）和嵌入式调试界面 Studio。它通过 Nacos 支持 [[concepts/agent2agent-protocol|A2A]] 注册与发现，模型侧支持 DashScope（通义）、OpenAI 等。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（Agent 框架层，见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：[[entities/spring-ai|Spring AI]]
- **竞争 / 替代**：[[entities/agentscope|AgentScope Java]]（同属阿里，已互相集成）、[[entities/langchain4j|LangChain4j]]、[[entities/embabel|Embabel]]、[[entities/langgraph|LangGraph]]（Graph 层思路相近）

## 接入其他中国模型

官方 starter 只单列 DashScope，README 另提到 OpenAI / DeepSeek。[[entities/kimi|Kimi]]、[[entities/glm|GLM]]、[[entities/minimax-m|MiniMax-M]] 有两种接法：一是用 Spring AI 的 OpenAI 兼容客户端直连各家 API；二是走阿里云百炼，它 2026-05 起用统一 API 提供 Kimi K2.6、GLM-5.1、MiniMax M2.7。这是整理者根据两份文档归纳的，官方没有专门写这种用法。

## 时间线

- 1.1.0.0 里程碑版：ReactAgent 前后钩子、`AgentTool`（Agent 当工具）、`ReactAgent.asNode()`（Agent 嵌入图）、`LlmRoutingAgent`、FlowAgent 抽象、A2A + Nacos
- 1.1.2.0：升级到 Spring AI 1.1.2，加入 Agent Skills、并行子 Agent、并行条件边与 AllOf / AnyOf 聚合，官方称可用于生产
- 1.1.2.2：集成 [[entities/agentscope|AgentScope]]、`LlmRoutingAgent` 可作图节点、单 Agent handoff 模式
- 2026-11 Maven Central：agent-framework 正式版 1.1.2.x，2.0.0-M1.1 预发布

## 相关实体

- [[entities/spring-ai|Spring AI]]
- [[entities/agentscope|AgentScope]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/kimi|Kimi]]
- [[entities/glm|GLM]]
- [[entities/minimax-m|MiniMax-M]]

## 相关概念

- [[concepts/java-agent-development|Java Agent 开发]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Agentic AI Framework for Java Developers" — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "A production-ready framework for building Agentic, Workflow, and Multi-agent applications." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
