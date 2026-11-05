---
title: NVIDIA
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["英伟达"]
competitors: []
depends_on: []
status: active
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# NVIDIA

## 描述

GPU 与 AI 加速计算的主导厂商。其数据中心 GPU 与 [[entities/cuda|CUDA]] 软件栈构成大模型训练和推理的事实标准底座，是整个生态最上游的瓶颈环节之一。软件上它还维护推理库 [[entities/tensorrt-llm|TensorRT-LLM]]、推理编排栈 [[entities/nvidia-dynamo|NVIDIA Dynamo]] 和训练库 [[entities/megatron-lm|Megatron Core]]，并参与发起 [[entities/llm-d|llm-d]]；风投部门 NVentures 投资了 SGLang 团队的 [[entities/radixark|RadixArk]]。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **上游依赖**：—
- **竞争 / 替代**：—

## 时间线

- 2006 CUDA 发布
- 2022 起数据中心 GPU 供不应求
- 2025-03-22 TensorRT-LLM 完全开源
- 2025-09-24 TensorRT-LLM 1.0，改为 PyTorch 架构
- 2026-03 GTC 发布 Dynamo 1.0
- 2026-05-05 NVentures 参投 RadixArk 1 亿美元种子轮
- 2026-07 Megatron Core 在 GB300 NVL72 上预训练 DeepSeek-V3，每 GPU 1,648 TFLOPs/s

## 相关实体

- [[entities/cuda|CUDA]]
- [[entities/pytorch|PyTorch]]
- [[entities/vllm|vLLM]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/megatron-lm|Megatron-LM]]
- [[entities/llm-d|llm-d]]
- [[entities/radixark|RadixArk]]

## 相关概念

- [[concepts/quantization|量化]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The open-source, datacenter-scale inference stack." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]

