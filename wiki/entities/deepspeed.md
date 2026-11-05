---
title: DeepSpeed
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["DeepSpeed", "ZeRO", "deepspeedai/DeepSpeed"]
org: "[[entities/microsoft]]"
released: "2020"
competitors: ["[[entities/megatron-lm]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/cuda]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# DeepSpeed

## 描述

[[entities/microsoft|微软]]开源的大规模分布式训练优化库，构建在 [[entities/pytorch|PyTorch]] 之上。核心是 ZeRO：把优化器状态、梯度和参数切分到各数据并行进程，去掉冗余副本，从而用同样的显存训练大得多的模型；在此基础上还有 CPU / NVMe 卸载、ZeRO++ 等。它曾与 [[entities/megatron-lm|Megatron]] 合作训练 Megatron-Turing NLG 530B。2025 年初微软把项目移交 Linux Foundation，同年 5 月成为 PyTorch Foundation 托管项目（与 [[entities/vllm|vLLM]] 同批），仓库迁到 `deepspeedai` 组织。近两年的工作集中在卸载（ZenFlow、SuperOffload）、编译优化（DeepCompile）、长序列训练和新优化器（Muon）。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练框架
- **上游依赖**：[[entities/pytorch|PyTorch]]、[[entities/cuda|CUDA]]；也支持 AMD GPU
- **竞争 / 替代**：[[entities/megatron-lm|Megatron Core]]、PyTorch FSDP

## 时间线

- 2020 微软研究院发布 ZeRO 与 DeepSpeed
- 2020-10-22 PyPI 包上线
- 2025-01 或 02 移交 Linux Foundation AI & Data（报道说法不一）
- 2025-03 AutoTP：Hugging Face 模型自动张量并行
- 2025-04 DeepCompile：分布式训练的编译器优化
- 2025-05 成为 PyTorch Foundation 托管项目
- 2025-06 ALST（与 Snowflake 合作的百万 token 级长序列训练）、DeepNVMe
- 2025-08 ZenFlow 无停顿卸载引擎
- 2025-10 SuperOffload：面向超级芯片的大模型训练卸载
- 2025-12 Core API 更新：PyTorch 风格 backward、低精度主权重
- 2026-03 SuperOffload 获 ASPLOS 2026 最佳论文荣誉提名
- 2026-05 支持 Muon 优化器；AMD GPU 上 ZeRO-3 使用 System DMA
- 2026-10-29 发布 0.19.9

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/pytorch|PyTorch]]
- [[entities/megatron-lm|Megatron-LM]]
- [[entities/vllm|vLLM]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/scaling-laws|规模定律]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Extreme Speed and Scale for DL Training" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Our SuperOffload work received an Honorable Mention for the ASPLOS 2026 Best Paper Award" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
