---
title: AWS
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["AWS", "Amazon Web Services", "亚马逊云科技"]
competitors: ["[[entities/azure]]", "[[entities/google-cloud]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# AWS

Amazon 的云业务，AI 算力上同时卖两种东西：[[entities/nvidia|NVIDIA]] 机器（EC2 UltraServers 上的 GB200 / GB300 集群、P 系列实例）和自研加速器 [[entities/aws-trainium|Trainium / Inferentia]]（Trn、Inf 实例），上层是托管模型服务 Amazon Bedrock 与 SageMaker。它是 [[entities/anthropic|Anthropic]] 的主要训练伙伴与云厂商，为其建设了 Trainium2 集群 Project Rainier；2025-11 又与 [[entities/openai|OpenAI]] 签下七年、约 380 亿美元的 GPU 协议，同时微软失去 OpenAI 算力的优先购买权。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 云厂商
- **自研硬件**：[[entities/aws-trainium|Trainium / Inferentia]]，软件栈 AWS Neuron
- **竞争 / 替代**：[[entities/azure|Microsoft Azure]]、[[entities/google-cloud|Google Cloud]]；专做算力出租的 [[concepts/gpu-cloud|GPU 云]]

## 时间线

- 2024-12 Trainium2 实例正式可用，并公布 Trainium3 计划
- 2025-10 Project Rainier 投入使用：为 Anthropic 部署近 50 万颗 Trainium2，目标扩至 100 万颗
- 2025-11-03 与 OpenAI 签七年、约 380 亿美元协议，提供 GB200 / GB300 集群，2026 年底达满容量
- 2025-12-02 re:Invent 上 Trainium3 UltraServer 正式可用，并预览 Trainium4
- 2026 宣布将部署 [[entities/cerebras|Cerebras]] 的 WSE-3；与各云一同宣布 2026 下半年提供 NVIDIA Vera Rubin 实例

## 相关实体

- [[entities/aws-trainium|AWS Trainium]]
- [[entities/anthropic|Anthropic]]
- [[entities/openai|OpenAI]]
- [[entities/nvidia|NVIDIA]]
- [[entities/cerebras|Cerebras]]
- [[entities/azure|Microsoft Azure]]
- [[entities/google-cloud|Google Cloud]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/gpu-cloud|GPU 云]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Anthropic remains committed to its partnership with Amazon, its primary training partner and cloud provider." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
