---
title: Unsloth
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["Unsloth", "Unsloth AI", "Unsloth Studio", "Unsloth Desktop", "unslothai/unsloth"]
released: "2023"
competitors: ["[[entities/axolotl]]", "[[entities/llama-factory]]", "[[entities/lm-studio]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/trl]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/training-methods-survey-2026-11]]"]
---

# Unsloth

## 描述

Unsloth AI 开发的微调与本地运行工具，用基于 Triton 的优化内核加速训练，README 称训练“快 2 倍、省 70% 显存，无精度损失”。支持 [[concepts/lora|LoRA]]、QLoRA、全量微调、[[concepts/pretraining|预训练]]、[[concepts/grpo|GRPO]]、[[concepts/dpo|DPO]] 和 FP8 训练，模型覆盖 LLM、扩散、TTS、嵌入等。现在定位为“第一个能运行和训练模型的桌面应用”，有 Unsloth Desktop、Unsloth Studio（Web UI）、Unsloth Core（代码库）三种用法；能本地运行 GGUF 模型，提供 OpenAI 兼容 API，`unsloth start claude` 一条命令把 [[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex]] 等编程 Agent 接到本地模型；训练结果可导出 [[concepts/gguf|GGUF]]、NVFP4、FP8。公司由 Daniel Han、Michael Han 兄弟 2023 年创办，参加 Y Combinator 2024 夏季批次（二手报道）。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 训练工具
- **上游依赖**：[[entities/pytorch|PyTorch]]、Triton、bitsandbytes、transformers、PEFT、[[entities/trl|TRL]]
- **竞争 / 替代**：[[entities/axolotl|Axolotl]]、[[entities/llama-factory|LLaMA-Factory]]；本地运行一侧与 [[entities/lm-studio|LM Studio]]、[[entities/ollama|Ollama]] 重叠
- **被集成**：[[entities/trl|TRL]] 与 [[entities/llama-factory|LLaMA-Factory]] 都可调用 Unsloth 内核

## 时间线

- 2023 项目开始（README 引用条目年份）
- 2024-08-04 PyPI 首个版本 2024.8（版本号按年月）
- 2024 夏 参加 Y Combinator S24（二手报道）
- 2026-11-04 发布 2026.11.2

## 相关实体

- [[entities/trl|TRL]]
- [[entities/axolotl|Axolotl]]
- [[entities/llama-factory|LLaMA-Factory]]
- [[entities/llama-cpp|llama.cpp]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/lora|LoRA]]
- [[concepts/quantization|量化]]
- [[concepts/grpo|GRPO]]
- [[concepts/gguf|GGUF]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Unsloth is the first desktop app to run and train models." — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
- "Train LLMs, diffusion, decision, TTS, and embedding models 2× faster with 70% less VRAM" — [[sources/training-methods-survey-2026-11|训练与后训练方法调研]]
