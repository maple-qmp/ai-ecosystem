---
title: AMD
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["AMD", "超微", "Advanced Micro Devices"]
competitors: ["[[entities/nvidia]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# AMD

GPU 与 CPU 厂商，在 AI 算力上是 [[entities/nvidia|NVIDIA]] 唯一在数据中心形成规模的通用 GPU 对手。产品线是数据中心加速器 [[entities/amd-instinct|Instinct]]（MI 系列），软件栈是开源的 [[entities/rocm|ROCm]]，核心策略是用 HIP 把接口做成贴近 [[entities/cuda|CUDA]] 的形态以降低移植成本。2026 年的主力是 CDNA 5 架构的 MI450 与机架级平台 Helios，目标下半年量产，Oracle 计划在 OCI 部署 5 万颗。管理层称最大规模的客户部署用于推理。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **产品**：[[entities/amd-instinct|Instinct]] 加速器、[[entities/rocm|ROCm]] 软件栈、EPYC CPU
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]]；在云厂商自研芯片（[[entities/google-tpu|TPU]]、[[entities/aws-trainium|Trainium]]）面前则是「第三方供应商」的同一阵营

## 时间线

- 2025-06 在 Advancing AI 上公布 [[entities/rocm|ROCm]] 7，同时推出 AMD Developer Cloud
- 2025-09 ROCm 7.0 正式发布
- 2026 向头部客户送样 MI450，并与客户接触 MI500
- 2026 下半年 MI450 量产与 Helios 系统上市目标
- 2027 MI500（CDNA 6、HBM4E）规划

## 相关实体

- [[entities/amd-instinct|AMD Instinct]]
- [[entities/rocm|ROCm]]
- [[entities/nvidia|NVIDIA]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/deepspeed|DeepSpeed]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "ROCm is powered by HIP, a C++ runtime API and kernel language that lets developers write portable GPU code with an interface similar to NVIDIA CUDA™." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
