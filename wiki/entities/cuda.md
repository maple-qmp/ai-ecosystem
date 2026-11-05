---
title: CUDA
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["CUDA", "Compute Unified Device Architecture", "CUDA Toolkit"]
org: "[[entities/nvidia|NVIDIA]]"
released: "2006"
competitors: ["[[entities/rocm]]", "[[entities/cann]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]", "[[sources/inference-engines-survey-2026-11]]"]
---

# CUDA

[[entities/nvidia|NVIDIA]] 的 GPU 并行计算平台与编程模型，2006 年发布，是 NVIDIA 最深的护城河：[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]] 等几乎所有训练与推理软件都建立在其上，换芯片的真实成本因此落在算子库与框架适配，而不是硬件本身。竞争者的策略都围着它打转：[[entities/rocm|ROCm]] 用 HIP 做出接口相近的可移植层，[[entities/cann|CANN]] 以「全面开源开放」争取框架适配。CUDA Toolkit 13.0（2025-08）在传统 SIMT 之外铺设了第二条路线——基于 tile 的编程模型与 CUDA Tile IR 后端，13.1 推出 CUDA Tile 与 cuTile Python（Apache-2.0），这是二十年来编程模型层面最大的一次变化，动机是让 Python 侧也写得出接近内核水平的性能，正面对冲 Triton、TileLang 这类第三方 DSL。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 基础设施
- **上游依赖**：NVIDIA GPU 硬件
- **下游**：[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]、[[entities/deepspeed|DeepSpeed]]、[[entities/megatron-lm|Megatron-LM]]、[[entities/llama-cpp|llama.cpp]]（CUDA 后端）
- **竞争 / 替代**：[[entities/rocm|ROCm]]（HIP）、[[entities/cann|CANN]]；[[entities/google-tpu|TPU]] 侧则走 XLA / JAX 的另一条栈

## 时间线

- 2006 发布
- 2025-08 CUDA Toolkit 13.0：引入基于 tile 的编程模型与 CUDA Tile IR 后端；统一 Arm 工具链（服务器与嵌入式合并）；向量类型改为 32 字节对齐以利 Blackwell；新增 GCC 15 / Clang 20 支持，去掉 ICC 与 MSVC 2017
- 2026 CUDA 13.1 推出 CUDA Tile 与 cuTile Python（Apache-2.0）
- 2026-10 TensorRT-LLM README 的依赖已标到 CUDA 13.4.1

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/pytorch|PyTorch]]
- [[entities/vllm|vLLM]]
- [[entities/rocm|ROCm]]
- [[entities/cann|CANN]]
- [[entities/tensorrt-llm|TensorRT-LLM]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "在传统 SIMT 之外铺设第二条路线——基于 tile 的编程模型，引入 CUDA Tile IR 后端" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "TensorRT-LLM README 的版本徽章为 1.4.0rc3，依赖 CUDA 13.4.1、torch 2.14.0。" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
