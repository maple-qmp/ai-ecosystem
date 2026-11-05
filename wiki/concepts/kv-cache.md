---
title: KV cache
type: concept
tags: [method]
layer: L3
aliases: ["KV cache", "KV 缓存", "键值缓存", "PagedAttention", "RadixAttention", "前缀缓存", "prefix caching"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# KV cache

## 定义

Transformer 自回归解码时，每个已处理 token 的注意力 key / value 张量会保留在显存里，供生成后续 token 时复用，这部分缓存叫 KV cache。它随上下文长度和并发数线性增长，而且大小动态变化，是 LLM 服务的主要显存瓶颈，所以推理引擎的大部分优化都围绕它展开：怎么存得省、怎么在请求之间复用、怎么在显存放不下时卸载到别处。

## 关键特征

- **分页管理（PagedAttention）**：[[entities/vllm|vLLM]] 2023 年提出，借鉴操作系统虚拟内存分页，把 KV cache 切成固定大小的块，块在显存里不必连续。vLLM 的测量是，此前的系统因碎片和过度预留浪费 60%–80% 的 KV cache 显存
- **前缀复用（RadixAttention）**：[[entities/sglang|SGLang]] 2024 年提出，请求结束后不丢弃 KV cache，而是把提示和生成结果存进基数树，新请求自动匹配最长公共前缀；与连续批处理、PagedAttention 兼容
- **前缀缓存**：之后 vLLM 等引擎也内置了自动前缀缓存。系统提示、多轮对话历史、agent 的工具定义都是共享长前缀，命中后可以跳过预填充
- **分层卸载与跨实例共享**：显存放不下时把 KV 卸载到 CPU 内存或磁盘，或在多个推理实例间共享。LMCache 提供这一层；[[entities/llm-d|llm-d]] 做全局 KV 索引，[[entities/nvidia-dynamo|NVIDIA Dynamo]] 做多层 KV 缓存
- **KV 感知路由**：编排层把请求发到已缓存相同前缀的实例
- **压缩与量化**：降低 KV 精度或做稀疏化，例如 [[entities/tensorrt-llm|TensorRT-LLM]] 2026-10 的 KV cache 压缩

## 应用

- 提高并发与吞吐：同样显存下装下更多请求
- 降低首 token 延迟：前缀命中时省去重复的预填充计算
- agent 与多轮对话：[[entities/llm-d|llm-d]] 用会话感知路由在轮次之间复用上下文；它在 4×H100、250 并发下用分层 KV 卸载让吞吐提升 13.9 倍
- [[concepts/disaggregated-serving|预填充 / 解码分离]]：KV cache 要从预填充 GPU 传到解码 GPU

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]
- 引擎层：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]
- 编排层：[[entities/nvidia-dynamo|NVIDIA Dynamo]]、[[entities/llm-d|llm-d]]

## 相关概念

- [[concepts/transformer|Transformer]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/speculative-decoding|推测解码]]
- [[concepts/quantization|量化]]

## 相关实体

- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/llm-d|llm-d]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "To address this problem, we introduce PagedAttention, an attention algorithm inspired by the classic idea of virtual memory and paging in operating systems." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "KV cache reuse means different prompts with the same prefix can share the intermediate KV cache and avoid redundant memory and computation." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Instead of discarding the KV cache after finishing a generation request, our approach retains the KV cache for both prompts and generation results in a radix tree." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Furthermore, RadixAttention is compatible with existing techniques like continuous batching and paged attention." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
