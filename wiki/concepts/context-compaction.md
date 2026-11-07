---
title: 上下文压缩
type: concept
tags: [method]
layer: L4
aliases: ["上下文压缩", "Context Compaction", "Compaction"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/context-memory-survey-2026-11]]"]
---

# 上下文压缩

## 定义

将较长的对话与工具历史提炼成较短表示，供后续调用继续任务。Anthropic 的工程文章把 compaction 与外部笔记、子 Agent 上下文隔离并列为长任务的管理方式。

## 关键特征

- **保留什么**：任务目标、关键决定、未解决问题和继续工作所需细节；不是单纯缩短字数。
- **丢弃什么**：冗余或过时的工具输出；是否可丢弃取决于后续能否重新读取。
- **风险**：压缩可能漏掉否定、日期、例外或证据位置，造成后续错误。
- **调优方向**：Anthropic 建议先确保关键信息召回，再精简多余内容。
- **与记忆的关系**：摘要是上下文表示，长期记忆还有更新、召回和跨线程范围等问题；两者不是同义词。

## 应用

用于超过单次窗口的持续任务。可用相同问题比较压缩前后的约束保留、事实正确性和成本；保留原始材料引用供需要时重读。专题提供的压缩对照实验未运行，不宣称任何压缩率下都无损。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 研究依据与详细设计：[[sources/context-memory-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/context-engineering|上下文工程]]
- [[concepts/agent-memory|Agent 记忆]]
- [[concepts/observational-memory|观察式记忆]]
- [[concepts/ai-application-evaluation|AI 应用评测]]

## 相关实体

- [[entities/claude-code|Claude Code]]
- [[entities/langgraph|LangGraph]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/context-memory-survey-2026-11|专题来源索引]]。
