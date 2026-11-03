---
title: vLLM
type: entity
tags: [project]
kind: framework
layer: L3
released: "2023"
competitors: []
depends_on: ["[[entities/pytorch]]", "[[entities/cuda]]"]
status: active
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: []
---

# vLLM

> [!info] 种子页面
> 由 Claude 基于训练知识生成（截至 2026-06），尚无来源支撑。核实后补充 `sources`，并把 `reviewed` 设为 `true`。

## 描述

源自 UC Berkeley 的开源 LLM 推理与服务引擎，核心是 PagedAttention 显存管理，大幅提升吞吐量，是部署 [[entities/llama|Llama]]、[[entities/qwen|Qwen]] 等开放权重模型最常用的方案之一。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 框架
- **上游依赖**：[[entities/pytorch|PyTorch]]、[[entities/cuda|CUDA]]
- **竞争 / 替代**：—

## 时间线

- 2023 发布 PagedAttention

## 相关实体

- [[entities/pytorch|PyTorch]]
- [[entities/cuda|CUDA]]
- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]

## 相关概念

- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

