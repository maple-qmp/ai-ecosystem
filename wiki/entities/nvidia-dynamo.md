---
title: NVIDIA Dynamo
type: entity
tags: [project]
kind: infra
layer: L3
aliases: ["NVIDIA Dynamo", "Dynamo", "ai-dynamo"]
org: "[[entities/nvidia]]"
released: "2025-03"
competitors: ["[[entities/llm-d]]"]
depends_on: ["[[entities/vllm]]", "[[entities/sglang]]", "[[entities/tensorrt-llm]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# NVIDIA Dynamo

## 描述

[[entities/nvidia|NVIDIA]] 开源的数据中心级推理栈，定位是推理引擎之上的编排层。它不替代 [[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]、[[entities/vllm|vLLM]]，而是把这些引擎组织成多节点协同的推理系统。核心能力包括[[concepts/disaggregated-serving|预填充 / 解码分离]]、KV 感知路由（把请求发到已缓存相同前缀的实例，避免重复预填充）、多层 [[concepts/kv-cache|KV cache]]、按延迟 SLA 自动扩缩和快速冷启动。性能部分用 Rust 写，扩展部分用 Python；KV 传输用 NIXL 在显存间直传。Apache-2.0 协议，160+ 社区贡献者；2026-03 发布 1.0 并宣布投产。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 推理编排
- **上游依赖**：推理引擎 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]；传输库 NIXL；[[entities/cuda|CUDA]]
- **竞争 / 替代**：[[entities/llm-d|llm-d]]、Ray Serve

## 时间线

- 2025-03-12 PyPI 首个开发包
- 2026-03 GTC 期间发布 1.0，宣布投产；报道列出的采用方有 CoreWeave、Nebius、Together AI、[[entities/cursor|Cursor]]、Perplexity、[[entities/bytedance|字节跳动]]、美团等，NVIDIA 称在 GB200 NVL 上推理性能最高提升 7 倍
- 2026-11 稳定版 1.6.1，1.7.0 开发中

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/llm-d|llm-d]]

## 相关概念

- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/kv-cache|KV cache]]
- [[concepts/speculative-decoding|推测解码]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The open-source, datacenter-scale inference stack." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Dynamo is the orchestration layer above inference engines — it doesn't replace SGLang, TensorRT-LLM, or vLLM, it turns them into a coordinated multi-node inference system." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Built in Rust for performance, Python for extensibility." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
