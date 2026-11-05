---
title: MMLU / MMLU-Pro
type: concept
tags: [standard]
layer: X
aliases: ["MMLU", "MMLU-Pro", "Measuring Massive Multitask Language Understanding"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# MMLU / MMLU-Pro

## 定义

MMLU（Measuring Massive Multitask Language Understanding）是 Hendrycks 等 2020 年提出的 57 个学科四选一题基准，是 2021–2024 年衡量大模型知识面的事实标准。MMLU-Pro 是 TIGER-AI-Lab 2024 年的加强版（NeurIPS 2024）：加入更多推理型题目，选项从 4 个增加到 10 个，共 12,000 多道题。

## 关键特征

- **MMLU 历史分数**：随机基线 25%，GPT-3 175B few-shot 43.9%，Chinchilla 70B 67.5%（README 榜单）
- **MMLU-Pro 更难更稳**：相比 MMLU 准确率下降 16%–33%；对提示词变化的敏感度从 4–5% 降到 2%；使用思维链的模型得分更高
- **饱和**：MMLU 已饱和，前沿模型发布时多改报 MMLU-Pro 或多语言版本（二手）

## 应用

- 预训练基座模型的知识面对比；[[concepts/scaling-laws|规模定律]]相关论文常用的下游指标（Chinchilla 论文即以 MMLU 67.5% 为亮点）

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（知识）

## 相关概念

- [[concepts/gpqa|GPQA]]
- [[concepts/humanitys-last-exam|Humanity's Last Exam]]
- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/scaling-laws|规模定律]]

## 相关实体

- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gpt|GPT]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "MMLU-Pro integrates more challenging, reasoning-focused questions and increases the answer choices per question from four to ten, significantly raising the difficulty and reducing the chance of success through random guessing." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
