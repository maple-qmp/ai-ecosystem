---
title: SWE-bench
type: concept
tags: [standard]
layer: X
aliases: ["SWE-bench", "SWE-bench Verified", "SWE-bench Pro", "SWE-Bench Pro", "SWE-bench Multimodal", "SWE-bench Lite"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# SWE-bench

## 定义

用真实 GitHub issue 评测模型软件工程能力的基准：原始测试集有 2,294 道题，来自 12 个流行 Python 仓库的 issue 及对应 PR。给定代码库和 issue 描述，模型修改代码，再用仓库自带测试判断问题是否解决。Princeton 团队发布（arXiv 2023-10，ICLR 2024 Oral），MIT 协议。论文发布时最好的模型 Claude 2 只解决 1.96%。

## 关键特征

- **子集**：Verified 500 题（人工确认可解，2024-08-13 与 [[entities/openai|OpenAI]] Preparedness 团队合作发布）、Lite 300 题、Multilingual 300 题（42 个仓库、9 种语言）、Multimodal 480 题
- **Bash Only 视图**：所有模型在同一个 mini-SWE-agent 环境里运行，比较的是模型而不是 harness
- **官方 Verified 榜现状**（2026-11-05 读取）：共 180 条记录，最后一次提交在 2026-02-26。最高 79.2%（Claude 4.5 Opus 配 Sonar Foundation Agent 或 live-SWE-agent，2025-12）；Bash Only 视图最高 76.8%（Claude 4.5 Opus high，2026-02-17）。2026 年模型发布材料和聚合站引用的 90% 以上的 Verified 分数，官方榜都没有收录
- **SWE-Bench Pro**（Scale AI）：面向长程任务，分公开榜和商业私有榜；2026-09-22 发布 V2，642 道验证过的任务，改用 Harbor 格式。公开榜 2026-11 的榜首是 [[entities/muse|Muse Spark]] 1.1，61.50±3.10%，其次 gpt-5.4 (xHigh) 59.10%、claude-opus-4-6 (thinking) 51.90%
- **分数依赖 harness**：同一模型换脚手架、工具权限或超时设置，分数差别很大

## 应用

- 前沿模型和编程 Agent（如 [[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex CLI]]）的能力宣传与横向对比
- 研究编程 Agent 脚手架（SWE-agent、mini-swe-agent），以及训练数据合成（SWE-smith）

## 时间线

- 2023-10-10 论文发布；2024-01 ICLR 2024 接收为 Oral
- 2024-03 发布 Lite 与 SWE-agent；2024-06 改用 Docker 评测
- 2024-08-13 发布 SWE-bench Verified；2024-10 发布 Multimodal
- 2026-02-23 OpenAI 宣布停止报告 Verified，理由是污染和题目缺陷，改为推荐 SWE-bench Pro（二手）；官方 Verified 榜此后没有新提交
- 2026-05 发布 ProgramBench；2026-09 Multimodal v2 开源、SWE-Bench Pro V2 发布

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（编程）
- **同类**：[[concepts/terminal-bench|Terminal-Bench]]（终端任务）、[[concepts/tau-bench|τ-bench]]（客服 Agent）

## 相关概念

- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/terminal-bench|Terminal-Bench]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/claude-code|Claude Code]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/muse|Muse]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "we introduce SWE-bench, an evaluation framework consisting of $2,294$ software engineering problems drawn from real GitHub issues and corresponding pull requests across $12$ popular Python repositories." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "The default Verified view: every model in the same mini-SWE-agent environment." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "SWE-Bench Pro is a challenging benchmark evaluating LLMs/Agents on long-horizon software engineering tasks." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
