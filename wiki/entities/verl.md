---
title: verl
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["verl", "Volcano Engine Reinforcement Learning for LLMs", "HybridFlow", "verl-project/verl", "volcengine/verl"]
org: "[[entities/bytedance]]"
released: "2024"
competitors: ["[[entities/trl]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/megatron-lm]]", "[[entities/vllm]]", "[[entities/sglang]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# verl

## 描述

[[entities/bytedance|字节跳动]] Seed 团队发起、verl 社区维护的 LLM 强化学习训练库（Volcano Engine Reinforcement Learning for LLMs），是 EuroSys 2025 论文 HybridFlow（arXiv 2409.19256）的开源实现，Apache-2.0。它用“混合控制器”编程模型把 RL 数据流拆成训练与生成两部分：训练后端用 FSDP / FSDP2 / [[entities/megatron-lm|Megatron-LM]]，rollout 生成用 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]] 或 HF Transformers，3D-HybridEngine 在两阶段切换时对 actor 模型重分片以消除显存冗余。算法覆盖 PPO、[[concepts/grpo|GRPO]]、GSPO、RLOO、REINFORCE++、DAPO、DrGRPO 等，支持模型奖励与[[concepts/rlvr|可验证奖励]]、多模态 RL 和多轮工具调用，能借专家并行扩展到 671B 模型和数百张 GPU。字节的豆包 1.5 Pro RL 预览模型、Seed-Thinking-v1.5、DAPO、VAPO 都用它训练。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练工具（RL 框架）
- **上游依赖**：[[entities/pytorch|PyTorch]]、Ray、[[entities/megatron-lm|Megatron-LM]]（可选训练后端）、[[entities/vllm|vLLM]] / [[entities/sglang|SGLang]]（rollout）
- **竞争 / 替代**：[[entities/trl|TRL]]（更轻量的通用后训练库）；SGLang 生态中的 Miles、slime、AReaL

## 时间线

- 2024-09-28 HybridFlow 论文提交 arXiv，摘要称在多种 RLHF 算法上比现有基线吞吐提升 1.53–20.57 倍
- 2024-11-01 PyPI 首个版本 0.1rc0
- 2025-01 豆包 1.5 Pro 的 RL scaling 预览模型用 verl 训练（AIME pass@1 70.0）
- 2025-03 DAPO 发布（完全基于 verl）；v0.3.0.post1 约 1.4 倍提速；论文在 EuroSys 2025 发表
- 2025-04 Seed-Thinking-v1.5（AIME 2024 86.7）、VAPO
- 2025-06 Megatron 后端支持 DeepSeek-671B、Qwen3-235B 等大型 MoE
- 2025-12 Mind Lab 用 verl + Megatron-Bridge 在 64 张 H800 上做万亿参数模型的 GRPO LoRA
- 2026-01 迁入 verl-project 组织，recipe 拆为独立仓库 verl-recipe；首届 meetup（上海，火山引擎与 NVIDIA 主办）
- 2026-03 NVIDIA GTC26 演讲
- 2026-05 uni-agent（大规模训练 LLM agent）、VeRL-Omni 预发布（扩散与全模态 RL）
- 2026-06 verl-SpeCo：RL 训练中协同训练[[concepts/speculative-decoding|推测解码]]草稿模型
- 2026-08 verl-vla v0.1.0、VeRL-Tinker（SFT、RL、蒸馏）、VeRL-Omni v0.2.0
- 2026-09-20 发布 0.9.1

## 相关实体

- [[entities/bytedance|字节跳动]]
- [[entities/doubao|豆包]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/megatron-lm|Megatron-LM]]
- [[entities/trl|TRL]]

## 相关概念

- [[concepts/grpo|GRPO]]
- [[concepts/rlvr|RLVR]]
- [[concepts/rlhf|RLHF]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/knowledge-distillation|知识蒸馏]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "verl is a flexible, efficient and production-ready RL training library for large language models (LLMs)." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "Build RL dataflows such as GRPO, PPO in a few lines of code." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "Eliminates memory redundancy and significantly reduces communication overhead during transitions between training and generation phases." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
