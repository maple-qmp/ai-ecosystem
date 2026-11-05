---
title: LoRA
type: concept
tags: [method]
layer: L3
aliases: ["LoRA", "Low-Rank Adaptation", "低秩适配", "QLoRA"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# LoRA

## 定义

[[entities/microsoft|微软]]研究者 Edward J. Hu 等 2021 年提出的参数高效微调方法（论文“LoRA: Low-Rank Adaptation of Large Language Models”，arXiv 2106.09685）：冻结原模型权重，只为权重矩阵学习一对低秩分解矩阵。可训练参数大幅减少，每个任务只需存一份很小的适配器，部署时可以高效切换任务；低秩矩阵能合并回原权重，因此不引入推理延迟。

## 关键特征

- 参数量：论文 README 的 GLUE 实验中，RoBERTa base 全量微调训练 125M 参数，LoRA 只训练 0.8M，平均分 87.24 对 86.40；DeBERTa XXL 1.5B 对 4.7M，91.32 对 91.06；效果好于 adapter、prefix-tuning 和全量微调
- 官方包 `loralib` 只支持 [[entities/pytorch|PyTorch]]；2023-02 起 [[entities/hugging-face|Hugging Face]] 的 PEFT 库支持 LoRA，此后成为各训练工具的标准功能
- **QLoRA**（Dettmers 等，华盛顿大学，2023-05，arXiv 2305.14314）：把梯度反向传播穿过冻结的 4-bit [[concepts/quantization|量化]]模型进入 LoRA 适配器，单张 48GB GPU 可微调 65B 模型并保持 16-bit 全量微调的性能；三项省显存技术为 4-bit NormalFloat（NF4）、双重量化、分页优化器；量化由 bitsandbytes 实现
- 变体：DoRA、LoRA+、rsLoRA、PiSSA、LoftQ、LongLoRA（[[entities/llama-factory|LLaMA-Factory]] 均支持）；MixLoRA、MoE 专家权重上的 LoRA、NVFP4 LoRA（[[entities/axolotl|Axolotl]]，2026）
- 显存（LLaMA-Factory 估算，7B 模型）：全量 bf16/fp16 约 120GB，LoRA 约 16GB，4-bit QLoRA 约 6GB

## 应用

- 开源模型的领域微调、风格与角色定制：[[entities/trl|TRL]]、[[entities/unsloth|Unsloth]]、[[entities/axolotl|Axolotl]]、[[entities/llama-factory|LLaMA-Factory]] 都支持 LoRA / QLoRA
- 强化学习中省显存：[[entities/verl|verl]] 支持多 GPU LoRA RL，有团队用它对万亿参数模型做 [[concepts/grpo|GRPO]] LoRA
- 多 LoRA 服务：[[entities/vllm|vLLM]] 可在同一个基座上同时服务多个 LoRA 适配器

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法

## 相关概念

- [[concepts/quantization|量化]]
- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/grpo|GRPO]]

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/llama|Llama]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/trl|TRL]]
- [[entities/unsloth|Unsloth]]
- [[entities/llama-factory|LLaMA-Factory]]

## 我的判断

## 来源摘录

- "LoRA reduces the number of trainable parameters by learning pairs of rank-decompostion matrices while freezing the original weights." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "This vastly reduces the storage requirement for large language models adapted to specific tasks and enables efficient task-switching during deployment all without introducing inference latency." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "QLoRA backpropagates gradients through a frozen, 4-bit quantized pretrained language model into Low Rank Adapters (LoRA)." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
