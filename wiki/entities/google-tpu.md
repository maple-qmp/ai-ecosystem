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

Google 自研的 AI 加速器系列，是 [[entities/nvidia|NVIDIA]] 之外唯一长期承担前沿模型训练的平台。软件上与编译器 XLA、框架 JAX、运行时 Pathways 配套（JAX README：「JAX uses XLA to compile and scale your NumPy programs on TPUs, GPUs, and other hardware accelerators.」），不走 [[entities/cuda|CUDA]] 生态。第七代 Ironwood（文档里的 TPU7x）2025-04 发布时定位「专为推理设计」，到 2025-11 的 GA 公告已改为训练、强化学习与推理兼顾；每颗 192 GiB [[concepts/hbm|HBM]]、约 7.37 TB/s 带宽、单颗峰值 4,614 TFLOPs，superpod 9,216 颗液冷芯片经 ICI 互联（9.6 Tb/s）、合计 42.5 EFLOPS、共享 1.77 PB HBM，对客户提供 256 颗与 9,216 颗两种规模，另有 OCS 光交换做故障绕行。除服务 [[entities/gemini|Gemini]] 外，最大外部客户是 [[entities/anthropic|Anthropic]]——官方 GA 公告写明 Claude 在 TPU 上训练与服务。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 加速器
- **上游依赖**：[[concepts/hbm|HBM]]；先进制程（第八代规划台积电 2nm）
- **软件栈**：XLA、JAX、[[entities/pytorch|PyTorch]]/XLA；推理侧 [[entities/vllm|vLLM]] 的 TPU 支持由独立仓库 vLLM JAX（原 `tpu-inference`）与 `vllm-torchtpu` 承担，[[entities/sglang|SGLang]] 有 SGLang-TorchTPU 与 SGL-JAX 两条路径
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]] 数据中心 GPU、[[entities/aws-trainium|AWS Trainium]]、[[entities/amd-instinct|AMD Instinct]]

## 时间线

- 2016 第一代 TPU 公开
- 2025-04 Cloud Next 25 发布第七代 Ironwood，当时口径为「首个专为推理设计的 TPU」，perf/watt 为第六代 Trillium 的 2 倍
- 2025-10-23 [[entities/anthropic|Anthropic]] 宣布扩大用量至最多 100 万颗、2026 年超过 1 GW
- 2025-11-06 GA 公告：称数周内全面可用，定位扩回训练 / RL / 推理兼顾，峰值性能为 TPU v5p 的 10 倍、单颗性能为 Trillium 的 4 倍以上；同场预览 Arm 架构的 Axion N4A 实例
- 2026 预览第八代：TPU 8t（训练）与 TPU 8i（推理）分家，台积电 2nm，目标 2027 年底（二手报道）

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
- "It offers a 10X peak performance improvement over TPU v5p and more than 4X better performance per chip for both training and inference workloads compared to TPU v6e (Trillium)" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "Each chip is equipped with 192 GiB of HBM, with bandwidth of approximately 7.37 TB/s." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
