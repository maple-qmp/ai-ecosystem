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
updated: 2026-11-05
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# ARC-AGI

## 定义

François Chollet 2019 年随论文《On the Measure of Intelligence》提出的抽象推理基准（Abstraction and Reasoning Corpus），目标是衡量“类人的流体智力”：每道题给几组输入 / 输出彩色网格示例，要求推出规则并为测试输入生成输出网格，每个测试输入允许 3 次尝试。目前由 ARC Prize 基金会维护，共三代：ARC-AGI-1、ARC-AGI-2 和交互式的 ARC-AGI-3。

## 关键特征

- **ARC-AGI-1**：训练集 400 题、评测集 400 题，网格 1×1 到 30×30，每格取值 0–9
- **ARC-AGI-2**：更难的静态网格版本；年度 Kaggle 竞赛的 85% 大奖在 2024、2025 两届均无人领取；2026-10 报道 Tufa Labs 在 Kaggle 公榜上达到 88.06%（只用约一半测试数据计算，为过渡分数）（二手）
- **ARC-AGI-3**：2026-03 发布，改为交互式回合制游戏环境（报道称 135 个游戏、1,000 多个关卡），Agent 需通过 API 观察画面、执行动作、自行发现目标；人类可全部解出，发布时最好的模型仅 0.37%（二手）
- **半私有 / 私有测试集**：竞赛成绩在不公开的测试集上计算，以减少污染和过拟合
- **开源要求**：领取奖金须开源方案

## 应用

- 衡量“举一反三”的泛化能力，而非知识储备；常被用来论证推理时计算扩展的效果和局限
- ARC Prize 2026：总奖池 200 万美元，提交截止 2026-11-02，结果 2026-12-04 公布（二手）

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

- "ARC can be seen as a general artificial intelligence benchmark, as a program synthesis benchmark, or as a psychometric intelligence test." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
