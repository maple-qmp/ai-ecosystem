---
title: AI 应用评测
type: concept
tags: [method]
layer: L4
aliases: ["AI 应用评测", "Agent 评测", "AI Application Evaluation", "Agent Evals"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/ai-evaluation-observability-survey-2026-11]]"]
---

# AI 应用评测

## 定义

把任务输入、初始环境与成功条件固定下来，通过一次或多次试验测量 AI 应用是否完成目标。评测对象包含模型、上下文、数据、工具与 Agent 运行框架，不能用单一模型榜单分数替代。

## 关键特征

- **任务与试验**：task 定义要完成什么，trial 是一次尝试，grader 对指定维度评分。
- **结果与轨迹**：实际环境终态是 outcome，调用记录是 trace；“声称完成”不能替代状态验证。
- **评分组合**：程序检查客观条件，模型裁判处理开放维度，人工复核校准边界。
- **离线与在线**：固定数据集比较版本；真实流量帮助发现漏测行为，审核后的失败回流回归集。
- **能力与回归**：前者探索难题，后者保护已能完成的任务。
- **随机性**：重复运行并隔离初始状态；pass@k 表示至少成功一次，pass^k 表示全部成功，二者衡量目标不同。
上述定义和方法主要依据 Anthropic Agent 评测文章与 LangSmith 官方文档。

## 应用

用于模型、提示、检索和记忆策略变更前后比较。专题以知识库助手设计六类用例，记录成功率、证据支撑、拒答、延迟与每成功任务成本；未实际运行，阈值须由业务要求确定。

## 生态位置

- 层级：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 研究依据与详细设计：[[sources/ai-evaluation-observability-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/llm-as-judge|LLM 裁判]]
- [[concepts/llm-observability|LLM 可观测性]]
- [[concepts/longmemeval|LongMemEval]]
- [[concepts/benchmark-contamination|基准污染与饱和]]

## 相关实体

- [[entities/langsmith|LangSmith]]
- [[entities/langfuse|Langfuse]]
- [[entities/arize-phoenix|Arize Phoenix]]
- [[entities/promptfoo|Promptfoo]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/ai-evaluation-observability-survey-2026-11|专题来源索引]]。
