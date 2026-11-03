---
title: 混合专家（MoE）
type: concept
tags: [method]
layer: L2
aliases: ["MoE", "Mixture of Experts"]
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: []
---

# 混合专家（MoE）

> [!info] 种子页面
> 由 Claude 基于训练知识生成（截至 2026-06），尚无来源支撑。核实后补充 `sources`，并把 `reviewed` 设为 `true`。

## 定义

一种稀疏模型架构：每层包含多个“专家”子网络，由路由器为每个 token 只激活其中少数几个，从而在总参数很大的同时控制单次计算量。

## 关键特征

- 总参数大、激活参数小
- 推理计算成本低于同规模稠密模型
- 对显存与负载均衡有额外要求

## 应用

- DeepSeek-V3/R1
- Mixtral
- Qwen 大型 MoE 版本

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/quantization|量化]]

## 相关实体

- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/mistral-ai|Mistral AI]]
- [[entities/qwen|Qwen]]

## 我的判断

## 来源摘录

