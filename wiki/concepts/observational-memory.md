---
title: Observational Memory
type: concept
tags: [method]
layer: L4
aliases: ["Observational Memory", "观察式记忆", "OM"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# Observational Memory

## 定义

[[entities/mastra|Mastra]] 2026-02 提出的 Agent 记忆方法：主 Agent 旁边常驻两个后台 Agent，Observer 把对话历史压缩成一份带日期、带优先级的观察日志，Reflector 定期把这份日志再浓缩。主 Agent 直接从上下文里读这份日志，不需要每轮去检索记忆，也不需要在上下文快满时停下来做整段压缩（compaction）。

## 关键特征

- **后台运行**：Observer 与 Reflector 不打断主 Agent，原文比作主 Agent 的“潜意识”
- **观察日志而非原始消息**：保留的是带时间和优先级的事实，旧消息逐步被替换
- **两级压缩**：Observer 做增量压缩，Reflector 做周期性再压缩
- **不依赖检索**：与基于向量召回的记忆（语义召回、[[concepts/rag|RAG]]）互补而非替代
- **自报成绩**：LongMemEval（longmemeval_s）上 gpt-5-mini 94.87%、gemini-3-pro-preview 93.27%、gpt-4o 84.23%；多会话类问题最弱（最好 87.2%）

## 应用

- 长会话编程 Agent：[[entities/mastra-code|Mastra Code]] 用它取代上下文压缩
- Mastra 框架 Memory 模块中的一种记忆类型，与消息历史、语义召回、working memory 并列

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 属于 [[concepts/agent-harness|Agent Harness]] 中“上下文管理”与“记忆”这一块的一种实现

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/rag|检索增强生成（RAG）]]

## 相关实体

- [[entities/mastra|Mastra]]
- [[entities/mastra-code|Mastra Code]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Think of them as the subconscious mind of the main agent: always running, never interrupting." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
