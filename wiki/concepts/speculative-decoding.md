---
title: 推测解码
type: concept
tags: [method]
layer: L3
aliases: ["推测解码", "投机解码", "Speculative decoding", "EAGLE", "MTP", "多 token 预测"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# 推测解码

## 定义

一种加速 LLM 解码的推理技术：先用便宜的办法一次猜出后面几个 token（草稿），再让目标模型用一次前向计算并行验证这些猜测，接受猜对的前缀，从第一个猜错的位置继续。因为最终输出仍由目标模型决定，输出分布不变（无损）；猜对的比例越高，每次前向产出的 token 越多，延迟越低。

## 关键特征

- **草稿来源**：
  - n-gram / 提示查找：从上下文里找重复片段，不需要额外模型，适合代码编辑、摘要这类大量复用原文的场景
  - 独立的小草稿模型
  - 草稿头：在目标模型的特征上训练轻量预测头，如 Medusa、EAGLE 系列
  - 多 token 预测（MTP）头：模型训练时自带的多 token 预测模块
  - suffix 解码、DFlash 等较新的方法
- **EAGLE 系列**：EAGLE 在 13B 模型上比普通解码快 3 倍，EAGLE-2 快 4 倍，EAGLE-3（2025-03 发布，NeurIPS'25 收录）快 5.6 倍；EAGLE-3 去掉了特征预测约束，改用低、中、高层语义特征融合
- **代价**：草稿计算和验证会占用额外算力，高并发、算力已饱和时收益下降

## 应用

- 降低交互式对话和编程 Agent 的单请求延迟
- 引擎支持：[[entities/vllm|vLLM]]（n-gram、suffix、EAGLE、DFlash）、[[entities/sglang|SGLang]]（EAGLE，配套 SpecForge 训练草稿模型）、[[entities/tensorrt-llm|TensorRT-LLM]]（n-gram 自动启用，并能与引导解码结合）
- 本地推理：[[concepts/gguf|GGUF]] 规范为 MTP 草稿模块定义了 `mtp` sidecar 文件

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]

## 相关概念

- [[concepts/kv-cache|KV cache]]
- [[concepts/disaggregated-serving|预填充 / 解码分离]]
- [[concepts/quantization|量化]]
- [[concepts/reasoning-model|推理模型]]

## 相关实体

- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/llama-cpp|llama.cpp]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "EAGLE-3 removes the feature prediction constraint in EAGLE and simulates this process during training using training-time testing." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
