---
title: LLM 裁判
type: concept
tags: [method]
layer: L4
aliases: ["LLM 裁判", "LLM-as-a-Judge", "模型评分器"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/ai-evaluation-observability-survey-2026-11]]"]
---

# LLM 裁判

## 定义

让语言模型根据明确准则评估回答或任务轨迹的做法，可用于参考答案评分、分维度判断或成对比较。它提供可扩展的判断信号，但不是天然可靠的真值。

## 关键特征

- **适用维度**：证据支撑、覆盖、表达质量等难用简单规则判断的内容；客观状态优先直接检查。
- **已知偏差**：MT-Bench / Chatbot Arena 原始论文讨论位置、冗长、自偏好偏差和推理能力局限；历史一致率不是当前应用的保证。
- **校准**：Anthropic 建议用人工判断校准模型评分，按清晰准则评估，并允许信息不足时输出 unknown。
- **版本控制**：裁判模型和准则是测量的一部分；更换评分器会影响分数可比性。
- **结果审阅**：查看评分理由和证据是否对应，不只看聚合分数。

## 应用

用于开放问答、研究综合与 Agent 行为评估。专题给出的校准方案包括盲化答案来源、成对答案换序、检查误放行和误拒绝，并把被评文本作为数据处理；该方案未实测。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 研究依据与详细设计：[[sources/ai-evaluation-observability-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/ai-application-evaluation|AI 应用评测]]
- [[concepts/llm-observability|LLM 可观测性]]
- [[concepts/chatbot-arena|Chatbot Arena]]

## 相关实体

- [[entities/langsmith|LangSmith]]
- [[entities/arize-phoenix|Arize Phoenix]]
- [[entities/promptfoo|Promptfoo]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/ai-evaluation-observability-survey-2026-11|专题来源索引]]。
