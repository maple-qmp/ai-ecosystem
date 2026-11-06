---
title: CANN
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["CANN", "异构计算架构", "Compute Architecture for Neural Networks"]
org: "[[entities/huawei|华为]]"
released: "2019"
competitors: ["[[entities/cuda]]", "[[entities/rocm]]"]
depends_on: ["[[entities/ascend]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# CANN

[[entities/huawei|华为]][[entities/ascend|昇腾]]的异构计算架构，位置相当于昇腾生态里的 [[entities/cuda|CUDA]]：提供算子库、图编译与运行时，是框架（TorchNPU、MindSpore）和推理引擎接入昇腾的必经层。2026 年的主线是「全面开源开放」：已开放 50 多个代码仓、800 多个算子，并兼容 [[entities/pytorch|PyTorch]]、[[entities/vllm|vLLM]] 等框架以及 Triton、TileLang 等生态语言——与 [[entities/rocm|ROCm]] 用 HIP 贴近 CUDA 接口是同一思路：先降低移植成本，再谈性能。[[entities/llama-cpp|llama.cpp]] 的硬件后端列表里也包含 CANN。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 基础设施
- **上游依赖**：[[entities/ascend|昇腾]] 硬件
- **下游**：TorchNPU、MindSpore、`vllm-ascend`、[[entities/sglang|SGLang]]、llama.cpp
- **竞争 / 替代**：[[entities/cuda|CUDA]]、[[entities/rocm|ROCm]]

## 时间线

- 2019 随昇腾 910 推出
- 2025 华为宣布计划在 2025 年底前开源 CANN
- 2026 鲲鹏昇腾开发者大会（KADC2026）口径为「CANN 全面开源开放、兼容主流开源生态、Mind 系列软件升级并开源贡献」三方向，已开放 50+ 代码仓与 800+ 算子
- 2026-08-15 CCF 中国开源大会设「CANN 全面开源开放」分论坛，讨论昇腾 950 架构与 DeepSeek V4 的优化实践

## 相关实体

- [[entities/huawei|华为]]
- [[entities/ascend|昇腾]]
- [[entities/cuda|CUDA]]
- [[entities/rocm|ROCm]]
- [[entities/vllm|vLLM]]
- [[entities/llama-cpp|llama.cpp]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "已开放 50 多个代码仓、800 多个算子，兼容 PyTorch、vLLM 等框架与 Triton、TileLang 等生态语言" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
