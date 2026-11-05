---
title: 合成数据
type: concept
tags: [method]
layer: L1
aliases: ["Synthetic Data", "合成数据", "模型生成数据"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-data-layer-survey-2026-11]]"]
---

# 合成数据

## 定义

由模型而不是人类直接产出、用来训练或对齐其他模型的数据，例如让大模型按主题写教科书式文本、生成对话与指令回复，再经过过滤、去重后作为预训练或后训练语料。NVIDIA 的 Nemotron-4 技术报告给出的主要动机是人工标注成本高。

## 关键特征

- **预训练语料**：[[entities/hugging-face|Hugging Face]] 的 Cosmopedia 用 Mixtral-8x7B-Instruct 生成合成教科书、博客、故事与 WikiHow 文章，共 3000 多万个文件、250 亿 token，生成耗时超过 1 万 H100 GPU 小时
- **对齐数据**：NVIDIA Nemotron-4-340B-Instruct 对齐阶段用的数据超过 98% 是合成的，人工标注只有约 2 万条；技术报告认为人工标注太贵，所以合成数据对对齐至关重要
- **质量控制**：要配合过滤（奖励模型、分类器打分）、MinHash 去重，以及针对评测基准的 n-gram 去污染。Cosmopedia 用 datatrove 去重和去污染，Nemotron 用奖励模型做质量过滤与偏好排序
- **模型崩溃风险**：Shumailov 等（Nature，2024-07）发现，不加区分地用模型生成的内容训练后代模型，原始数据分布的尾部会逐渐消失，这一现象在 LLM、VAE 和高斯混合模型中都出现。所以合成数据通常要与真实数据混用

## 应用

- 预训练语料扩充（教科书式、按主题覆盖）
- 指令微调与偏好数据（SFT、RLHF / DPO）

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]]
- **上下游**：需要 L2 的基础模型做生成器，产出供 L3 训练使用；与人工的[[concepts/data-labeling|数据标注]]互补

## 相关概念

- [[concepts/data-labeling|数据标注]]
- [[concepts/scaling-laws|Scaling Laws]]
- [[concepts/lora|LoRA]]

## 相关实体

- [[entities/hugging-face|Hugging Face]]
- [[entities/nvidia|NVIDIA]]
- [[entities/fineweb|FineWeb]]
- [[entities/scale-ai|Scale AI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "It contains over 30 million files and 25 billion tokens, making it the largest open synthetic dataset to date." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
- "Cosmopedia consists of 25B tokens and was generated in > 10k H100 GPU hours." — [[sources/ai-data-layer-survey-2026-11|AI 数据层调研]]
