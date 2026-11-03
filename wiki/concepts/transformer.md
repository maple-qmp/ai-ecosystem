---
title: Transformer
type: concept
tags: [method]
layer: L2
aliases: ["变换器", "Attention Is All You Need"]
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: []
---

# Transformer

> [!info] 种子页面
> 由 Claude 基于训练知识生成（截至 2026-06），尚无来源支撑。核实后补充 `sources`，并把 `reviewed` 设为 `true`。

## 定义

2017 年 Google 论文《Attention Is All You Need》提出的神经网络架构，以自注意力机制取代循环结构，是当今几乎所有大语言模型的基础。

## 关键特征

- 自注意力，可并行训练
- 易于随参数与数据规模扩展
- 衍生出仅解码器（GPT 类）与编码器（BERT 类）等变体

## 应用

- 大语言模型
- 多模态模型
- 语音与视觉模型

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/scaling-laws|规模定律]]

## 相关实体

- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gpt|GPT]]
- [[entities/pytorch|PyTorch]]

## 我的判断

## 来源摘录

