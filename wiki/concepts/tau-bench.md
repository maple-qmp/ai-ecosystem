---
title: τ-bench
type: concept
tags: [standard]
layer: X
aliases: ["τ-bench", "tau-bench", "τ²-bench", "tau2-bench", "τ-i18n"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# τ-bench

## 定义

Sierra 发布的“工具—Agent—用户”交互基准：Agent 在客服类场景中一边调用领域 API（查订单、改签机票等），一边与 LLM 模拟的用户多轮对话，并且必须遵守领域政策。原版（2024-06）含 retail、airline 两个领域；τ²-bench（2025-06）新增 telecom 领域，用户和 Agent 都能用工具操作同一个共享环境（“双控”）。

## 关键特征

- **pass^k 指标**：同一任务 k 次独立尝试全部成功的概率，衡量 Agent 的可靠性而不只是单次成功率
- **评测方式**：对话结束时比较数据库状态与标注的目标状态
- **发布时难度**：即使 gpt-4o 这类函数调用 Agent 成功率也不到 50%，且很不稳定（retail 领域 pass^8 不到 25%）
- **τ²-bench**：Telecom 领域建模为 Dec-POMDP；加入组合式任务生成器，以及受工具和可观测状态约束的用户模拟器；Agent 从“无用户”换到“双控”时成绩明显下降
- **τ-bench 2.0**（2026）：新增 τ-i18n，英、西、葡、印地、中、韩六种语言的文本与全双工语音版本；新增 `intake` 领域（外呼电话中准确采集姓名、地址等，200 多题）；新增事后评审（judges）和冻结的发布版任务集（如 `text-v1`、`voice-v2`）
- **官方实时榜**：taubench.com

## 应用

- 前沿模型发布时报告的工具调用 / Agent 指标；企业客服 Agent 选型参考
- 语音 Agent（实时模型）评测

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（对话式 Agent）
- **同类**：[[concepts/terminal-bench|Terminal-Bench]]、[[concepts/swe-bench|SWE-bench]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/terminal-bench|Terminal-Bench]]
- [[concepts/benchmark-contamination|基准污染与饱和]]

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/anthropic|Anthropic]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Our experiments show that even state-of-the-art function calling agents (like gpt-4o) succeed on <50% of the tasks, and are quite inconsistent (pass^8 <25% in retail)." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "τ-bench 2.0 adds **τ-i18n** (also called τ-multi): the same customer-service tasks in six languages, in text and in full-duplex voice, plus post-hoc judges for how the agent speaks." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
