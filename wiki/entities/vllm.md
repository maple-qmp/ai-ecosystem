---
title: vLLM
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["vLLM", "vllm-project/vllm"]
org: "[[entities/inferact]]"
released: "2023-06"
competitors: ["[[entities/sglang]]", "[[entities/tensorrt-llm]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/cuda]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# vLLM

## 描述

开源的 LLM 推理与服务引擎，2023 年在 UC Berkeley Sky Computing Lab 开发，核心创新是 PagedAttention：像操作系统分页一样管理 [[concepts/kv-cache|KV cache]]，解决显存碎片问题，发布时吞吐比 Hugging Face Transformers 高 14–24 倍。现在是部署 [[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/gpt-oss|gpt-oss]] 等开放权重模型最常用的引擎之一，支持 200+ 种模型架构、2000+ 贡献者，2025-05 起由 PyTorch Foundation 托管。服务端同时提供 OpenAI 兼容 API、[[concepts/anthropic-messages-api|Anthropic Messages API]] 和 gRPC。2026-01 核心团队成立 [[entities/inferact|Inferact]] 做商业化，项目仍保持开源（Apache-2.0）。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 推理引擎
- **上游依赖**：[[entities/pytorch|PyTorch]]（含 torch.compile）、[[entities/cuda|CUDA]] / HIP；注意力内核 FlashAttention、FlashInfer、FlashMLA 等
- **下游 / 编排**：[[entities/nvidia-dynamo|NVIDIA Dynamo]]、[[entities/llm-d|llm-d]]、Ray Serve 把 vLLM 作为后端
- **竞争 / 替代**：[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]；本地场景是 [[entities/llama-cpp|llama.cpp]]、[[entities/ollama|Ollama]]

## 主要能力

- **调度与缓存**：连续批处理、分块预填充、前缀缓存（见 [[concepts/kv-cache|KV cache]]）
- **加速**：CUDA / HIP 图，[[concepts/speculative-decoding|推测解码]]（n-gram、suffix、EAGLE、DFlash），预填充 / 解码 / 编码分离（见 [[concepts/disaggregated-serving|预填充 / 解码分离]]）
- **量化**：FP8、MXFP8 / MXFP4、NVFP4、INT8、INT4、GPTQ / AWQ、[[concepts/gguf|GGUF]] 等（见 [[concepts/quantization|量化]]）
- **并行**：张量、流水线、数据、专家、上下文并行
- **接口**：OpenAI 兼容服务器、Anthropic Messages API、gRPC；结构化输出、工具调用与推理解析器、多 LoRA
- **硬件**：NVIDIA、AMD、Intel GPU，x86 / ARM / PowerPC CPU；TPU、Gaudi、昇腾、Apple Silicon 等通过插件

## 时间线

- 2023-06-19 PyPI 首个版本
- 2023-06-20 发布博客，介绍 PagedAttention；此前已在 LMSYS 的 Chatbot Arena 与 Vicuna Demo 运行两个月
- 2025-03 v0.8.0 起 V1 引擎成为默认
- 2025-05 成为 PyTorch Foundation 托管项目（与 [[entities/deepspeed|DeepSpeed]] 同批）
- 2025-10-02 v0.11.0 彻底移除 V0 引擎
- 2026-01-22 核心团队成立 [[entities/inferact|Inferact]]，种子轮 1.5 亿美元
- 2026-11-02 发布 0.33.0

## 相关实体

- [[entities/inferact|Inferact]]
- [[entities/sglang|SGLang]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/llm-d|llm-d]]
- [[entities/pytorch|PyTorch]]
- [[entities/cuda|CUDA]]
- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]

## 相关概念

- [[concepts/kv-cache|KV cache]]
- [[concepts/speculative-decoding|推测解码]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/quantization|量化]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Easy, fast, and cheap LLM serving for everyone" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "vLLM achieves 14x - 24x higher throughput than HF and 2.2x - 2.5x higher throughput than TGI." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "We find that existing systems waste 60% – 80% of memory due to fragmentation and over-reservation." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "OpenAI-compatible API server, plus Anthropic Messages API and gRPC support" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
