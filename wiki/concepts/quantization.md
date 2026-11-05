---
title: 量化
type: concept
tags: [method]
layer: L3
aliases: ["量化", "Quantization", "模型量化", "GPTQ", "AWQ", "LLM.int8()", "QAT", "量化感知训练"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]", "[[sources/training-methods-survey-2026-11]]"]
---

# 量化

## 定义

把模型权重（有时也包括激活和 KV cache）从 16/32 位浮点压缩为 8 位、4 位甚至更低的表示，以减少显存、加速推理，代价是可能的精度损失。按时机分为训练后量化（PTQ，训练完成后直接压缩，如 GPTQ、AWQ）和量化感知训练（QAT，训练时模拟低精度，让模型适应量化误差）；量化也被用于训练本身，如 QLoRA 和 8-bit 优化器。

## 关键特征

- **GPTQ**（IST Austria，ICLR 2023，arXiv 2210.17323）：生成式 Transformer 的训练后压缩，把 OPT、BLOOM 压到 2/3/4 bit，支持权重分组
- **AWQ**（MIT Han Lab，arXiv 2306.00978）：激活感知的 INT3/4 权重量化，支持指令微调模型与多模态模型，附 CUDA 推理内核和端侧推理 TinyChat
- **bitsandbytes**：PyTorch 的 k-bit 量化库，提供 8-bit 优化器（分块量化）、LLM.int8()（向量级 8-bit 量化，离群特征单独用 16-bit 矩阵乘，推理显存减半且无性能下降）和 QLoRA 用的 4-bit 量化（NF4）
- **新硬件格式**：FP8、MXFP8 / MXFP4、NVFP4，[[entities/vllm|vLLM]] 均已支持；训练侧 [[entities/axolotl|Axolotl]] 支持 FP8 混合精度训练和 int8 / int4 / FP8 / NVFP4 / MXFP4 的 QAT，[[entities/unsloth|Unsloth]] 支持 FP8 训练
- **本地格式**：[[concepts/gguf|GGUF]]；[[entities/llama-cpp|llama.cpp]] 支持 1.5–8 bit 整数量化；Unsloth 和 Axolotl 都能把训练结果直接导出为 GGUF
- **训练中的量化**：QLoRA 在 4-bit 冻结模型上训练 [[concepts/lora|LoRA]]；[[entities/llama-factory|LLaMA-Factory]] 的 QLoRA 支持 2–8 bit，经 AQLM / AWQ / GPTQ / LLM.int8 / HQQ / EETQ

## 应用

- 本地与端侧部署：[[entities/ollama|Ollama]]、[[entities/lm-studio|LM Studio]] 运行 GGUF 量化模型
- 降低数据中心推理成本：[[entities/vllm|vLLM]] 的 FP8 / MXFP4 / NVFP4 / INT4 推理
- 降低微调门槛：QLoRA 让单卡微调大模型成为可能，常与[[concepts/knowledge-distillation|知识蒸馏]]叠加做小模型部署

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]

## 相关概念

- [[concepts/lora|LoRA]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/gguf|GGUF]]
- [[concepts/kv-cache|KV cache]]
- [[concepts/knowledge-distillation|知识蒸馏]]

## 相关实体

- [[entities/vllm|vLLM]]
- [[entities/llama|Llama]]
- [[entities/nvidia|NVIDIA]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/axolotl|Axolotl]]
- [[entities/unsloth|Unsloth]]

## 我的判断

## 来源摘录

- "`bitsandbytes` enables accessible large language models via k-bit quantization for PyTorch." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "Compressing all models from the OPT and BLOOM families to 2/3/4 bits, including weight grouping" — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "reduces memory usage enough to finetune a 65B parameter model on a single 48GB GPU while preserving full 16-bit finetuning task performance." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
