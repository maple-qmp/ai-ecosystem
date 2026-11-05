---
title: 华为
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["华为", "Huawei", "华为技术有限公司"]
competitors: ["[[entities/nvidia]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# 华为

中国的通信与计算设备厂商，在 AI 生态里的位置是国产算力的主干：自研加速器[[entities/ascend|昇腾]]（Ascend）、配套软件栈 [[entities/cann|CANN]]、自研框架昇思 MindSpore，以及灵衢（UnifiedBus）互联与 Atlas 超节点。在出口管制下它是 [[entities/nvidia|NVIDIA]] 在中国市场的主要替代，2026 年开始承接国产模型的部分训练与推理负载——[[entities/zhipu-ai|智谱]]的 GLM-Image 称训练全程在昇腾完成，[[entities/deepseek|DeepSeek]] 的 V4 在昇腾上完成了推理适配与部分后训练。最大的不确定项是自研 HBM 与芯片产能。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **产品**：[[entities/ascend|昇腾]] 加速器、[[entities/cann|CANN]] 软件栈、MindSpore 框架、Atlas SuperPoD / SuperCluster
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]]、[[entities/amd|AMD]]（在中国市场则受出口管制影响）

## 时间线

- 2019 昇腾 910 发布，CANN 与 MindSpore 同期成形
- 2025-09 Huawei Connect 上公布三年芯片路线图：昇腾 950PR / 950DT / 960 / 970 与 Atlas 超节点
- 2026-01-14 与[[entities/zhipu-ai|智谱]]联合开源 GLM-Image，称自回归基座从数据预处理到大规模预训练全流程在昇腾 Atlas 800T A2 上完成
- 2026-04 称昇腾 SuperNode 全系完成 [[entities/deepseek-v|DeepSeek-V4]] 推理适配；另有华为团队称在昇腾 NPU SuperPOD 上完成 V4 家族全参数后训练的端到端优化
- 2026 鲲鹏昇腾开发者大会口径为「CANN 全面开源开放」，已开放 50+ 代码仓、800+ 算子
- 2026-08-15 CCF 中国开源大会设 CANN 开源分论坛

## 相关实体

- [[entities/ascend|昇腾]]
- [[entities/cann|CANN]]
- [[entities/nvidia|NVIDIA]]
- [[entities/zhipu-ai|智谱 AI]]
- [[entities/deepseek|DeepSeek]]
- [[entities/vllm|vLLM]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Ascend NPU (Neural Processing Unit) is a series of AI accelerators developed by Huawei." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
