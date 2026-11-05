---
title: Hugging Face
type: entity
tags: [organization]
kind: company
layer: L1
aliases: ["HF", "抱抱脸"]
competitors: []
depends_on: ["[[entities/pytorch]]"]
status: active
as_of: 2026-06
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# Hugging Face

## 描述

开源 AI 社区与平台：模型/数据集 Hub、`transformers` 等库。几乎所有开放权重模型（[[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/deepseek-r1|DeepSeek-R1]]）都在这里分发，是开源生态的“集散地”。2026-02 本地推理引擎 [[entities/llama-cpp|llama.cpp]] 的维护公司 ggml.ai 团队加入 HF，目标是让新模型从 transformers 几乎一键进入 llama.cpp；项目仍由 Georgi Gerganov 团队自治。

## 生态位置

- **层级**：[[maps/L1-数据|L1-数据]] · 公司
- **上游依赖**：[[entities/pytorch|PyTorch]]
- **竞争 / 替代**：—

## 时间线

- 2016 成立
- 2018 起 transformers 库流行
- 2026-02-20 ggml.ai（llama.cpp、ggml 的维护团队）加入 HF，财务条款未披露

## 相关实体

- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]
- [[entities/pytorch|PyTorch]]
- [[entities/llama-cpp|llama.cpp]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/lora|LoRA]]
- [[concepts/gguf|GGUF]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We are super happy to announce that GGML, creators of Llama.cpp, are joining HF in order to keep future AI open." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "The project will continue to be 100% open-source and community driven as it is now." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]

