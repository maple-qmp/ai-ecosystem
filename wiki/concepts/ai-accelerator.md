---
title: AI 加速器
type: concept
tags: [term]
layer: L0
aliases: ["AI 加速器", "AI accelerator", "NPU", "深度学习加速器"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# AI 加速器

专门为神经网络的矩阵乘法与张量运算设计的处理器，用来替代通用 CPU 承担训练与推理。2026 年在用的主流形态有四类：通用 GPU（[[entities/nvidia|NVIDIA]] 数据中心 GPU、[[entities/amd-instinct|AMD Instinct]]）、云厂商自研的专用加速器（[[entities/google-tpu|Google TPU]]、[[entities/aws-trainium|AWS Trainium]]、Azure Maia）、独立架构（[[entities/groq|Groq]] 的 LPU 以大容量片上 SRAM 替代 [[concepts/hbm|HBM]]、[[entities/cerebras|Cerebras]] 把整片晶圆做成一颗芯片）、以及中国市场的 NPU（[[entities/ascend|昇腾]]等）。

## 关键特征

- **算力以低精度为单位**：规格普遍按 FP8、FP4 标注，混合精度训练与量化推理是默认前提（见 [[concepts/quantization|量化]]）
- **内存带宽常是真正瓶颈**：解码阶段受 [[concepts/kv-cache|KV cache]] 读写限制，HBM 容量与带宽比峰值算力更能决定吞吐
- **训练与推理开始分化**：Google 第八代 TPU 拆成 TPU 8t / TPU 8i，华为昇腾 950 拆成 950PR / 950DT，AMD 分 MI455X / MI430X——同一代芯片按预填充、解码、训练切成不同型号
- **软件栈决定可用性**：换芯片的实际成本在算子库与框架适配上，而非硬件本身（见 [[entities/cuda|CUDA]]、[[entities/rocm|ROCm]]、[[entities/cann|CANN]]）
- **规模单位上移**：从单卡到机架（NVL72、Helios），再到超节点与集群（见 [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]）

## 应用

训练前沿模型目前仍集中在 NVIDIA GPU 与 Google TPU；推理是其他架构的主要突破口，云厂商的自研芯片与 Groq、Cerebras 都先从推理切入，因为推理负载对生态成熟度的要求低于训练，且成本敏感。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]]
- **下游**：[[maps/L3-训练与推理|L3-训练与推理]] 的引擎（[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]）需要为每种加速器做后端适配

## 相关概念

- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]
- [[concepts/quantization|量化]]
- [[concepts/kv-cache|KV cache]]

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/google-tpu|Google TPU]]
- [[entities/amd-instinct|AMD Instinct]]
- [[entities/ascend|昇腾]]
- [[entities/aws-trainium|AWS Trainium]]
- [[entities/groq|Groq]]
- [[entities/cerebras|Cerebras]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Ascend NPU (Neural Processing Unit) is a series of AI accelerators developed by Huawei." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
