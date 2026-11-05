---
title: TRL
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["TRL", "Transformers Reinforcement Learning", "huggingface/trl"]
org: "[[entities/hugging-face]]"
released: "2020-03"
competitors: ["[[entities/axolotl]]", "[[entities/llama-factory]]", "[[entities/verl]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/deepspeed]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# TRL

## 描述

[[entities/hugging-face|Hugging Face]] 的后训练库，全称 Transformers Reinforcement Learning，自称“全面的基础模型后训练库”，构建在 transformers 生态之上。它提供 `SFTTrainer`、`GRPOTrainer`、`DPOTrainer`、`KTOTrainer` 等 trainer，覆盖[[concepts/supervised-fine-tuning|监督微调]]、[[concepts/grpo|GRPO]]、[[concepts/dpo|DPO]] 等方法；每个 trainer 是 transformers Trainer 的轻量封装，原生支持 DDP、[[entities/deepspeed|DeepSpeed]] ZeRO 和 FSDP，借 Accelerate 从单卡扩到多节点。与 PEFT 完整集成，可做 [[concepts/lora|LoRA]] / QLoRA 训练，并集成 [[entities/unsloth|Unsloth]] 内核加速。它也是生态里的底层依赖：Unsloth、[[entities/axolotl|Axolotl]]、[[entities/llama-factory|LLaMA-Factory]] 都把 trl 列为依赖。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练工具
- **上游依赖**：[[entities/pytorch|PyTorch]]、transformers、Accelerate、PEFT；可选 [[entities/deepspeed|DeepSpeed]]
- **竞争 / 替代**：[[entities/axolotl|Axolotl]]、[[entities/llama-factory|LLaMA-Factory]]（两者都构建在 TRL 之上，更偏配置驱动）、[[entities/verl|verl]]（大规模 RL）

## 时间线

- 2020-03-30 PyPI 首个版本 0.0.1
- 2022-05 0.1.0
- 2024-03 0.8.0
- 2025-01 0.14.0
- 2026-03-30 1.0.0：API 分为稳定区与 `trl.experimental` 孵化区，报道称实现了 75+ 种后训练方法（二手报道）
- 2026 年 README：经 PyTorch ROCm 支持 AMD Instinct GPU，经 TorchNeuron 支持 AWS Trainium；在单节点 8×B300 上对 Mistral Large 4、Reflection Beam 做 LoRA SFT
- 2026-10-30 1.17.1

## 相关实体

- [[entities/hugging-face|Hugging Face]]
- [[entities/unsloth|Unsloth]]
- [[entities/axolotl|Axolotl]]
- [[entities/llama-factory|LLaMA-Factory]]
- [[entities/verl|verl]]
- [[entities/deepseek-r1|DeepSeek-R1]]

## 相关概念

- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/grpo|GRPO]]
- [[concepts/dpo|DPO]]
- [[concepts/rlvr|RLVR]]
- [[concepts/lora|LoRA]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "A comprehensive library to post-train foundation models" — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "TRL is a cutting-edge library designed for post-training foundation models using advanced techniques like Supervised Fine-Tuning (SFT), Group Relative Policy Optimization (GRPO), and Direct Preference Optimization (DPO)." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
