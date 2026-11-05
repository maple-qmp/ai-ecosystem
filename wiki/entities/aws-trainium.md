---
title: AWS Trainium
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["AWS Trainium", "Trainium", "Inferentia", "AWS Neuron", "Neuron SDK"]
org: "[[entities/aws|AWS]]"
released: "2020"
competitors: ["[[entities/google-tpu]]", "[[entities/nvidia]]"]
depends_on: ["[[concepts/hbm]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# AWS Trainium

[[entities/aws|AWS]] 自研的 AI 加速器系列：Inferentia 面向推理、Trainium 面向训练，近年两条线在对外叙事上逐渐合并到 Trainium。软件入口是 AWS Neuron SDK——包含图编译器、运行时与开发工具，集成 [[entities/pytorch|PyTorch]]、JAX 与 vLLM Neuron，并通过 Neuron Kernel Interface（NKI）开放 NeuronCore 内核编程；覆盖 Inf1、Inf2、Trn1、Trn2、Trn3 实例。最大用户是 [[entities/anthropic|Anthropic]]：Project Rainier 为其部署了近 50 万颗 Trainium2，目标 100 万颗。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 加速器
- **上游依赖**：[[concepts/hbm|HBM]]；Trainium3 为 3nm
- **下游**：AWS Neuron SDK、PyTorch / JAX、vLLM Neuron；Amazon Bedrock 的生产负载已跑在 Trainium3 上；[[entities/sglang|SGLang]] 的 Trainium 支持在接入中（机内互联 NeuronSwitch 与「10 微秒以内」的延迟数字只见于二手分析，官方新闻稿未提）
- **竞争 / 替代**：[[entities/google-tpu|Google TPU]]、[[entities/nvidia|NVIDIA]] GPU、Azure Maia

## 时间线

- 2020 Inferentia 与 Trainium 相继公布
- 2024-12 Trainium2 实例 GA，同时公布 Trainium3
- 2025-10 Project Rainier 为 Anthropic 投入使用：7 栋建筑、近 50 万颗 Trainium2，每服务器 16 颗、以自研 NeuronLink 互联
- 2025-12-02 Trainium3 UltraServer 在 re:Invent GA：每系统最多 144 颗、合计 362 PFLOPS（FP8），AWS 称相对 Trainium2 UltraServer 算力最高 4.4 倍、能效 4 倍、访存带宽近 4 倍、延迟降至四分之一；客户称用 Trainium 把训练与推理成本降低最多 50%（Anthropic、Ricoh、Splash Music 等），Amazon Bedrock 已在其上跑生产负载
- 2025-12-02 预览 Trainium4：AWS 称 FP8 性能至少为 Trainium3 的 3 倍、内存带宽 4 倍，并将支持 NVIDIA NVLink Fusion；无时间表

## 相关实体

- [[entities/aws|AWS]]
- [[entities/anthropic|Anthropic]]
- [[entities/nvidia|NVIDIA]]
- [[entities/google-tpu|Google TPU]]
- [[entities/vllm|vLLM]]
- [[entities/pytorch|PyTorch]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]
- [[concepts/hbm|HBM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "AWS Neuron is a software development kit (SDK) enabling high-performance deep learning and generative AI using AWS Inferentia and Trainium accelerators." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "Neuron includes a graph compiler, runtime, developer tools (Neuron Explorer, agentic development tools), and integrates with PyTorch, JAX, and vLLM Neuron for inference serving." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "Trn3 UltraServers scale up to 144 Trainium3 chips, delivering up to 362 FP8 PFLOPs with 4x lower latency" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
