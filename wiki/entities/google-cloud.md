---
title: Google Cloud
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["Google Cloud", "谷歌云", "GCP", "Google Cloud Platform"]
competitors: ["[[entities/aws]]", "[[entities/azure]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# Google Cloud

Google 的云业务，在 AI 算力上是三大云里自研程度最高的一家：训练与推理的主力是自研的 [[entities/google-tpu|TPU]]，通用负载有自研 Arm CPU Axion，同时照常售卖 [[entities/nvidia|NVIDIA]] GPU 实例。TPU 的最大外部客户是 [[entities/anthropic|Anthropic]]——2025-10 双方宣布把用量扩大到最多 100 万颗 TPU、2026 年上线超过 1 GW 容量。模型侧它还承载 [[entities/google-deepmind|Google DeepMind]] 的 [[entities/gemini|Gemini]] 训练与服务，是「自研芯片 + 自研模型 + 自有云」三位一体的唯一一家。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 云厂商
- **自研硬件**：[[entities/google-tpu|TPU]]（加速器）、Axion（Arm CPU）
- **竞争 / 替代**：[[entities/aws|AWS]]、[[entities/azure|Microsoft Azure]]；算力出租侧还有 [[concepts/gpu-cloud|GPU 云]]

## 时间线

- 2025-10-23 Anthropic 宣布扩大 TPU 用量，最多 100 万颗、2026 年超过 1 GW 容量
- 2025-11 发布第七代 TPU Ironwood
- 2026 Ironwood 正式可用（各来源日期不一，需按官方公告核实）
- 2026 预览第八代 TPU，拆成 TPU 8t（训练）与 TPU 8i（推理），目标 2027 年底

## 相关实体

- [[entities/google-tpu|Google TPU]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/anthropic|Anthropic]]
- [[entities/nvidia|NVIDIA]]
- [[entities/llm-d|llm-d]]
- [[entities/aws|AWS]]
- [[entities/azure|Microsoft Azure]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/gpu-cloud|GPU 云]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "including up to one million TPUs" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "is expected to bring well over a gigawatt of capacity online in 2026." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
