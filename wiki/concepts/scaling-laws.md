---
title: 规模定律
type: concept
tags: [theory]
layer: X
aliases: ["规模定律", "Scaling Laws", "缩放定律", "Chinchilla 定律", "Neural Scaling Laws"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/ai-benchmarks-survey-2026-11]]"]
---

# 规模定律

## 定义

描述语言模型性能随参数量、训练数据量和训练算力增长而可预测提升的经验规律。Kaplan 等（[[entities/openai|OpenAI]]，2020-01）发现交叉熵损失与这三者呈幂律关系，部分趋势跨越七个数量级以上；Hoffmann 等（DeepMind，2022-03，即 Chinchilla 论文）修正了算力分配结论：算力最优训练应让模型规模与训练 token 同比扩展。

## 关键特征

- **幂律关系**（Kaplan 2020）：损失随模型规模、数据规模、算力按幂律下降；网络宽度、深度等结构细节在较大范围内影响很小；可据此确定固定算力预算的最优分配；大模型样本效率显著更高，因此当时的结论偏向“把预算多给参数”
- **Chinchilla 修正**（Hoffmann 2022）：训练 400 多个模型（7000 万到 160 多亿参数、50 亿到 5000 亿 token）后发现当时的大模型“显著训练不足”；模型规模每翻一倍，训练 token 也应翻一倍。同等算力下 70B 的 Chinchilla 用 4 倍数据，全面超过 Gopher（280B）、GPT-3（175B）等，[[concepts/mmlu|MMLU]] 达 67.5%
- **经验值**：约 20 token / 参数；后来的模型为降低推理成本远超此比例训练（如 Llama 3 8B 约 1,875 token / 参数）（二手）
- **推理时计算扩展**：2024-09 OpenAI o1 报告准确率随训练时强化学习算力和推理时“思考”算力的增加而提升；ARC Prize 分析认为 AIME 准确率与推理时计算量呈对数线性关系（二手），见[[concepts/reasoning-model|推理模型]]

## 应用

- 预训练规划：在给定算力下选择参数量与数据量
- 算力投资与政策判断：欧盟 AI Act 以 10^25 FLOP、加州 SB 53 以 10^26 次运算的训练算力作为监管门槛，隐含“算力决定能力”的假设，见[[concepts/eu-ai-act|欧盟《人工智能法》]]、[[concepts/california-sb-53|加州 SB 53]]

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 关键论文

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/mmlu|MMLU / MMLU-Pro]]
- [[concepts/eu-ai-act|欧盟《人工智能法》]]

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/llama|Llama]]

## 我的判断

## 来源摘录

- "The loss scales as a power-law with model size, dataset size, and the amount of compute used for training, with some trends spanning more than seven orders of magnitude." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]（Kaplan et al. 2020）
- "for compute-optimal training, the model size and the number of training tokens should be scaled equally: for every doubling of model size the number of training tokens should also be doubled." — [[sources/ai-benchmarks-survey-2026-11|AI 评测基准调研]]（Hoffmann et al. 2022）
