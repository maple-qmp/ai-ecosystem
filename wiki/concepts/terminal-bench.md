---
title: Terminal-Bench
type: concept
tags: [standard]
layer: X
aliases: ["Terminal-Bench", "Terminal-Bench 2.0", "tbench", "Harbor"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# Terminal-Bench

## 定义

评测 AI Agent 在真实终端（命令行）环境中自主完成端到端任务的基准，由 Laude Institute 与 Stanford 发起。每道题是一个容器化环境加一段任务描述，Agent 需自己执行命令完成编译代码、训练模型、搭服务器、修复安全漏洞等工作，最后由验证测试判定是否完成。

## 关键特征

- **两部分**：任务数据集 + 把模型接到终端沙箱的执行 harness
- **1.0**：beta 版，约 100 题，CLI 为 `tb`
- **2.0**（2025-11）：89 道题，每题有独立环境、人写的参考解和验证测试，经数百小时人工与 LLM 辅助验证；官方 harness 改为 Harbor（`harbor run --dataset terminal-bench@2.0`）（二手 + 一手）
- **按“Agent + 模型”排名**：同一模型换 harness 分数明显不同；2026-10 快照中 GPT-5.5 约 82% 居首，独立复测（Vals AI，Terminus 2 harness）分数更低（二手）
- README 称“几乎所有前沿实验室都在用”

## 应用

- 编程 Agent 与通用 Agent 的能力对比；[[concepts/agent-harness|Agent Harness]] 设计的直接试金石
- Harbor 格式也被 [[concepts/swe-bench|SWE-bench Pro]] V2 采用

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（Agent / 终端）
- **同类**：[[concepts/swe-bench|SWE-bench]]、[[concepts/tau-bench|τ-bench]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/swe-bench|SWE-bench]]

## 相关实体

- [[entities/codex-cli|Codex CLI]]
- [[entities/claude-code|Claude Code]]
- [[entities/gpt|GPT]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Terminal-Bench is the benchmark for testing AI agents in real terminal environments." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "It is used by virtually all frontier labs." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
