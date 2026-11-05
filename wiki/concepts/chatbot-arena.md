---
title: Chatbot Arena（LMArena）
type: concept
tags: [standard]
layer: X
aliases: ["Chatbot Arena", "LMArena", "Arena", "LMSYS Chatbot Arena", "Arena Intelligence"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# Chatbot Arena（LMArena）

## 定义

众包的大模型“盲测对战”评测平台：用户输入同一个问题，同时看到两个匿名模型的回答，投票选出更好的一方，平台据此计算排行榜。2023-05 由 LMSYS 推出，2025 年成立公司 Arena Intelligence Inc. 以 LMArena 品牌运营，2026-01-28 改名 **Arena**，主域名迁到 arena.ai。

## 关键特征

- **人类偏好而非标准答案**：衡量的是真实用户觉得哪个回答更好，覆盖开放式对话、写作、编程等难以自动判分的场景
- **规模**：服务框架 FastChat 的 README 称已收集超过 150 万张对战投票；后来扩展出文生图、视觉、WebDev 等分榜
- **公开数据**：发布过 Chatbot Arena Conversations 等带人类偏好标注的对话数据集
- **争议**：2025-04 Cohere Labs 等发表《The Leaderboard Illusion》，指出少数厂商可以私下测试多个变体、只公开最好的一个，且公开榜上的版本不一定与对外发布的模型一致；Arena 方回应称该政策是为了防止厂商只报告测试中的最高分

## 应用

- 新模型上线前的匿名测试与上线后的排名宣传
- 作为偏好数据来源，用于研究奖励模型和自动评审（如 Arena-Hard）

## 时间线

- 2023-05 LMSYS 推出 Chatbot Arena
- 2024-03 发布技术报告
- 2025-04-29 《The Leaderboard Illusion》发表
- 2025-05 公司化，种子轮 1 亿美元（二手）
- 2026-01-06 A 轮 1.5 亿美元，投后估值约 17 亿美元（二手）
- 2026-01-28 改名 Arena

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 评测基准（人类偏好）
- **同类 / 互补**：静态基准 [[concepts/mmlu|MMLU]]、[[concepts/gpqa|GPQA]]；Agent 基准 [[concepts/swe-bench|SWE-bench]]

## 相关概念

- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/mmlu|MMLU / MMLU-Pro]]

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/anthropic|Anthropic]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/meta-ai|Meta AI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Chatbot Arena has collected over 1.5M human votes from side-by-side LLM battles to compile an online LLM Elo leaderboard." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]
