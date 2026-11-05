---
title: SGLang
type: entity
tags: [project]
kind: framework
layer: L3
aliases: ["SGLang", "sgl-project/sglang"]
org: "[[entities/radixark]]"
released: "2024-01"
competitors: ["[[entities/vllm]]", "[[entities/tensorrt-llm]]"]
depends_on: ["[[entities/pytorch]]", "[[entities/cuda]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]", "[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# SGLang

## 描述

开源推理框架，面向大语言模型、视觉语言模型和扩散模型，针对 agent 工作负载、大规模服务和强化学习 rollout 做了优化。2024-01 由 LMSYS 发布，核心创新是 RadixAttention：请求结束后把 [[concepts/kv-cache|KV cache]] 保存在基数树里，自动复用共享前缀，因此多轮对话和 agent 这类长前缀负载收益最大。项目由非营利组织 LMSYS 托管，Apache-2.0 协议；2026 年核心团队成立 [[entities/radixark|RadixArk]] 做商业化。与 [[entities/vllm|vLLM]] 是数据中心开源推理的两大主力，设计上借鉴并复用过 vLLM、FlashInfer、Guidance 等项目的代码。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 推理引擎
- **上游依赖**：[[entities/pytorch|PyTorch]]、[[entities/cuda|CUDA]]；注意力内核 FlashInfer；TPU 路径用 JAX / Pallas
- **下游 / 编排**：[[entities/nvidia-dynamo|NVIDIA Dynamo]]、[[entities/llm-d|llm-d]]、Ray Serve；RL 框架 Miles、slime、AReaL、verl、Tunix 用它生成 rollout
- **竞争 / 替代**：[[entities/vllm|vLLM]]、[[entities/tensorrt-llm|TensorRT-LLM]]

## 主要组件

- **SGLang 运行时**：RadixAttention 前缀复用、连续批处理、[[concepts/speculative-decoding|推测解码]]、[[concepts/disaggregated-serving|预填充 / 解码分离]]
- **SGLang Diffusion**：内置的图像、视频生成引擎
- **SGLang Omni**：语音模型服务（TTS、ASR）
- **SpecForge**：训练推测解码的草稿模型，再部署到 SGLang
- **硬件**：NVIDIA（Blackwell 到 Jetson）、[[entities/amd-instinct|AMD Instinct]]、[[entities/google-tpu|Google TPU]]（SGLang-TorchTPU、SGL-JAX）、Intel、Apple Silicon、[[entities/ascend|华为昇腾]]、摩尔线程；在接入 [[entities/aws-trainium|AWS Trainium]]、平头哥 PPU、寒武纪等

## 时间线

- 2024-01-16 PyPI 首个版本
- 2024-01-17 LMSYS 发布博客，介绍 RadixAttention，称吞吐最高提升 5 倍
- 2026-01-21 报道称团队拆分成立 [[entities/radixark|RadixArk]]，估值约 4 亿美元
- 2026-05-05 RadixArk 宣布 1 亿美元种子轮
- 2026-10-30 发布 0.5.23
- 2026-11-12 至 13 SGLang Summit 2026（旧金山）

## 相关实体

- [[entities/radixark|RadixArk]]
- [[entities/vllm|vLLM]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/llm-d|llm-d]]
- [[entities/pytorch|PyTorch]]
- [[entities/claude-code|Claude Code]]（长期贡献者可获赞助）

## 相关概念

- [[concepts/kv-cache|KV cache]]
- [[concepts/speculative-decoding|推测解码]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "SGLang is an open-source inference framework for large language, vision-language, and diffusion models, optimized for agentic workloads, large-scale serving, and RL rollouts." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "SGLang is hosted by LMSYS, a non-profit open-source organization." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "On the backend, we propose RadixAttention, a technique for automatic and efficient KV cache reuse across multiple LLM generation calls." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
