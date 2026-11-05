---
title: GGUF
type: concept
tags: [standard]
layer: L3
aliases: ["GGUF", "GGUF 格式", ".gguf"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# GGUF

## 定义

ggml 系推理引擎（[[entities/llama-cpp|llama.cpp]] 及以它为后端的工具）使用的模型文件格式。它是二进制单文件格式，把加载模型所需的全部信息放在一个文件里，设计目标是加载保存快、容易读取。模型通常在 [[entities/pytorch|PyTorch]] 等框架中训练，再转换成 GGUF 用于推理，常常同时做[[concepts/quantization|量化]]。2023-08 推出，取代 GGML、GGMF、GGJT 等旧格式。

## 关键特征

- **单文件部署**：不依赖额外文件
- **可扩展**：超参数改为键值结构的元数据（这是与前身 GGJT 的关键区别），加新字段不破坏旧模型的兼容
- **兼容 `mmap`**：可以内存映射加载
- **易用**：任何语言用少量代码就能读写，不需要外部库
- **命名约定**：`[<Sidecar>]<BaseName><SizeLabel><FineTune><Version><Encoding><Type><Shard>.gguf`；Sidecar 可以是 `mmproj`（多模态投影器）或 `mtp`（多 token 预测头，用作[[concepts/speculative-decoding|推测解码]]的草稿模块）

## 应用

- 本地推理：[[entities/llama-cpp|llama.cpp]]、[[entities/ollama|Ollama]]、[[entities/lm-studio|LM Studio]]
- `llama serve -hf <仓库>` 直接从 Hugging Face 拉取 GGUF 模型
- [[entities/vllm|vLLM]] 也能加载 GGUF 量化模型

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]

## 相关概念

- [[concepts/quantization|量化]]
- [[concepts/speculative-decoding|推测解码]]

## 相关实体

- [[entities/llama-cpp|llama.cpp]]
- [[entities/ollama|Ollama]]
- [[entities/lm-studio|LM Studio]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/vllm|vLLM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "GGUF is a file format for storing models for inference with GGML and executors based on GGML." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "It is a successor file format to GGML, GGMF and GGJT, and is designed to be unambiguous by containing all the information needed to load a model." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
