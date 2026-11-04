---
title: Embabel
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Embabel", "Embabel Agent Framework", "embabel-agent"]
released: "2026-04"
competitors: ["[[entities/langgraph]]", "[[entities/langchain4j]]", "[[entities/koog]]"]
depends_on: ["[[entities/spring-ai]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# Embabel

## 描述

Spring 框架创始人 Rod Johnson 联合创建的 JVM Agent 框架（Apache-2.0，GitHub 约 4500 星），用 Kotlin 写成，Java 也能自然使用。它构建在 [[entities/spring-ai|Spring AI]] 之上，直接用 Spring AI 的 `ChatModel`、`@Tool` 和 MCP 配置，自比为 Spring AI 之上的“Spring MVC”。开发者用类型化领域对象声明目标（goal）、动作（action）和条件（condition），由规划器在运行时找出达成目标的动作序列，默认算法是 [[concepts/goal-oriented-action-planning|GOAP]]，条件变化时可以重新规划。这和 [[entities/langgraph|LangGraph]] 那种预先画好图的方式不同。1.0 GA 约在 2026-07，2026-10 已到 1.5.x。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（Agent 框架层，见 [[concepts/java-agent-development|Java Agent 开发]]）
- **上游依赖**：[[entities/spring-ai|Spring AI]]
- **竞争 / 替代**：[[entities/langgraph|LangGraph]]、[[entities/langchain4j|LangChain4j]] Agentic、[[entities/koog|Koog]]

## 主要特性

- **规划**：GOAP 为默认规划器，规划器可插拔；也支持 Utility AI（按效用分数选动作）；可与显式状态机混用
- **按动作选模型**：每个动作可指定具体模型，或用 best、cheapest 等角色别名
- **可解释**：执行轨迹可检查、可复现
- **MCP**：可消费 MCP 服务器，也能作为 MCP 服务器运行（见 [[concepts/model-context-protocol|MCP]]）

## 时间线

- 2026-04 在 Microsoft JDConf 公开介绍
- 2026-07 前后 1.0 GA（InfoQ 2026-08-03 报道）
- 2026-10 Devoxx Belgium 2026 有 Embabel Agent v1.5 演讲
- 2026-10-28 Maven Central 发布 1.5.4

## 相关实体

- [[entities/spring-ai|Spring AI]]
- [[entities/langgraph|LangGraph]]
- [[entities/langchain4j|LangChain4j]]

## 相关概念

- [[concepts/goal-oriented-action-planning|目标导向行动规划（GOAP）]]
- [[concepts/java-agent-development|Java Agent 开发]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Agent framework for the JVM. Pronounced Em-BAY-bel /ɛmˈbeɪbəl/" — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "Written in Kotlin but offers a natural usage model from Java." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "We build on it, and embrace the Spring component model." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
- "Spring AI exists at the level of the Servlet API, while Embabel is more like Spring MVC." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
