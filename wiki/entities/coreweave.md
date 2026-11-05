---
title: CoreWeave
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["CoreWeave", "CRWV"]
competitors: ["[[entities/aws]]", "[[entities/azure]]"]
depends_on: ["[[entities/nvidia]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# CoreWeave

最具代表性的 [[concepts/gpu-cloud|GPU 云]]（「neocloud」），从以太坊矿场转型而来，只做加速计算这一层。商业模式是先与模型公司签多年长约，再用这些合同融资或举债去买 [[entities/nvidia|NVIDIA]] GPU、租数据中心：2026 Q2 营收约 25.8 亿美元（上年同期 12.1 亿）、积压订单约 1,040 亿美元，Q3 初又新增 250 亿美元以上承诺，同期季度净亏约 6.26 亿美元。[[entities/openai|OpenAI]] 2025-03 与其签五年约 120 亿美元合同，并在 IPO 的定向增发中买入 3.5 亿美元股票。技术上它也参与开源推理编排栈 [[entities/llm-d|llm-d]] 的发起。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **上游依赖**：[[entities/nvidia|NVIDIA]] GPU 供应配额、数据中心与电力（托管商 Core Scientific 等）
- **下游**：模型公司与推理服务；参与 [[entities/llm-d|llm-d]]，并采用 [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- **竞争 / 替代**：Nebius、Lambda、Nscale 等同类新云；三大云 [[entities/aws|AWS]]、[[entities/azure|Azure]]、[[entities/google-cloud|Google Cloud]]

## 时间线

- 2025-03 与 OpenAI 签五年、约 120 亿美元合同
- 2025-03-28 纳斯达克 IPO，募资 15 亿美元（发行规模曾由 27 亿缩至 15 亿）；OpenAI 定向增发买入 3.5 亿美元股票
- 2025-07 宣布以约 90 亿美元全股票收购托管商 Core Scientific
- 2025-10-30 收购被 Core Scientific 股东投票否决、协议终止，此前的 100 亿美元 / 12 年托管合同继续执行
- 2026 Q1 营收 20.8 亿美元，积压订单 994 亿美元
- 2026 Q2 营收约 25.8 亿美元，积压订单约 1,040 亿美元，净亏约 6.26 亿美元
- 2026 下半年 宣布提供 NVIDIA Vera Rubin 实例

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/openai|OpenAI]]
- [[entities/llm-d|llm-d]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/stargate|Stargate]]
- [[entities/azure|Microsoft Azure]]

## 相关概念

- [[concepts/gpu-cloud|GPU 云]]
- [[concepts/ai-accelerator|AI 加速器]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "CoreWeave 2026 Q2 营收约 25.8 亿美元（上年同期 12.1 亿）、积压订单约 1,040 亿美元" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
