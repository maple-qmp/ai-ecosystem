---
title: Megatron-LM
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["Megatron-LM", "Megatron Core", "Megatron Bridge", "Megatron"]
org: "[[entities/nvidia]]"
released: ""
competitors: ["[[entities/deepspeed]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/cuda]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# Megatron-LM

## 描述

[[entities/nvidia|NVIDIA]] 的大模型训练仓库，包含两部分。Megatron-LM 是带预置训练脚本的参考实现，适合研究、教学和快速实验；Megatron Core 是可组合的 GPU 优化库，提供 Transformer 构件、张量 / 流水线 / 数据 / 专家 / 上下文并行（TP、PP、DP、EP、CP）和 FP16 / BF16 / FP8 / FP4 混合精度，供各家自建训练框架使用。配套的 Megatron Bridge（属 NVIDIA NeMo）负责 Hugging Face 与 Megatron 检查点的双向转换，并提供训练配方。2026 年它跟进了 DeepSeek-V4、Muon 优化器和混合架构模型，在 GB300 NVL72 上创下 MoE 预训练纪录。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练框架
- **上游依赖**：[[entities/pytorch|PyTorch]]（2.6.0+）、[[entities/cuda|CUDA]]
- **竞争 / 替代**：[[entities/deepspeed|DeepSpeed]]、PyTorch FSDP

## 时间线

- 2023-05-11 megatron-core 首次发布到 PyPI
- 2026-04 通过新优化器库支持 Muon 等新型优化器
- 2026-05 `dev` 分支初步支持 DeepSeek-V4，Bridge 提供转换、推理和预训练配方
- 2026-07 在 GB300 NVL72 上预训练 DeepSeek-V3 671B：256 块 GPU，每 GPU 1,648 TFLOPs/s
- 2026-08 Megatron Core 0.19：HybridModel、按分位数的 MoE 路由均衡、兼容 CUDA Graph 的激活卸载
- 2026-10 发布比特级确定性预训练指南；10-29 发布 megatron-core 0.20.0

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/deepspeed|DeepSpeed]]
- [[entities/pytorch|PyTorch]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/deepseek|DeepSeek]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/transformer|Transformer]]
- [[concepts/scaling-laws|规模定律]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Megatron-LM is a reference example that includes Megatron Core plus pre-configured training scripts, ideal for research teams, learning distributed training, and quick experimentation." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Megatron Core is a composable library with GPU-optimized building blocks for custom training frameworks." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Megatron Core achieves 1,648 TFLOPs/s per GPU for DeepSeek-V3 671B on 256 GPUs." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
