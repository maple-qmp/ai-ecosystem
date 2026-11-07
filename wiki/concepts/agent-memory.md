---
title: Agent 记忆
type: concept
tags: [term]
layer: L4
aliases: ["Agent 记忆", "Agent Memory", "智能体记忆", "长期记忆", "短期记忆"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/context-memory-survey-2026-11]]"]
---

# Agent 记忆

## 定义

让 Agent 保存、更新并重新使用此前交互信息的系统机制。LangGraph 按使用范围区分线程内短期记忆和跨线程长期记忆；短期状态也可以持久化到数据库，“短期”不等于只能存在 RAM 中。

## 关键特征

- **内容维度**：事实型 semantic、经历型 episodic、操作规则型 procedural；这与短期/长期范围维度可以交叉。
- **语义记忆不等于语义搜索**：前者描述事实内容，后者是检索手段。
- **存储形态**：整体 profile 易于读取全貌，分散 collection 易于追加；两者分别面临复杂修改或去重、检索、冲突维护问题。
- **写入时机**：同步写入便于立即使用但增加响应延迟；后台写入减少主流程负担但存在可见性滞后。
- **诊断阶段**：LongMemEval 将长期记忆分为索引、检索、读取；记录存在、被召回、被正确使用是不同条件。
- **工程边界**：持久化提供恢复条件，不能代替权限检查、事实修正和检索策略。分类和写入权衡依据 LangGraph 文档，阶段划分依据 LongMemEval。

## 应用

用于跨会话偏好、长任务状态和历史经验复用。专题中的知识库助手设计将来源、作用范围、观察时间、生效时间和替代关系一起保存，并用纠正旧事实、跨用户干扰、无法回答等用例验证；这是设计示例，尚未部署。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 研究依据与详细设计：[[sources/context-memory-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/context-engineering|上下文工程]]
- [[concepts/observational-memory|观察式记忆]]
- [[concepts/longmemeval|LongMemEval]]
- [[concepts/rag|RAG]]

## 相关实体

- [[entities/langgraph|LangGraph]]
- [[entities/mastra|Mastra]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/context-memory-survey-2026-11|专题来源索引]]。
