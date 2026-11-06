---
title: DSPy
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["DSPy", "Declarative Self-improving Python", "dspy"]
released: "2023"
competitors: ["[[entities/langchain]]", "[[entities/llamaindex]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/python-agent-frameworks-survey-2026-11]]"]
---

# DSPy

## 描述

起源于斯坦福 NLP 的开源框架（MIT，GitHub 约 3.89 万星），主张“编程而非提示”：用签名（signature）和模块写组合式 Python 程序，再用优化器根据评测数据自动优化提示和权重，适用于分类器、RAG 流水线到 Agent 循环。名字是 Declarative Self-improving Python 的缩写。代表性优化器有 MIPROv2 和 GEPA（2025-07 论文，反思式提示进化）。3.0 于 2025-08 发布，2026 年依次推出 3.2（dspy.RLM 改进）、3.3（dspy.Flex 让 GEPA 同时优化代码和提示，dspy.ReActV2 支持原生与并行工具调用）和 3.4（新优化器 ReAnchor）。README 称它已改用内置的 lm15 引擎，不再依赖 LiteLLM。它常与其他 Agent 框架组合使用，负责提示优化这一环。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架（见 [[concepts/python-agent-development|Python Agent 开发]]）
- **上游依赖**：—（各模型厂商 API）
- **竞争 / 替代**：[[entities/langchain|LangChain]]、[[entities/llamaindex|LlamaIndex]]（手写提示与链式编排的替代思路）

## 时间线

- 2023-01 仓库创建；2023-10 DSPy 论文
- 2025-07 GEPA 论文
- 2025-08-12 3.0.0
- 2026-04 3.2.0：开始与 LiteLLM 解耦
- 2026-08 3.3.0：dspy.Flex、dspy.ReActV2
- 2026-09 3.4.0：ReAnchor 优化器
- 2026-10-12 3.4.1（PyPI）

## 相关实体

- [[entities/langchain|LangChain]]
- [[entities/llamaindex|LlamaIndex]]

## 相关概念

- [[concepts/python-agent-development|Python Agent 开发]]
- [[concepts/rag|检索增强生成（RAG）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "DSPy is the framework for _programming—rather than prompting—language models_." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
- "DSPy stands for Declarative Self-improving Python." — [[sources/python-agent-frameworks-survey-2026-11|Python Agent 框架调研]]
