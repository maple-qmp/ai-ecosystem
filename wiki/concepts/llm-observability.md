---
title: LLM 可观测性
type: concept
tags: [field]
layer: L4
aliases: ["LLM 可观测性", "LLM Observability", "Agent 可观测性", "AI 运行追踪"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/ai-evaluation-observability-survey-2026-11]]"]
---

# LLM 可观测性

## 定义

通过追踪、指标与运行记录观察 AI 应用的模型调用、检索、工具和任务状态，帮助解释延迟、成本与失败原因。追踪展示发生了什么，正确性还需要任务标准和评分。

## 关键特征

- **层次**：span 描述一次步骤，trace 关联一次请求中的步骤，session/thread 可关联多轮请求；平台命名可能不同。
- **诊断信息**：模型与提示版本、token、耗时、错误、文档引用和工具结果等，具体字段取决于埋点。
- **标准边界**：OpenTelemetry 提供遥测机制；GenAI conventions 和 OpenInference 定义 AI 语义。查阅时 GenAI spans 仍标记 Development，不能假设属性永久稳定。
- **兼容边界**：Phoenix 使用 OpenInference 解释 AI span；支持 OTLP 接入不等于所有其他约定都得到同样渲染。
- **内容管理**：GenAI 规范不建议默认记录完整指令和输入输出；可按需启用或存外部引用。Langfuse 文档提供导出前脱敏方式。
以上依据 OpenTelemetry 规范及 Langfuse、Phoenix 官方文档，不代表所有平台具有相同默认行为。

## 应用

用于定位检索漏召回、压缩后失真、工具重试、延迟和费用异常，并将失败轨迹转为离线用例。日志应有适当访问与保留范围，不能因便于调试而默认复制全部私有正文。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 研究依据与详细设计：[[sources/ai-evaluation-observability-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/ai-application-evaluation|AI 应用评测]]
- [[concepts/llm-as-judge|LLM 裁判]]
- [[concepts/context-engineering|上下文工程]]

## 相关实体

- [[entities/langsmith|LangSmith]]
- [[entities/langfuse|Langfuse]]
- [[entities/arize-phoenix|Arize Phoenix]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/ai-evaluation-observability-survey-2026-11|专题来源索引]]。
