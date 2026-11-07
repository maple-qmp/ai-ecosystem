---
title: AI 应用评测与可观测性调研（2026-11）
type: source
tags: [notes]
source_note: "[[raw/AI应用评测与可观测性调研-2026-11]]"
url: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents
created: 2026-11-06
updated: 2026-11-06
sources:
  - "[[concepts/ai-application-evaluation]]"
  - "[[concepts/llm-as-judge]]"
  - "[[concepts/llm-observability]]"
  - "[[entities/langfuse]]"
  - "[[entities/arize-phoenix]]"
  - "[[entities/langsmith]]"
  - "[[entities/promptfoo]]"
---

# AI 应用评测与可观测性调研（2026-11）

## Summary

综合官方评测实践、裁判偏差研究、遥测规范与工具文档，建立任务成功标准、离线实验、轨迹诊断和线上失败回流的闭环；案例和阈值均未实测。

完整研究、逐项来源及证据边界见 [[raw/AI应用评测与可观测性调研-2026-11|原始调研]]。这是二次研究笔记，不是原文逐字存档。检索与查阅日期为 2026-11-06。

## Key Points

- 区分 task、trial、grader、trace 与实际 outcome。
- 模型裁判需要校准；重复试验需隔离状态，不能把 pass@k 当作稳定可靠性。
- GenAI 遥测约定仍在 Development；完整内容采集与脱敏需单独设计。

## Mentioned Pages

- [[concepts/ai-application-evaluation|ai-application-evaluation]]
- [[concepts/llm-as-judge|llm-as-judge]]
- [[concepts/llm-observability|llm-observability]]
- [[entities/langfuse|langfuse]]
- [[entities/arize-phoenix|arize-phoenix]]
- [[entities/langsmith|langsmith]]
- [[entities/promptfoo|promptfoo]]

- [[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- [[maps/X-横切主题|X-横切主题]]

## 原始来源与摘录

原始调研的来源表给出官方链接和适用范围；其中“官方原文摘录”保留短句，其余内容为中文转述。实验设计不等于已验证结论。
