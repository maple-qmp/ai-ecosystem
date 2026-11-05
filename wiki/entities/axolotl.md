---
title: Axolotl
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["Axolotl", "axolotl-ai-cloud/axolotl"]
released: "2023"
competitors: ["[[entities/llama-factory]]", "[[entities/unsloth]]", "[[entities/trl]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/trl]]", "[[entities/deepspeed]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# Axolotl

## 描述

自由开源的 LLM 后训练与微调工具（Apache-2.0），特点是用一个 YAML 配置文件贯穿数据预处理、训练、评估、量化和推理全流程。训练方法覆盖全量微调、[[concepts/lora|LoRA]]、QLoRA、GPTQ、量化感知训练（int8 / int4 / FP8 / NVFP4 / MXFP4）、FP8 混合精度、偏好调优（[[concepts/dpo|DPO]]、IPO、KTO、ORPO）、强化学习（[[concepts/grpo|GRPO]]、GDPO）以及奖励模型 / 过程奖励模型。性能方面集成 Flash Attention 2/3/4、Liger Kernel、多样本打包、序列并行，多卡用 FSDP2 / [[entities/deepspeed|DeepSpeed]]，多节点用 Torchrun / Ray，并支持 CP + TP + FSDP 组合的 ND 并行和面向 [[concepts/mixture-of-experts|MoE]] 的专家并行。2026 年的更新集中在 MoE 与低精度：MoE 专家权重上的 LoRA、NVFP4 LoRA、专家量化，以及导出 [[concepts/gguf|GGUF]] 供 [[entities/llama-cpp|llama.cpp]] 和 [[entities/ollama|Ollama]] 部署。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练工具
- **上游依赖**：[[entities/pytorch|PyTorch]]（≥2.13）、transformers、PEFT、[[entities/trl|TRL]]、bitsandbytes、Triton、torchao；可选 [[entities/deepspeed|DeepSpeed]]、Ray、[[entities/vllm|vLLM]]
- **竞争 / 替代**：[[entities/llama-factory|LLaMA-Factory]]、[[entities/unsloth|Unsloth]]、直接用 [[entities/trl|TRL]]

## 时间线

- 2023 项目开始（README 引用条目年份）
- 2024-11-08 PyPI 首个版本 0.5.0
- 2025-01 奖励模型 / 过程奖励模型微调
- 2025-02 GRPO
- 2025-03 序列并行、多模态微调（beta）
- 2025-05 量化感知训练（QAT）
- 2025-07 ND 并行、FP8 微调、gpt-oss 支持
- 2025-09 文本扩散模型训练
- 2026-02 ScatterMoE LoRA、GDPO
- 2026-04 异步 GRPO（步时最多快 58%）、Flash Attention 4，改为 uv 优先
- 2026-06 专家并行（DeepEP）、Tinker 兼容 API 远程训练、BitNet 1.58-bit 微调
- 2026-09 `axolotl export` 导出 GGUF、torch all-to-all 专家并行
- 2026-10 支持 Mistral Large 4、Reflection Beam；2026-10-27 发布 0.21.1

## 相关实体

- [[entities/trl|TRL]]
- [[entities/llama-factory|LLaMA-Factory]]
- [[entities/unsloth|Unsloth]]
- [[entities/deepspeed|DeepSpeed]]
- [[entities/mistral-models|Mistral 模型]]

## 相关概念

- [[concepts/lora|LoRA]]
- [[concepts/quantization|量化]]
- [[concepts/dpo|DPO]]
- [[concepts/grpo|GRPO]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Axolotl is a free and open-source tool designed to streamline post-training and fine-tuning for the latest large language models (LLMs)." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "Re-use a single YAML configuration file across the full fine-tuning pipeline: dataset preprocessing, training, evaluation, quantization, and inference." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
