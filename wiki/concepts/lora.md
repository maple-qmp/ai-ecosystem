---
title: LoRA
type: concept
tags: [method]
layer: L3
aliases: ["Low-Rank Adaptation", "低秩适配"]
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: []
---

# LoRA

## 定义

Microsoft 研究者 2021 年提出的参数高效微调方法：冻结原模型，只训练插入的低秩矩阵，大幅降低微调显存与存储成本。

## 关键特征

- 只训练极少量参数
- 适配器可单独分发与切换
- QLoRA 将其与量化结合

## 应用

- 开源模型领域微调
- 风格与角色定制

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]

## 相关概念

- [[concepts/quantization|量化]]

## 相关实体

- [[entities/microsoft|Microsoft]]
- [[entities/llama|Llama]]
- [[entities/hugging-face|Hugging Face]]

## 我的判断

## 来源摘录

