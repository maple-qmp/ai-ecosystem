---
title: TensorRT-LLM
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["TensorRT-LLM", "TensorRT LLM", "TRT-LLM"]
org: "[[entities/nvidia]]"
released: "2023-10"
competitors: ["[[entities/vllm]]", "[[entities/sglang]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/cuda]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# TensorRT-LLM

## 描述

[[entities/nvidia|NVIDIA]] 的开源 LLM 与视觉生成模型推理优化库，只面向 NVIDIA GPU。它为 attention、GEMM、MoE 等常见算子提供定制内核，并在运行时做[[concepts/disaggregated-serving|预填充 / 解码分离]]、宽专家并行、[[concepts/speculative-decoding|推测解码]]等优化。2025-03 完全开源并转到 GitHub 开发；2025-09 的 1.0 版本把基于 [[entities/pytorch|PyTorch]] 的架构定为默认，用户用 Python 的 LLM API 就能从单卡扩展到多节点。可以接入 [[entities/nvidia-dynamo|NVIDIA Dynamo]] 和 Triton Inference Server。NVIDIA 用它发布新卡（Blackwell、GB200 / GB300 NVL72）上的推理性能纪录，2026 年的技术博客集中在 DeepSeek-V3.2 / V4 优化、稀疏注意力、agentic 服务和 KV cache 压缩。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 推理引擎
- **上游依赖**：[[entities/cuda|CUDA]]（README 标注 13.4.1）、[[entities/pytorch|PyTorch]]（2.14.0）
- **下游 / 编排**：[[entities/nvidia-dynamo|NVIDIA Dynamo]]、Triton Inference Server
- **竞争 / 替代**：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]

## 时间线

- 2023-10-20 PyPI 首个公开版本 0.5.0
- 2025-03-22 完全开源，开发转到 GitHub
- 2025-09-24 1.0：PyTorch 架构成为稳定默认，LLM API 稳定，此后执行弃用策略
- 2026-01 至 2026-10 技术博客：DeepSeek-V3.2 / V4 在 Blackwell 上的优化、稀疏注意力、NVL72 上的分布式权重数据并行、agent 应用联合优化、KV cache 压缩（2026-10-14）
- 2026-10-28 1.4.0rc2 预发布；当前稳定版 1.2.1

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/cuda|CUDA]]
- [[entities/pytorch|PyTorch]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/gpt-oss|gpt-oss]]

## 相关概念

- [[concepts/kv-cache|KV cache]]
- [[concepts/speculative-decoding|推测解码]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/quantization|量化]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "TensorRT LLM is now fully open-source, with developments moved to GitHub!" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "TensorRT LLM is an open-sourced library for optimizing LLM and Visual Gen inference." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "TensorRT LLM is designed to be modular and easy to modify." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
