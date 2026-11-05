---
title: GRPO
type: concept
tags: [method]
layer: L3
aliases: ["GRPO", "组相对策略优化", "Group Relative Policy Optimization", "DAPO", "GSPO", "Dr.GRPO"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# GRPO

## 定义

组相对策略优化：[[entities/deepseek|DeepSeek]] 在 DeepSeekMath 论文（2024-02，arXiv 2402.03300）中提出的强化学习算法，DeepSeekMath-RL 7B 即用它训练。GRPO 是 PPO 的变体：对同一个问题采样一组回答，以组内平均奖励为基线，奖励减去组均值、再除以组标准差，得到每个回答的相对优势，以此替代 PPO 中的价值（critic）模型，省掉一个与策略同等规模的模型。[[entities/deepseek-r1|DeepSeek-R1]]（2025-01，arXiv 2501.12948）用大规模 RL 训练出长思维链，使 GRPO 成为[[concepts/reasoning-model|推理模型]]训练的标准算法。

## 关键特征

- 比 PPO 省显存（[[entities/trl|TRL]] 的说法）；只需策略、参考模型和奖励函数
- 常与[[concepts/rlvr|可验证奖励]]搭配：奖励来自答案比对、单元测试等规则，而不是奖励模型
- DeepSeek-R1-Zero 直接在基座模型上做 RL、不经过 SFT，自发出现自我验证、反思和长思维链，DeepSeek 称这是第一个公开验证“推理能力可以纯靠 RL 激发”的研究；但 R1-Zero 有无限重复、可读性差、语言混杂的问题，R1 在 RL 前加入冷启动数据
- 变体与改进：DAPO（字节 Seed 与清华 AIR，2025-03，arXiv 2503.14476；基于 Qwen2.5-32B 基座在 AIME 2024 上拿到 50 分，超过 DeepSeek-R1-Zero-Qwen-32B 且训练步数少一半，完全基于 [[entities/verl|verl]]）、Dr.GRPO、GSPO；基于价值的 VAPO 则走回 PPO 路线（AIME 2024 60.4）

## 应用

- 数学、代码、推理能力的强化学习后训练
- 工具：[[entities/trl|TRL]] 的 `GRPOTrainer`；[[entities/unsloth|Unsloth]]（gpt-oss 20B GRPO 笔记本称快 2 倍、省 80% 显存）；[[entities/axolotl|Axolotl]]（2025-02 起支持，2026-04 加入异步 GRPO）；[[entities/verl|verl]]（GRPO、DAPO、DrGRPO、GSPO 等）；Ai2 的 open-instruct 用 GRPO 实现 RLVR
- rollout 生成依赖推理引擎：verl 用 [[entities/vllm|vLLM]] 或 [[entities/sglang|SGLang]] 采样

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法
- **改进对象**：[[concepts/rlhf|RLHF]] 中的 PPO

## 相关概念

- [[concepts/rlvr|RLVR]]
- [[concepts/rlhf|RLHF]]
- [[concepts/dpo|DPO]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/knowledge-distillation|知识蒸馏]]

## 相关实体

- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/trl|TRL]]
- [[entities/verl|verl]]
- [[entities/unsloth|Unsloth]]
- [[entities/axolotl|Axolotl]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "GRPO foregoes the critic model, instead estimating the baseline from group scores, significantly reducing training resources." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "DeepSeekMath-RL 7B is trained on the foundation of DeepSeekMath-Instruct 7B, utilizing our proposed Group Relative Policy Optimization (GRPO) algorithm." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "Notably, it is the first open research to validate that reasoning capabilities of LLMs can be incentivized purely through RL, without the need for SFT." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
