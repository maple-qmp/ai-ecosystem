---
title: AgentScope
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["AgentScope", "AgentScope Java", "agentscope-java"]
org: "[[entities/alibaba]]"
competitors: ["[[entities/spring-ai-alibaba]]", "[[entities/langchain4j]]", "[[entities/google-adk]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]", "[[sources/moonshot-ai-survey-2026-11]]", "[[sources/minimax-survey-2026-11]]", "[[sources/bytedance-doubao-survey-2026-11]]"]
---

# AgentScope

## 描述

[[entities/alibaba|阿里巴巴]]开源的 Agent 框架，有 Python 与 Java 两个实现；本页侧重 Java 版（java.agentscope.io）。AgentScope Java 1.0 约在 2025 年末发布，以 ReAct 循环为核心，同时推出 AgentScope Runtime（安全沙箱、A2A Agent、一键部署到阿里云），并支持把 Agent Card 注册到 Nacos。2.0 改为两部分：自建应用用的 AgentScope Harness SDK，和用 API 发布、调用 Agent 的托管平台 AgentScope Service，两者共享 HarnessAgent 内核（见 [[concepts/agent-harness|Agent Harness]]）。官方称它是阿里集团内部最广泛使用的 Agent 框架，在 13+ 个业务单元生产运行。Java 版需 JDK 17+。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（Agent 框架层，见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：—（通义等模型 API；部署依赖阿里云）
- **竞争 / 替代**：[[entities/spring-ai-alibaba|Spring AI Alibaba]]（同属阿里，1.1.2.2 起已集成 AgentScope）、[[entities/langchain4j|LangChain4j]]、[[entities/google-adk|Google ADK]]

## 2.0 HarnessAgent 能力

- 沿用 ReActAgent 的推理—工具循环
- Java 工具与 [[concepts/model-context-protocol|MCP]]，子 Agent 委派
- 每步构建上下文、长历史压缩，按需加载记忆、skills 与工作文件
- 持久会话：事件日志与检查点
- 工具可在本地或配置好的沙箱中执行

## 模型提供方

- **Python 版**：模型模块内置 OpenAI、Anthropic、Gemini、DashScope、DeepSeek、Moonshot（[[entities/kimi|Kimi]]）、Volcengine（[[entities/doubao|豆包]]）、xAI、Ollama；2026-09 起新增 `MiniMaxChatModel`，默认用 [[entities/minimax-m|MiniMax-M3]]
- **Java 2.0**：模型提供方拆成独立扩展模块，官方列出 DashScope、OpenAI、Anthropic、Gemini、[[entities/ollama|Ollama]]；[[entities/glm|GLM]] 等其他模型通过 OpenAI 兼容模块接入

## 时间线

- 2025 年末 AgentScope Java 1.0 与 AgentScope Runtime 1.0 同时发布
- 2026 AgentScope Java 2.0（Harness SDK + Service）
- 2026-09 Python 版新增 MiniMax 模型支持
- 2026-10-08 `agentscope-core` 2.1.0-BETA1；最新正式版 2.0.4（Maven Central）

## 相关实体

- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/spring-ai-alibaba|Spring AI Alibaba]]
- [[entities/qwen|Qwen]]
- [[entities/kimi|Kimi]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/doubao|豆包]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]
- [[concepts/java-agent-development|Java Agent 开发]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Java Harness requires JDK 17 or later and credentials for your chosen model." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "MiniMax chat models supported via `MiniMaxChatModel` (MiniMax-M3 by default)." — [[sources/minimax-survey-2026-11|MiniMax 调研]]（AgentScope README）
