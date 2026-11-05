---
title: llama.cpp
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["llama.cpp", "ggml", "ggml-org/llama.cpp", "ggml.ai"]
org: "[[entities/hugging-face]]"
released: "2023-03"
competitors: ["[[entities/vllm]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# llama.cpp

## 描述

用纯 C/C++ 实现、没有外部依赖的 LLM / VLM 推理引擎，是本地推理的事实底座。作者 Georgi Gerganov 先写了张量库 ggml 和 whisper.cpp，2023-03 发布 llama.cpp。它的特点是硬件覆盖面广：Apple Silicon（Metal）是一等公民，另有 x86 AVX / AMX、RISC-V、CUDA、HIP、Vulkan、SYCL、昇腾、骁龙等十余种后端，还能 CPU+GPU 混合推理，运行超出显存的模型。模型用自家的 [[concepts/gguf|GGUF]] 格式，支持 1.5–8 bit [[concepts/quantization|量化]]。[[entities/ollama|Ollama]]、[[entities/lm-studio|LM Studio]] 等桌面工具都以它为推理后端。2026-02 维护公司 ggml.ai 的团队加入 [[entities/hugging-face|Hugging Face]]，项目保持 MIT 开源和技术自治。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 本地推理引擎
- **上游依赖**：ggml 张量库；各硬件后端（[[entities/cuda|CUDA]]、Metal、Vulkan 等）
- **下游**：[[entities/ollama|Ollama]]（早期后端）、[[entities/lm-studio|LM Studio]]（定制分支）、llama-cpp-python 等绑定
- **竞争 / 替代**：Apple MLX；数据中心场景是 [[entities/vllm|vLLM]] 等

## 主要组件

- **ggml**：底层张量库，负责各硬件后端
- **llama cli / llama serve**：命令行对话与 OpenAI 兼容 API 服务器（带内置 Web UI），可用 `-hf` 直接从 Hugging Face 拉 GGUF 模型
- **GGUF**：模型文件格式，见 [[concepts/gguf|GGUF]]

## 时间线

- 2022-09 Georgi Gerganov 开始写 ggml
- 2023-03-10 llama.cpp 首个版本
- 2023-03-23 Python 绑定 llama-cpp-python 首个版本
- 2023 成立公司 ggml.ai
- 2023-08 推出 GGUF 格式，取代旧的 GGML / GGJT 格式
- 2026-02-20 ggml.ai 团队加入 [[entities/hugging-face|Hugging Face]]，财务条款未披露；Georgi 团队继续全职维护，保有技术方向和社区自主权

## 相关实体

- [[entities/hugging-face|Hugging Face]]
- [[entities/ollama|Ollama]]
- [[entities/lm-studio|LM Studio]]
- [[entities/llama|Llama]]
- [[entities/qwen|Qwen]]

## 相关概念

- [[concepts/gguf|GGUF]]
- [[concepts/quantization|量化]]
- [[concepts/speculative-decoding|推测解码]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "LLM inference in C/C++" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "CPU+GPU hybrid inference to partially accelerate models larger than the total VRAM capacity" — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "llama.cpp is the fundamental building block for local inference, and transformers is the fundamental building block for model definition, so this is basically a match made in heaven." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Not much – Georgi and team still dedicate 100% of their time maintaining llama.cpp and have full autonomy and leadership on the technical directions and the community." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
