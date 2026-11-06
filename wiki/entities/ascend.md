---
title: 昇腾
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["昇腾", "Ascend", "华为昇腾", "Ascend NPU", "Atlas"]
org: "[[entities/huawei|华为]]"
released: "2019"
competitors: ["[[entities/nvidia]]", "[[entities/amd-instinct]]"]
depends_on: ["[[concepts/hbm]]", "[[entities/cann]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# 昇腾

[[entities/huawei|华为]]的 AI 加速器（NPU）系列，是中国市场最主要的国产算力平台。软件栈分三层：底层 [[entities/cann|CANN]] 提供算子与运行时，框架侧由 TorchNPU 把 [[entities/pytorch|PyTorch]] 适配到昇腾（BSD-3-Clause，PyPI 包 `torch-npu`），另有自研框架昇思 MindSpore；推理侧由社区插件 `vllm-ascend` 支持 [[entities/vllm|vLLM]]，[[entities/sglang|SGLang]] 与 [[entities/llama-cpp|llama.cpp]]（CANN 后端）也有昇腾路径。硬件按负载分型：昇腾 950PR 面向预填充与推荐，950DT 面向解码与训练，同一 Die 分别配自研 [[concepts/hbm|HBM]] HiBL 1.0 与 HiZQ 2.0。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 加速器
- **上游依赖**：自研 HBM 与国内制程产能；软件栈 [[entities/cann|CANN]]
- **下游**：TorchNPU / MindSpore、`vllm-ascend`、SGLang、llama.cpp；模型侧 [[entities/glm|GLM]]、[[entities/deepseek-v|DeepSeek-V 系列]]
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]]（受出口管制影响的中国市场）、[[entities/amd-instinct|AMD Instinct]]；国内另有摩尔线程、寒武纪、沐曦、海光、天数智芯等

## 时间线

- 2019 昇腾 910 发布
- 2023-10-16 `torch-npu` 首个 PyPI 版本
- 2025-02-19 `vllm-ascend` 首个 PyPI 版本
- 2025-09 Huawei Connect 公布三年路线图：950PR（2026 Q1，配低成本 HBM HiBL 1.0）、950DT（2026 Q4，配 HiZQ 2.0，144 GB 显存、4 TB/s 访存带宽，支持 FP8 / MXFP8 / XMFP4 / HiF8）、960（2027 Q4，算力与带宽翻倍、新增 HiF4）、970（2028 Q4）；950 系列互联带宽 2 TB/s，为 910C 的 2.5 倍。Atlas 950 SuperPoD 最大 8,192 颗 950DT、160 个机柜、占地 1,000 ㎡、全光互联、互联带宽 16 PB/s、显存 1,152 TB，训练 491 万 token/s、推理 1,960 万 token/s，2026 Q4 上市；Atlas 960 SuperPoD 15,488 颗、30 EFLOPS（FP8）/ 60 EFLOPS（FP4）、4,460 TB 显存、34 PB/s，2027 Q4。同场发布 UnifiedBus 2.0 规范
- 2026-01-14 [[entities/zhipu-ai|智谱]] GLM-Image 称训练全程在昇腾 Atlas 800T A2 完成
- 2026-04 昇腾 SuperNode 全系完成 DeepSeek-V4 推理适配；DeepSeek 称 950PR 超节点规模出货前吞吐受限
- 2026-04-30 TorchNPU 26.0.0 支持 PyTorch 2.10.0
- 2026-10 `vllm-ascend` v0.30.0；`torch-npu` 2.14.0

## 相关实体

- [[entities/huawei|华为]]
- [[entities/cann|CANN]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/pytorch|PyTorch]]
- [[entities/glm|GLM]]
- [[entities/deepseek-v|DeepSeek-V 系列]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "vLLM Ascend (`vllm-ascend`) is a community maintained hardware plugin for running vLLM seamlessly on the Huawei Ascend NPU." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "TorchNPU is a deep learning adapter plugin built by Ascend for PyTorch, enabling the PyTorch framework to directly invoke Ascend NPU" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "So we'll have the Ascend 950PR chip for prefill and recommendation, and the Ascend 950DT chip for decode and training." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
