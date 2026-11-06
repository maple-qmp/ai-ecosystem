---
title: Terminal-Bench
type: concept
tags: [standard]
layer: X
aliases: ["Terminal-Bench", "Terminal-Bench 2.0", "Terminal-Bench 3.0", "Terminal-Bench 4.0", "tbench", "Harbor"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# Terminal-Bench

## 定义

评测 AI Agent 在真实终端（命令行）环境中自主完成端到端任务的基准，由 Stanford 与 Laude Institute 主持。每道题是一个容器化环境加任务描述，Agent 自己执行命令完成编译代码、训练模型、搭服务器、修复安全漏洞等工作，最后由验证测试判定。2026 年起改为“持续基准”：按语义化版本持续修复、删除和新增任务，目前是 4.0。

## 关键特征

- **两部分**：任务数据集，加上把模型接到终端沙箱的执行 harness（2.0 起为 Harbor）
- **按“Agent + 模型”排名**：同一模型换 harness 成绩明显不同
- **持续基准**：把基准当软件维护，尽早发布、频繁修复、删除饱和任务，用复用、重判、重跑迁移排行榜结果
- **排行榜诚信规则**（2026-04-19）：通过的试验必须附 ATIF 轨迹，用 Agent 评审检查。奖励投机（如上网找答案）的试验记 0 分，作弊的提交直接下架。已处理的案例有：OB-1 在 Agent 二进制里存加密答案，Pilot 把 tests/ 目录带进 Agent 环境，ForgeCode 的 Agent 把从网上 curl 来的答案写进 AGENTS.md
- **饱和定义**（4.0）：最新一代所有模型家族每次都 5/5 解出的任务，视为饱和并删除

## 时间线

- 2025-05 发布 1.0（约 100 题）
- 2025-11-07 发布 2.0（89 题，经大量人工与 LLM 辅助验证）与 Harbor；论文（2026-01-17）报告前沿模型与 Agent 得分低于 65%
- 2026-04-19 排行榜诚信更新
- 2026-05-06 发布 2.1，修复 28 道题
- 2026-07-30 发布 3.0：74 道题、7 个领域，含多容器网络与 GPU 环境，最好成绩约 34%（GPT-5.6 Sol + Codex 34.4%，[[entities/claude|Fable 5]] + [[entities/claude-code|Claude Code]] 33.8%）
- 2026-08-28 发布 4.0：统一 8 小时超时，删除 8 道题（其中 2 道饱和），修复 19 道题；计划中的 4.1 加入防篡改验证器，5.0 加新任务

## 应用

- 编程 Agent 与通用 Agent 的能力对比；检验 [[concepts/agent-harness|Agent Harness]] 设计
- Harbor 格式也被 [[concepts/swe-bench|SWE-Bench Pro]] V2 采用

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（Agent / 终端）
- **同类**：[[concepts/swe-bench|SWE-bench]]、[[concepts/tau-bench|τ-bench]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/swe-bench|SWE-bench]]
- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/agents-md|AGENTS.md]]

## 相关实体

- [[entities/codex-cli|Codex CLI]]
- [[entities/claude-code|Claude Code]]
- [[entities/gpt|GPT]]
- [[entities/claude|Claude]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "we present Terminal-Bench 2.0: a carefully curated hard benchmark composed of 89 tasks in computer terminal environments inspired by problems from real workflows." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "Reward hacking will result in a reward of 0 for a trial (e.g. finding solutions on the internet)" — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "Benchmarks are software and should be maintained like software" — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
