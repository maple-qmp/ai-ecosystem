---
title: Google TPU
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["Google TPU", "TPU", "Tensor Processing Unit", "张量处理单元", "Ironwood"]
org: "[[entities/google-cloud|Google Cloud]]"
released: "2016"
competitors: ["[[entities/nvidia|NVIDIA]]", "[[entities/aws-trainium]]"]
depends_on: ["[[concepts/hbm]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# Google TPU

Google 自研的 AI 加速器系列，是 [[entities/nvidia|NVIDIA]] 之外唯一长期承担前沿模型训练的平台。软件上与编译器 XLA、框架 JAX 配套（JAX README：「JAX uses XLA to compile and scale your NumPy programs on TPUs, GPUs, and other hardware accelerators.」），不走 [[entities/cuda|CUDA]] 生态。第七代 Ironwood 定位推理，每颗 192 GB [[concepts/hbm|HBM]]、约 7.37 TB/s 带宽、4,614 TFLOPS（FP8），完整 pod 9,216 颗芯片经 3D torus 互联、共享约 1.77 PB 内存。除服务 [[entities/gemini|Gemini]] 外，最大外部客户是 [[entities/anthropic|Anthropic]]。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 加速器
- **上游依赖**：[[concepts/hbm|HBM]]；先进制程（第八代规划台积电 2nm）
- **软件栈**：XLA、JAX、[[entities/pytorch|PyTorch]]/XLA；推理侧 [[entities/vllm|vLLM]] 的 TPU 支持由独立仓库 vLLM JAX（原 `tpu-inference`）与 `vllm-torchtpu` 承担，[[entities/sglang|SGLang]] 有 SGLang-TorchTPU 与 SGL-JAX 两条路径
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]] 数据中心 GPU、[[entities/aws-trainium|AWS Trainium]]、[[entities/amd-instinct|AMD Instinct]]

## 时间线

- 2016 第一代 TPU 公开
- 2025-10-23 [[entities/anthropic|Anthropic]] 宣布扩大用量至最多 100 万颗、2026 年超过 1 GW
- 2025-11 第七代 Ironwood 发布，定位推理，宣称能效为上一代两倍
- 2026 Ironwood 正式可用（GA 日期各来源不一）
- 2026 预览第八代：TPU 8t（训练）与 TPU 8i（推理）分家，台积电 2nm，目标 2027 年底

## 相关实体

- [[entities/google-cloud|Google Cloud]]
- [[entities/anthropic|Anthropic]]
- [[entities/gemini|Gemini]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/nvidia|NVIDIA]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "JAX uses XLA to compile and scale your NumPy programs on TPUs, GPUs, and other hardware accelerators." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "`tpu-inference` is now vLLM JAX (`vllm-jax`) and is focused on serving JAX models on TPU with vLLM." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
