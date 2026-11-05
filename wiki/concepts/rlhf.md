---
title: RLHF
type: concept
tags: [method]
layer: L3
aliases: ["RLHF", "基于人类反馈的强化学习", "Reinforcement Learning from Human Feedback", "奖励模型", "Reward model", "PPO"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# RLHF

## 定义

基于人类反馈的强化学习：先让人对模型的多个输出排序，用排序数据训练一个奖励模型，再以奖励模型的打分为奖励、用强化学习（通常是 PPO）微调语言模型。OpenAI 的 InstructGPT（2022，arXiv 2203.02155）确立了大模型上的三阶段流程：① 用标注员示范做[[concepts/supervised-fine-tuning|监督微调]]；② 训练奖励模型；③ PPO 强化学习。

## 关键特征

- InstructGPT 的结果：在其提示分布上，1.3B 参数的 InstructGPT 比 175B 的 GPT-3 更受人偏好，参数少 100 倍；真实性提高、有害输出减少，公开 NLP 数据集上的性能退化很小
- 工程代价高：PPO 要同时维护策略、参考、奖励、价值（critic）四个模型，训练中还要在线采样
- 后续方法都在简化它：[[concepts/dpo|DPO]] 去掉奖励模型和在线采样；[[concepts/grpo|GRPO]] 去掉价值模型；[[concepts/rlvr|RLVR]] 用可验证的规则奖励替代学习到的奖励模型

## 应用

- 对齐聊天模型的有用性、无害性与风格
- 工具：[[entities/llama-factory|LLaMA-Factory]] 支持奖励建模与 PPO；[[entities/verl|verl]] 支持 PPO，其论文 HybridFlow 的标题即“A Flexible and Efficient RLHF Framework”；[[entities/axolotl|Axolotl]] 支持奖励模型与过程奖励模型（PRM）

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法
- **替代 / 简化**：[[concepts/dpo|DPO]]、[[concepts/grpo|GRPO]]、[[concepts/rlvr|RLVR]]

## 相关概念

- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/dpo|DPO]]
- [[concepts/grpo|GRPO]]
- [[concepts/rlvr|RLVR]]

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/verl|verl]]
- [[entities/llama-factory|LLaMA-Factory]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We then collect a dataset of rankings of model outputs, which we use to further fine-tune this supervised model using reinforcement learning from human feedback (RLHF)." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "outputs from the 1.3B parameter InstructGPT model are preferred to outputs from the 175B GPT-3, despite having 100x fewer parameters." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
