---
title: Arize Phoenix
type: entity
tags: [project]
kind: infra
layer: L4
aliases: ["Arize Phoenix", "Phoenix"]
competitors: ["[[entities/langsmith]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/ai-evaluation-observability-survey-2026-11]]"]
---

# Arize Phoenix

## 描述

Arize AI 与开源社区构建的 AI 可观测性和评测工具。官方文档将逐步运行追踪、评分、提示迭代与同输入实验比较连接起来；它与 Arize 的托管企业产品 AX 应分别识别。

- 接收 OTLP 追踪，使用 OpenInference 仪表化和语义约定展示模型、检索与工具等步骤。
- 支持模型评分、代码检查与人工标签，也能用数据集和实验比较版本。
- 可对运行中的特定 span 分析，定位局部失败，再查看完整任务结果。
- 支持 OTLP 不意味着任意 GenAI 字段都得到同样展示；接入前应核对属性映射。
- 本次未部署，未核实商业套餐或部署地域，不作工具效果排名。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]。
- 技术基础：OpenTelemetry 与 OpenInference。
- 同类：[[entities/langsmith|LangSmith]]；配置式回归检查可另参考 [[entities/promptfoo|Promptfoo]]。

## 时间线

- 2026-11-06：查阅官方文档收录，本日期是核实日期，不是发布日期。

## 相关实体

- [[entities/langsmith|LangSmith]]
- [[entities/promptfoo|Promptfoo]]

## 相关概念

- [[concepts/llm-observability|LLM 可观测性]]
- [[concepts/ai-application-evaluation|AI 应用评测]]
- [[concepts/llm-as-judge|LLM 裁判]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用官方文档转述，原始链接见 [[sources/ai-evaluation-observability-survey-2026-11|评测与可观测性专题来源索引]]。
