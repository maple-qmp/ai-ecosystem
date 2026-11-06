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

[[entities/nvidia|NVIDIA]] 的 GPU 并行计算平台与编程模型，2006 年发布，是 NVIDIA 最深的护城河：[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]] 等几乎所有训练与推理软件都建立在其上，换芯片的真实成本因此落在算子库与框架适配，而不是硬件本身。竞争者的策略都围着它打转：[[entities/rocm|ROCm]] 用 HIP 做出接口相近的可移植层，[[entities/cann|CANN]] 以「全面开源开放」争取框架适配。CUDA Toolkit 13.0（2025-08-06）在传统 SIMT 之外引入了第二套模型——基于 tile 的编程：开发者对整块数据定义运算，由编译器负责线程分配与 Tensor Core 映射，并分两层提供（Python / C++ 的高层 API 与 DSL，以及给编译器作者的 CUDA Tile IR 后端）。这是二十年来编程模型层面最大的一次变化，动机是让 Python 侧也写得出接近内核水平的性能，正面对冲 Triton、TileLang 这类第三方 DSL。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 基础设施
- **上游依赖**：NVIDIA GPU 硬件
- **下游**：[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]、[[entities/deepspeed|DeepSpeed]]、[[entities/megatron-lm|Megatron-LM]]、[[entities/llama-cpp|llama.cpp]]（CUDA 后端）
- **竞争 / 替代**：[[entities/rocm|ROCm]]（HIP）、[[entities/cann|CANN]]；[[entities/google-tpu|TPU]] 侧则走 XLA / JAX 的另一条栈

## 时间线

- 2006 发布
- 2025-08-06 CUDA Toolkit 13.0：引入基于 tile 的编程模型与 CUDA Tile IR 后端；统一 Arm 工具链，一次安装覆盖 SBSA 服务器与 Thor 等嵌入式目标（Orin / sm_87 除外）；为 Blackwell 的 256-bit 访存新增 32 字节对齐的向量类型 `_32a` / `_16a`，旧的 `double4` 等开始告警
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

- "CUDA Toolkit 13.0 introduces a tile-based programming model that lets developers define operations on entire data tiles while the compiler handles thread distribution and Tensor Core mapping." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "Crucially, the tile model maps naturally onto Tensor Cores." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "TensorRT-LLM README 的版本徽章为 1.4.0rc3，依赖 CUDA 13.4.1、torch 2.14.0。" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
