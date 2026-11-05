---
title: SWE-bench
type: concept
tags: [standard]
layer: X
aliases: ["SWE-bench", "SWE-bench Verified", "SWE-bench Pro", "SWE-bench Multimodal"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# SWE-bench

## 定义

用 GitHub 真实 issue 评测模型软件工程能力的基准：给定一个代码库和一条 issue，模型生成补丁，再用仓库自带的单元测试判断问题是否解决。Princeton 团队发布（ICLR 2024 Oral），MIT 协议，是编程模型和编程 Agent 发布时最常引用的指标之一。

## 关键特征

- **评测方式**：只看补丁能否让指定的失败测试通过且不破坏其他测试；2024-06 起改为 Docker 容器化评测，提高可复现性
- **SWE-bench Verified**（2024-08-13）：与 [[entities/openai|OpenAI]] Preparedness 团队合作，从原测试集中挑出 500 道经真人软件工程师确认可解的题，一度是事实标准
- **SWE-bench Multimodal**：带截图等视觉信息的前端类任务；2026-09-01 发布 v2，480 道题完全开源
- **SWE-bench Pro**（Scale AI）：面向长程任务的更难版本，分公开榜和商业私有榜；2026-09-22 发布 V2，642 道验证过的任务，改用 Harbor 格式，含 HARD-51 子集和锁定评测协议
- **分数依赖 harness**：同一模型换 Agent 脚手架、工具权限、超时设置，分数差别很大

## 应用

- 前沿模型和编程 Agent（如 [[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex CLI]]）的能力宣传与横向对比
- 研究编程 Agent 的脚手架设计（SWE-agent、mini-swe-agent）

## 时间线

- 2023-10 论文发布；2024-01 ICLR 2024 接收为 Oral
- 2024-04-02 发布 SWE-agent
- 2024-08-13 发布 SWE-bench Verified
- 2025-01-13 并入 Multimodal，发布云端提交工具 sb-cli
- 2026-02-23 OpenAI 宣布停止报告 Verified 分数，理由是污染和题目缺陷，改为推荐 SWE-bench Pro（二手）
- 2026-09 Multimodal v2 开源；SWE-bench Pro V2 发布

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

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "SWE-bench is a benchmark for evaluating large language models on real world software issues collected from GitHub." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "A subset of 500 problems that real software engineers have confirmed are solvable." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "SWE-Bench Pro is a challenging benchmark evaluating LLMs/Agents on long-horizon software engineering tasks." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
