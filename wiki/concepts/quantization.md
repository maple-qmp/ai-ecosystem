---
title: 量化
type: concept
tags: [method]
layer: L3
aliases: ["Quantization", "模型量化"]
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# 量化

## 定义

把模型权重（和激活）从 16/32 位浮点压缩为 8 位、4 位等低精度表示，以减少显存并加速推理，代价是可能的精度损失。

## 关键特征

- INT8 / INT4 / FP8 等格式
- 训练后量化与量化感知训练
- [[concepts/gguf|GGUF]]、AWQ、GPTQ 等常见方案
- 新硬件格式：MXFP8 / MXFP4、NVFP4（[[entities/vllm|vLLM]] 均已支持）
- [[entities/llama-cpp|llama.cpp]] 支持 1.5–8 bit 整数量化

## 应用

- 本地与端侧部署：[[entities/ollama|Ollama]]、[[entities/lm-studio|LM Studio]] 运行 GGUF 量化模型
- 降低推理成本

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]

## 相关概念

- [[concepts/lora|LoRA]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/gguf|GGUF]]
- [[concepts/kv-cache|KV cache]]

## 相关实体

- [[entities/vllm|vLLM]]
- [[entities/llama|Llama]]
- [[entities/nvidia|NVIDIA]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/tensorrt-llm|TensorRT-LLM]]

## 我的判断

## 来源摘录

