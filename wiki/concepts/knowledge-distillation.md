---
title: 知识蒸馏
type: concept
tags: [method]
layer: L3
aliases: ["知识蒸馏", "蒸馏", "Knowledge Distillation", "Distillation", "模型蒸馏"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# 知识蒸馏

## 定义

用大模型（教师）的输出训练小模型（学生），把能力压缩进部署成本更低的模型。经典形式来自 Hinton、Vinyals、Dean 2015 年的论文“Distilling the Knowledge in a Neural Network”（arXiv 1503.02531，2015-03-09）：用教师产生的类别概率作为“软目标”训练学生，并提高最后一层 softmax 的温度，让软目标足够平滑；论文在 MNIST 和一个商用语音声学模型上，把一组模型的集成蒸馏成单个模型。大模型时代更常见的是数据蒸馏：用强模型生成回答或推理轨迹，再用这些数据对小模型做[[concepts/supervised-fine-tuning|监督微调]]。

## 关键特征

- 软目标蒸馏需要教师的 logits；数据蒸馏只需要教师的文本输出，因此也能“蒸馏” API 模型
- [[entities/deepseek-r1|DeepSeek-R1]] 用 R1 生成的约 80 万条推理样本微调了 6 个基于 [[entities/qwen|Qwen]]2.5 与 [[entities/llama|Llama]]3 的稠密模型（1.5B–70B）；DeepSeek 称这比在小模型上直接做 RL 效果更好，DeepSeek-R1-Distill-Qwen-32B 在多项基准上超过 OpenAI-o1-mini
- 许可证：R1 的 MIT 许可明确允许用于蒸馏训练其他 LLM

## 应用

- 把[[concepts/reasoning-model|推理模型]]的能力迁移到小模型
- 端侧和低成本部署，常与[[concepts/quantization|量化]]叠加使用
- 工具：[[entities/verl|verl]] 的 VeRL-Tinker（2026-08）可跑 SFT、RL 和蒸馏；任何 SFT 工具都能做数据蒸馏

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法

## 相关概念

- [[concepts/supervised-fine-tuning|监督微调（SFT）]]
- [[concepts/grpo|GRPO]]
- [[concepts/quantization|量化]]
- [[concepts/reasoning-model|推理模型]]

## 相关实体

- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/qwen|Qwen]]
- [[entities/llama|Llama]]
- [[entities/verl|verl]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Our more general solution, called “distillation”, is to raise the temperature of the final softmax until the cumbersome model produces a suitably soft set of targets." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "We demonstrate that the reasoning patterns of larger models can be distilled into smaller models, resulting in better performance compared to the reasoning patterns discovered through RL on small models." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
