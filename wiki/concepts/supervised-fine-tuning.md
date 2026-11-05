---
title: 监督微调（SFT）
type: concept
tags: [method]
layer: L3
aliases: ["监督微调", "SFT", "Supervised Fine-Tuning", "指令微调", "Instruction tuning"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# 监督微调（SFT）

## 定义

用人工撰写或筛选的“指令—回答”示范数据，以交叉熵损失继续训练[[concepts/pretraining|预训练]]模型，让它学会遵循指令、对话格式和工具调用格式。它通常是后训练的第一步：InstructGPT 先用标注员示范做 SFT，再做奖励模型和 [[concepts/rlhf|RLHF]]；[[concepts/dpo|DPO]] 的参考实现也先做 SFT，让偏好数据落在策略模型的分布内。

## 关键特征

- 本质仍是下一个 token 预测，但只在回答部分计算损失（对提示部分做掩码）
- 可以全量微调，也可以用 [[concepts/lora|LoRA]] / QLoRA 等参数高效方法
- 在推理模型的流水线里，SFT 用作“冷启动”种子：[[entities/deepseek-r1|DeepSeek-R1]] 的流水线包含两个 SFT 阶段和两个 RL 阶段；R1-Zero 则完全跳过 SFT
- Tülu 3 的流水线为 SFT → DPO → [[concepts/rlvr|RLVR]]
- 用强模型生成的数据做 SFT，就是大模型时代最常见的[[concepts/knowledge-distillation|知识蒸馏]]

## 应用

- 通用助手与领域模型微调
- 工具：[[entities/trl|TRL]] 的 `SFTTrainer`、[[entities/unsloth|Unsloth]]、[[entities/axolotl|Axolotl]]（2026-09 加入按 token 概率加权损失的 Dynamic Fine-Tuning）、[[entities/llama-factory|LLaMA-Factory]]、[[entities/verl|verl]]

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练方法
- **上一步**：[[concepts/pretraining|预训练]]
- **下一步**：[[concepts/rlhf|RLHF]] / [[concepts/dpo|DPO]] / [[concepts/rlvr|RLVR]]

## 相关概念

- [[concepts/pretraining|预训练]]
- [[concepts/rlhf|RLHF]]
- [[concepts/dpo|DPO]]
- [[concepts/lora|LoRA]]
- [[concepts/knowledge-distillation|知识蒸馏]]

## 相关实体

- [[entities/trl|TRL]]
- [[entities/axolotl|Axolotl]]
- [[entities/llama-factory|LLaMA-Factory]]
- [[entities/unsloth|Unsloth]]
- [[entities/deepseek-r1|DeepSeek-R1]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "For DPO, the SFT stage essentially ensures that the preference data we train on is in-distribution for our policy before we actually do the learning from preferences part." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
