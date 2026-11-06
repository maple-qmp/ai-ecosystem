---
title: Microsoft Azure
type: entity
tags: [product]
kind: infra
layer: L0
aliases: ["Microsoft Azure", "Azure", "微软云", "Maia"]
org: "[[entities/microsoft|Microsoft]]"
released: "2010"
competitors: ["[[entities/aws]]", "[[entities/google-cloud]]"]
depends_on: ["[[entities/nvidia]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# Microsoft Azure

[[entities/microsoft|Microsoft]] 的云平台，AI 算力上同样走「自研芯片压成本 + [[entities/nvidia|NVIDIA]] 机器接前沿需求」的双轨。自研加速器叫 Maia：首代 Maia 100 为 2023 年，第二代 Maia 200 于 2026-01-26 公布并在 Azure 上线，定位推理——台积电 3nm、单芯片超 1400 亿晶体管、216 GB HBM3e @ 7 TB/s、272 MB 片上 SRAM、FP4 超过 10 PFLOPS / FP8 超过 5 PFLOPS、SoC TDP 750 W；微软宣称每美元性能比自家机队现有最新一代好 30%，FP4 为第三代 [[entities/aws-trainium|Trainium]] 的 3 倍、FP8 高于 [[entities/google-tpu|Google 第七代 TPU]]（均为厂商数字，无第三方基准）。系统层用建立在标准以太网上的两层 scale-up 网络，不依赖私有 fabric。它服务的模型包括 [[entities/openai|OpenAI]] 的 GPT-5.2，Microsoft Superintelligence 团队用它做合成数据生成与强化学习。数据中心侧推出 Fairwater 系列（威斯康星、亚特兰大），自称是其建过最大的 AI 工厂。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 云厂商
- **自研硬件**：Maia 加速器（Maia 100 / Maia 200）、Cobalt Arm CPU；软件栈 Maia SDK（Triton、PyTorch、NPL）
- **上游依赖**：[[entities/nvidia|NVIDIA]] GPU 供应；台积电 3nm
- **竞争 / 替代**：[[entities/aws|AWS]]、[[entities/google-cloud|Google Cloud]]；也向 [[concepts/gpu-cloud|GPU 云]]（如 Nebius）采购算力

## 时间线

- 2023 首代自研加速器 Maia 100 公布
- 2025-11 OpenAI 承诺采购 2500 亿美元 Azure 服务，同时微软失去 OpenAI 算力的优先购买权
- 2026-01-26 公布 Maia 200 并在 Azure 上线：先铺 US Central（爱荷华 Des Moines 附近），随后 US West 3（凤凰城）；同时开放 Maia SDK 预览，含 Triton 编译器、PyTorch 集成、低层语言 NPL 与模拟器 / 成本计算器
- 2026 Fairwater 系列数据中心（威斯康星、亚特兰大）投入与公布
- 2026 下半年 宣布提供 NVIDIA Vera Rubin 实例

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/openai|OpenAI]]
- [[entities/nvidia|NVIDIA]]
- [[entities/aws|AWS]]
- [[entities/google-cloud|Google Cloud]]
- [[entities/coreweave|CoreWeave]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/gpu-cloud|GPU 云]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "an accelerator built on TSMC's 3nm process with native FP8/FP4 tensor cores, a redesigned memory system with 216GB HBM3e at 7 TB/s and 272MB of on-chip SRAM" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "30% better performance per dollar than the latest generation hardware in our fleet today" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
