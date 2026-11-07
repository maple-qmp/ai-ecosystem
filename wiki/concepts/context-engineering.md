---
title: 上下文工程
type: concept
tags: [method]
layer: L4
aliases: ["上下文工程", "Context Engineering"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/context-memory-survey-2026-11]]"]
---

# 上下文工程

## 定义

管理每次模型推理所接收的信息集合，包括指令、工具描述、消息历史、任务状态和外部证据。Anthropic 将它与侧重指令措辞和组织的提示词工程区分：Agent 每完成一步，下一次调用的上下文都需要重新选择和组织。

## 关键特征

- **选择与即时加载**：先保存路径、查询等轻量引用，需要时读取具体内容，减少无关信息；额外工具调用会增加延迟。
- **外置与压缩**：大结果保存到文件，用有来源的摘要和引用维持连续性；压缩可能丢失限定条件。
- **隔离**：子任务可使用独立上下文，向主任务汇报结果；汇报也要保留证据和不确定性。
- **混合策略**：预取必需约束和基础资料，再按需检索，不要求把所有问题都交给自主搜索。
- **有效性边界**：大窗口不自动保证使用好证据；具体收益需在固定模型、任务和预算下验证。以上方法依据 Anthropic 上下文工程文章，属于工程经验。

## 应用

用于长会话、代码研究、知识库问答和多步骤任务。针对本库的未运行设计：先读约定与相关地图，再取实体页和来源；压缩时保留用户要求、版本范围、未决冲突及证据位置。完整对照方案见专题原始调研。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 研究依据与详细设计：[[sources/context-memory-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/agent-memory|Agent 记忆]]
- [[concepts/context-compaction|上下文压缩]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/rag|RAG]]
- [[concepts/ai-application-evaluation|AI 应用评测]]

## 相关实体

- [[entities/langgraph|LangGraph]]
- [[entities/mastra|Mastra]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/context-memory-survey-2026-11|专题来源索引]]。
