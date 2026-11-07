---
title: 上下文工程与 Agent 记忆体系调研（2026-11）
type: source
tags: [notes]
source_note: "[[raw/上下文工程与Agent记忆体系调研-2026-11]]"
url: https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
created: 2026-11-06
updated: 2026-11-06
sources:
  - "[[concepts/context-engineering]]"
  - "[[concepts/agent-memory]]"
  - "[[concepts/context-compaction]]"
  - "[[concepts/longmemeval]]"
---

# 上下文工程与 Agent 记忆体系调研（2026-11）

## Summary

综合 Anthropic 上下文工程经验、LangGraph 记忆文档与 LongMemEval 原始研究，区分当前上下文、线程状态和跨线程记忆；提供知识库助手的未运行对照设计。

完整研究、逐项来源及证据边界见 [[raw/上下文工程与Agent记忆体系调研-2026-11|原始调研]]。这是二次研究笔记，不是原文逐字存档。检索与查阅日期为 2026-11-06。

## Key Points

- 上下文选择、外置、压缩、隔离与按需读取各有收益和代价。
- 记忆范围、内容类型、写入时机是不同分类轴。
- 使用索引、检索、读取三个阶段定位记忆失败；历史论文分数不代表当前产品能力。

## Mentioned Pages

- [[concepts/context-engineering|context-engineering]]
- [[concepts/agent-memory|agent-memory]]
- [[concepts/context-compaction|context-compaction]]
- [[concepts/longmemeval|longmemeval]]

- [[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- [[maps/X-横切主题|X-横切主题]]

## 原始来源与摘录

原始调研的来源表给出官方链接和适用范围；其中“官方原文摘录”保留短句，其余内容为中文转述。实验设计不等于已验证结论。
