---
title: DPO
type: concept
tags: [method]
layer: L3
aliases: ["DPO", "直接偏好优化", "Direct Preference Optimization", "偏好优化", "KTO", "ORPO", "SimPO", "IPO"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# DPO

## 定义

直接偏好优化：Rafailov 等（斯坦福）在 NeurIPS 2023 论文“Direct Preference Optimization: Your Language Model is Secretly a Reward Model”（arXiv 2305.18290）中提出的偏好对齐方法。论文证明 [[concepts/rlhf|RLHF]] 中“奖励模型 + 带 KL 约束的强化学习”这个目标有闭式最优解，奖励可以写成策略模型与参考模型的对数概率比，因此可以直接在偏好对（优选 / 劣选回答）上用一个分类式损失训练策略，不需要单独训练奖励模型，也不需要在训练中采样。

## 关键特征

- 两阶段流水线：先[[concepts/supervised-fine-tuning|监督微调]]，再在偏好数据上做偏好学习（最好与 SFT 数据同分布）
- 不需要奖励模型和在线采样，比 PPO 式 RLHF 简单、省显存；Tülu 3 的流水线为 SFT → DPO → [[concepts/rlvr|RLVR]]
- 离线方法：只用事先收集好的偏好数据，不像 [[concepts/grpo|GRPO]] 那样在线采样并用奖励打分
- 变体：conservative DPO（标签平滑）、IPO、KTO、ORPO、SimPO、GDPO 等

## 应用

- 聊天模型的偏好对齐、风格与安全调整
- 工具：[[entities/trl|TRL]] 的 `DPOTrainer`、`KTOTrainer`；[[entities/llama-factory|LLaMA-Factory]] 2023-08 支持 DPO，之后加入 ORPO、KTO、SimPO；[[entities/axolotl|Axolotl]] 支持 DPO、IPO、KTO、ORPO、GDPO；[[entities/unsloth|Unsloth]] 支持 DPO；[[entities/verl|verl]] 的 VeRL-Omni 用 DPO 训练全模态模型

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法
- **替代**：PPO 式 [[concepts/rlhf|RLHF]]

## 相关概念

- [[concepts/rlhf|RLHF]]
- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/grpo|GRPO]]
- [[concepts/rlvr|RLVR]]

## 相关实体

- [[entities/trl|TRL]]
- [[entities/llama-factory|LLaMA-Factory]]
- [[entities/axolotl|Axolotl]]
- [[entities/unsloth|Unsloth]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "In this paper we introduce a new parameterization of the reward model in RLHF that enables extraction of the corresponding optimal policy in closed form, allowing us to solve the standard RLHF problem with only a simple classification loss." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "This repo includes a reference implementation of the DPO algorithm for training language models from preference data" — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
