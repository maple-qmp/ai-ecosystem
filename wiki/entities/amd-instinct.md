---
title: AMD Instinct
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["AMD Instinct", "Instinct", "MI 系列", "MI300X", "MI450"]
org: "[[entities/amd|AMD]]"
released: "2020"
competitors: ["[[entities/nvidia]]", "[[entities/google-tpu]]"]
depends_on: ["[[concepts/hbm]]", "[[entities/rocm]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# AMD Instinct

[[entities/amd|AMD]] 的数据中心 GPU 系列，是目前唯一被主流推理引擎普遍支持的非 NVIDIA 通用 GPU：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]（MI300X–MI355X）与 [[entities/llama-cpp|llama.cpp]]（HIP 后端）都有 Instinct 路径，软件入口是 [[entities/rocm|ROCm]]。2026 年的新一代 MI400 / MI450 采用 CDNA 5 架构与 HBM4，报道规格为 432 GB 显存、19.6 TB/s 带宽（上一代 MI350 为 288 GB HBM3E），分 MI455X（训练与推理）与 MI430X（HPC 与主权 AI）两档，配机架级平台 Helios（MI450X IF128，128 颗 GPU 一机架）对标 NVIDIA 的 VR200 NVL144。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 加速器
- **上游依赖**：[[concepts/hbm|HBM]]（MI450 为 HBM4）、台积电 2nm；软件栈 [[entities/rocm|ROCm]]
- **下游**：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/llama-cpp|llama.cpp]]、[[entities/deepspeed|DeepSpeed]]（2026-05 起在 AMD GPU 上支持 ZeRO-3 的 System DMA）
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]] 数据中心 GPU；云厂商自研的 [[entities/google-tpu|TPU]]、[[entities/aws-trainium|Trainium]]

## 时间线

- 2020 Instinct MI100，CDNA 架构起点
- 2023 MI300 系列，成为首个被广泛部署的 AI 推理替代方案
- 2025 MI350 系列（288 GB HBM3E）
- 2026 MI450 向头部客户送样；AMD 否认 MI455X 延期的报道
- 2026 下半年 MI450 量产与 Helios 机架目标；Oracle 计划自 2026 年底起在 OCI 部署 5 万颗（二手报道）
- 2026-10 ROCm 10.1.0 的兼容性矩阵仍未列出 MI450，最新的 Instinct 为 MI355X / MI350X / MI350P
- 2027 AMD / Cisco / HUMAIN 合资项目计划部署最多 250 MW 的 MI400 系列算力，容量自 2027 下半年起上线；MI500（CDNA 6、HBM4E）规划

## 相关实体

- [[entities/amd|AMD]]
- [[entities/rocm|ROCm]]
- [[entities/nvidia|NVIDIA]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/llm-d|llm-d]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "报道规格为 432 GB HBM4（MI350 为 288 GB HBM3E）、19.6 TB/s 带宽；分 MI455X（训练 + 推理）与 MI430X（HPC 与主权 AI）两档" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
