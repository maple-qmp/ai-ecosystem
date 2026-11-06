---
title: ROCm
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["ROCm", "AMD ROCm", "HIP"]
org: "[[entities/amd|AMD]]"
released: "2016"
competitors: ["[[entities/cuda]]"]
depends_on: ["[[entities/amd-instinct]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# ROCm

[[entities/amd|AMD]] 的开源 GPU 计算软件栈，涵盖驱动、开发工具、编译器与数学 / 通信库，官方定位是「从底层内核到终端应用的 GPU 编程」，当前版本 10.1.0（2026-10-05）。核心是 HIP：一套 C++ 运行时 API 与内核语言，接口刻意贴近 [[entities/cuda|CUDA]]，让已有 CUDA 代码可移植；另支持 OpenMP 与 OpenCL，并集成 [[entities/pytorch|PyTorch]]、TensorFlow。它是 CUDA 之外唯一在数据中心形成规模的通用 GPU 栈，短板仍在长尾算子与内核库的成熟度。主仓库已声明即将弃用，后续开发迁往 `ROCm/TheRock`。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 基础设施
- **上游依赖**：[[entities/amd-instinct|AMD Instinct]] 与 Radeon GPU；10.1.0 的兼容性矩阵中最新的 Instinct 仍是 MI355X / MI350X / MI350P（gfx950），尚未列出 MI450
- **下游**：[[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/llama-cpp|llama.cpp]]（HIP 后端）、[[entities/deepspeed|DeepSpeed]]
- **竞争 / 替代**：[[entities/cuda|CUDA]]；在中国市场的对应物是 [[entities/cann|CANN]]

## 时间线

- 2016 ROCm 1.0 发布
- 2025-06 公布 ROCm 7，AMD 宣称推理为 ROCm 6 的 3.5 倍、训练 3 倍（厂商数字），新增 Radeon 消费级 GPU 支持；同期推出 AMD Developer Cloud
- 2025-09-16 ROCm 7.0.0 正式发布，含 HIP 7.0
- 2025-10-30 ROCm 7.1.0
- 2026-01-21 ROCm 7.2.0（其后 7.2.1–7.2.4 到 2026-05）
- 2026-07-15 ROCm 7.14.0，2026-09-02 7.14.1
- 2026-08-26 ROCm 10.0.0
- 2026-10-05 ROCm 10.1.0（当前版本，文档树改称「ROCm Core SDK」，并分出 AI Ecosystem、GPU Systems and Infrastructure 等子站）
- 2026 初 ROCm SMI 进入维护模式，ROCTracer / ROCProfiler / rocprofv2 让位给 ROCprofiler-SDK
- 2026 主仓库声明弃用，开发迁往 ROCm/TheRock

## 相关实体

- [[entities/amd|AMD]]
- [[entities/amd-instinct|AMD Instinct]]
- [[entities/cuda|CUDA]]
- [[entities/pytorch|PyTorch]]
- [[entities/vllm|vLLM]]
- [[entities/llama-cpp|llama.cpp]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "ROCm is an open-source software stack of drivers, development tools, and APIs that enable GPU programming from low-level kernels to end-user applications." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "This repository will be deprecated soon. Use ROCm/TheRock moving forward" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
