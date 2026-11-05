---
title: LLaMA-Factory
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["LLaMA-Factory", "LlamaFactory", "llamafactory", "hiyouga/LLaMA-Factory"]
released: "2023"
competitors: ["[[entities/axolotl]]", "[[entities/unsloth]]", "[[entities/trl]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/trl]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# LLaMA-Factory

## 描述

北京航空航天大学郑耀威（hiyouga）主导的统一高效微调框架，论文“LlamaFactory: Unified Efficient Fine-Tuning of 100+ Language Models”发表于 ACL 2024 系统演示（arXiv 2403.13372）。它把（继续）[[concepts/pretraining|预训练]]、（多模态）[[concepts/supervised-fine-tuning|监督微调]]、奖励建模、PPO、[[concepts/dpo|DPO]]、KTO、ORPO、SimPO 等方法与全量、冻结、[[concepts/lora|LoRA]]、2–8 bit QLoRA 等调参方式组合成一张支持矩阵，模型覆盖 [[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/deepseek|DeepSeek]]、[[entities/glm|GLM]]、Gemma 等，并为新模型提供 Day 0 / Day 1 支持。附带 Web UI LlamaBoard，推理可接 [[entities/vllm|vLLM]] 或 [[entities/sglang|SGLang]] worker；也可调用 [[entities/unsloth|Unsloth]]、Liger Kernel 等加速。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练工具
- **上游依赖**：[[entities/pytorch|PyTorch]]、transformers、PEFT、[[entities/trl|TRL]]、Accelerate；可选 [[entities/deepspeed|DeepSpeed]]、bitsandbytes、[[entities/vllm|vLLM]]；2025-10 起可用 [[entities/megatron-lm|Megatron]] Core 作训练后端
- **竞争 / 替代**：[[entities/axolotl|Axolotl]]、[[entities/unsloth|Unsloth]]

## 时间线

- 2023-08-11 支持 DPO
- 2023-10 支持 NEFTune
- 2024-02 支持 DoRA
- 2024-03 支持 GaLore、LoRA+、ORPO；2024-03-21 论文上线 arXiv
- 2024-05 支持昇腾 NPU、KTO、SimPO；2024-05-16 PyPI 首个版本 0.7.1
- 2024-06 支持 PiSSA
- 2025-01 支持 APOLLO 优化器
- 2025-08 支持 OFT / OFTv2
- 2025-10-26 支持 Megatron-core 训练后端（经阿里 ROLL 的 mcore_adapter）
- 2026-05-30 发布 0.9.5

## 相关实体

- [[entities/trl|TRL]]
- [[entities/axolotl|Axolotl]]
- [[entities/unsloth|Unsloth]]
- [[entities/qwen|Qwen]]
- [[entities/alibaba|阿里巴巴（通义）]]

## 相关概念

- [[concepts/lora|LoRA]]
- [[concepts/quantization|量化]]
- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/dpo|DPO]]
- [[concepts/rlhf|RLHF]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "(Continuous) pre-training, (multimodal) supervised fine-tuning, reward modeling, PPO, DPO, KTO, ORPO, etc." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
