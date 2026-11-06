---
title: ARC-AGI
type: concept
tags: [standard]
layer: X
aliases: ["ARC-AGI", "ARC-AGI-1", "ARC-AGI-2", "ARC-AGI-3", "ARC Prize", "Abstraction and Reasoning Corpus"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# ARC-AGI

## 定义

François Chollet 2019 年随论文《On the Measure of Intelligence》提出的抽象推理基准（Abstraction and Reasoning Corpus），目标是衡量“类人的流体智力”：每道题给几组输入 / 输出彩色网格示例，要求推出规则并为测试输入生成输出网格，每个测试输入允许 3 次尝试。目前由 ARC Prize 基金会维护，共三代：ARC-AGI-1、ARC-AGI-2 和交互式的 ARC-AGI-3。

## 关键特征

- **ARC-AGI-1**：训练集 400 题、评测集 400 题，网格 1×1 到 30×30，每格取值 0–9
- **ARC-AGI-2**：更难的静态网格版本；年度 Kaggle 竞赛的 85% 大奖在 2024、2025 两届均无人领取；2026-10 报道 Tufa Labs 在 Kaggle 公榜上达到 88.06%（只用约一半测试数据计算，为过渡分数）（二手）
- **ARC-AGI-3**：2026-03-24 发布，改为交互式回合制环境，Agent 须在没有明确指令的情况下探索、推断目标、建立环境动态模型并规划行动；只依赖“核心知识”先验，不用语言和外部知识；按人类行动基线计算效率分，100% 表示能像人类一样高效通关所有游戏。人类可解出 100% 的环境，截至 2026-03 前沿 AI 低于 1%（报道称发布时最好的 Gemini 3.1 Pro 为 0.37%，二手）
- **半私有 / 私有测试集**：竞赛成绩在不公开的测试集上计算，以减少污染和过拟合
- **开源要求**：领取奖金须开源方案

## 应用

- 衡量“举一反三”的泛化能力，而非知识储备；常被用来论证推理时计算扩展的效果和局限
- ARC Prize 2026：总奖金 200 万美元，三个赛道（ARC-AGI-3、ARC-AGI-2、论文奖）；2026-03-25 开赛，2026-11-02 截止提交，**2026-12-04 公布结果**；获奖方案须以 CC0、MIT-0 等宽松许可开源

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（抽象推理 / 交互）

## 相关概念

- [[concepts/reasoning-model|推理模型]]
- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/scaling-laws|规模定律]]

## 相关实体

- [[entities/gemini|Gemini]]
- [[entities/gpt|GPT]]
- [[entities/claude|Claude]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Our testing shows humans can solve 100% of the environments, in contrast to frontier AI systems which, as of March 2026, score below 1%." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
- "ARC can be seen as a general artificial intelligence benchmark, as a program synthesis benchmark, or as a psychometric intelligence test." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
