---
title: Langfuse
type: entity
tags: [project]
kind: infra
layer: L4
aliases: ["Langfuse"]
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

# Langfuse

## 描述

开源、可自托管的 AI 工程平台，提供运行追踪、会话观察、提示管理等能力。官方文档说明它基于 OpenTelemetry，支持通过原生 SDK、框架集成或网关采集调用；定位是帮助分析与迭代应用，而非仅列出模型调用日志。

- 追踪覆盖模型和非模型步骤，例如检索、嵌入和外部 API。
- 会话可关联多轮交互，面板可分析质量、成本和延迟。
- 脱敏文档说明可在数据离开应用前处理输入、输出与元信息；具体 hook 取决于 SDK 版本。
- 本次未部署，也未核实套餐价格、所有组件许可证和自托管功能边界；开源与可自托管不意味着托管服务免费或零运维。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]。
- 技术基础：OpenTelemetry 与对应语言 SDK/集成。
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
