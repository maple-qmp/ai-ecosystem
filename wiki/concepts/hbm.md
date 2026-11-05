---
title: HBM
type: concept
tags: [standard]
layer: L0
aliases: ["HBM", "高带宽内存", "High Bandwidth Memory"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# HBM

堆叠式高带宽内存，是绝大多数 [[concepts/ai-accelerator|AI 加速器]] 的显存方案：多层 DRAM 裸片垂直堆叠后与计算裸片做近距离封装，以极宽的接口换取带宽。它决定了一颗芯片能装下多大的模型权重和多长的 [[concepts/kv-cache|KV cache]]，因此在 2026 年的产品规格里，HBM 容量与带宽往往比峰值算力更关键。

## 关键特征

- **容量与带宽成为营销主轴**：[[entities/google-tpu|Ironwood TPU]] 每颗 192 GB、约 7.37 TB/s；[[entities/amd-instinct|AMD MI450]] 报道为 432 GB HBM4、19.6 TB/s，而上一代 MI350 为 288 GB HBM3E
- **代际推进**：HBM3E → HBM4 → HBM4E，与芯片代际绑定（MI450 用 HBM4，2027 年的 MI500 规划 HBM4E）
- **供应即产能**：HBM 产能集中在少数存储厂手里，是整条 AI 硬件链最容易卡住的环节；[[entities/huawei|华为]]因此自研 HiBL 1.0 与 HiZQ 2.0 两种 HBM，分别配[[entities/ascend|昇腾]] 950PR 与 950DT
- **绕开 HBM 的尝试**：[[entities/groq|Groq]] 用大容量片上 SRAM、[[entities/cerebras|Cerebras]] 用晶圆级片上内存，换低延迟并回避 HBM 供应，代价是单机可容纳的模型规模受限

## 应用

模型权重、KV cache 与激活都放在 HBM 里。显存不足时的常规手段是量化（见 [[concepts/quantization|量化]]）、KV cache 分层卸载到 CPU 内存或磁盘，以及把模型切分到多卡（张量并行）——后者又把压力转移到 [[concepts/scale-up-interconnect|互联]]上。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]]
- **上游**：存储厂的堆叠与先进封装产能
- **下游**：加速器规格，以及 [[maps/L3-训练与推理|L3]] 推理引擎的显存管理策略

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/kv-cache|KV cache]]
- [[concepts/quantization|量化]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 相关实体

- [[entities/google-tpu|Google TPU]]
- [[entities/amd-instinct|AMD Instinct]]
- [[entities/ascend|昇腾]]
- [[entities/cerebras|Cerebras]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Ascend 950PR 与 Ascend 950DT 使用同一 Die，分别配自研 HBM HiBL 1.0 与 HiZQ 2.0" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
