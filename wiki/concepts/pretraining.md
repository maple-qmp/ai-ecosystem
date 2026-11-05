---
title: 预训练
type: concept
tags: [method]
layer: L3
aliases: ["预训练", "Pretraining", "Pre-training", "继续预训练", "Continual pre-training"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# 预训练

## 定义

在海量无标注文本上做下一个 token 预测（自回归语言建模），从随机初始化训练出基座模型的阶段。模型的知识和通用能力主要在这一步形成，绝大部分训练算力也花在这里；之后的[[concepts/supervised-fine-tuning|监督微调]]、[[concepts/rlhf|RLHF]]、[[concepts/grpo|GRPO]] 等后训练都在基座模型上进行。在已有基座上用领域语料接着训练称为继续预训练。

## 关键特征

- 目标简单（预测下一个 token），难点在规模：数据量、参数量与算力的配比由[[concepts/scaling-laws|规模定律]]指导
- 需要多维并行：张量、流水线、数据、专家、上下文并行，以及 ZeRO / FSDP 式的状态切分
- 产出的基座模型只会续写，不会按指令回答，要靠后训练变成可用的助手或[[concepts/reasoning-model|推理模型]]

## 应用

- 训练基础模型：大规模预训练用 [[entities/megatron-lm|Megatron-LM]]、[[entities/deepspeed|DeepSpeed]] 和 PyTorch FSDP
- 继续预训练：[[entities/llama-factory|LLaMA-Factory]] 支持全量、冻结、LoRA、QLoRA 等方式的（继续）预训练；[[entities/unsloth|Unsloth]] 也列出预训练；[[entities/axolotl|Axolotl]] 2025-12 为 FSDP2 预训练加入分布式 Muon 优化器

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法
- **下一步**：[[concepts/supervised-fine-tuning|监督微调（SFT）]]

## 相关概念

- [[concepts/scaling-laws|规模定律]]
- [[concepts/transformer|Transformer]]
- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/knowledge-distillation|知识蒸馏]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 相关实体

- [[entities/megatron-lm|Megatron-LM]]
- [[entities/deepspeed|DeepSpeed]]
- [[entities/pytorch|PyTorch]]
- [[entities/llama-factory|LLaMA-Factory]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "(Continuous) pre-training, (multimodal) supervised fine-tuning, reward modeling, PPO, DPO, KTO, ORPO, etc." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
