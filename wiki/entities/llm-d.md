---
title: llm-d
type: entity
tags: [project]
kind: infra
layer: L3
aliases: ["llm-d"]
released: ""
competitors: ["[[entities/nvidia-dynamo]]"]
depends_on: ["[[entities/vllm]]", "[[entities/sglang]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# llm-d

## 描述

面向 Kubernetes 生产部署的开源分布式推理服务栈，CNCF 沙箱项目，由 Red Hat、Google Cloud、IBM Research、CoreWeave 和 [[entities/nvidia|NVIDIA]] 发起。和 [[entities/nvidia-dynamo|NVIDIA Dynamo]] 一样，它不自己执行模型，而是在 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]] 等模型服务器之上做编排。主要能力是前缀缓存感知和负载感知的路由、分层 [[concepts/kv-cache|KV cache]] 卸载（CPU、磁盘）与全局索引、[[concepts/disaggregated-serving|预填充 / 解码分离]]与宽专家并行，以及面向 agent 多轮会话的路由和 Responses API 状态。项目以「well-lit path」形式提供经过基准测试的部署配方和 Helm chart。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 推理编排
- **上游依赖**：模型服务器 [[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]；Kubernetes
- **竞争 / 替代**：[[entities/nvidia-dynamo|NVIDIA Dynamo]]、Ray Serve

## 主要效果（README 引用合作方数据）

- 前缀缓存感知路由比轮询：输出吞吐 3 倍、首 token 快 2 倍（Llama 3.1 70B，4×AMD MI300X）
- 预填充 / 解码分离比标准 vLLM：每秒 token 数最多高 70%（GPT-OSS，NVIDIA B200，AWS）
- 分层 KV 卸载：250 并发时吞吐提升 13.9 倍（4×H100）

## 时间线

- 2026-03 入选 CNCF 沙箱（二手报道称 03-24）

## 相关实体

- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/nvidia|NVIDIA]]
- [[entities/gpt-oss|gpt-oss]]

## 相关概念

- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/kv-cache|KV cache]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "llm-d is a high-performance distributed inference serving stack optimized for production deployments on Kubernetes." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "llm-d is a Cloud Native Computing Foundation (CNCF) sandbox project, founded by Red Hat, Google Cloud, IBM Research, CoreWeave, and NVIDIA." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
