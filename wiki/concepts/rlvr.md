---
title: RLVR
type: concept
tags: [method]
layer: L3
aliases: ["RLVR", "可验证奖励强化学习", "Reinforcement Learning with Verifiable Rewards", "可验证奖励"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# RLVR

## 定义

可验证奖励强化学习：奖励不来自学习到的奖励模型，而来自能自动检验对错的规则或程序（答案比对、单元测试、格式检查），模型的回答被验证为正确才给奖励。名称出自 Ai2 的 Tülu 3 论文（2024-11，arXiv 2411.15124），在那里作为 SFT → DPO 之后的最后一个后训练阶段，用于数学、精确指令遵循等答案可检验的技能；Tülu 3 基于 Llama 3.1 基座，开放了权重、数据、代码和评测工具。

## 关键特征

- 与 [[concepts/rlhf|RLHF]] 的区别：不需要人工偏好标注，也不训练奖励模型，因此更难被“奖励黑客”钻空子；代价是只适用于答案能自动判定的任务
- 与 [[concepts/grpo|GRPO]] 正交：RLVR 回答“奖励从哪来”，GRPO / PPO 回答“怎么用奖励更新策略”；实践中常组合使用（open-instruct 用 GRPO 跑 RLVR）
- [[entities/deepseek-r1|DeepSeek-R1]] 一类[[concepts/reasoning-model|推理模型]]的 RL 阶段也以规则奖励为主（二手说法，R1 论文原文未核对）

## 应用

- 数学、代码、精确指令遵循、可执行的 agent 任务
- 工具：[[entities/verl|verl]] 支持“函数奖励（可验证奖励）”用于数学与代码；[[entities/trl|TRL]] 提供 `accuracy_reward`（依赖 math-verify）和面向推理模型的 `reasoning_accuracy_reward()`；Ai2 open-instruct 的 `grpo_fast.py`

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法

## 相关概念

- [[concepts/grpo|GRPO]]
- [[concepts/rlhf|RLHF]]
- [[concepts/dpo|DPO]]
- [[concepts/reasoning-model|推理模型]]

## 相关实体

- [[entities/verl|verl]]
- [[entities/trl|TRL]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/llama|Llama]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Code for DPO, preference finetuning and reinforcement learning with verifiable rewards (RLVR)." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
