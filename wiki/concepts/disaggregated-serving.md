---
title: 预填充 / 解码分离
type: concept
tags: [method]
layer: L3
aliases: ["预填充 / 解码分离", "PD 分离", "分离式推理", "Disaggregated serving", "Prefill-decode disaggregation"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# 预填充 / 解码分离

## 定义

一种 LLM 服务架构：把推理的两个阶段放到不同的 GPU 池上运行。预填充（prefill）一次性处理整段提示，是计算密集型；解码（decode）逐个生成 token，是访存密集型。两者混在同一组 GPU 上会互相干扰，分开之后可以各自选硬件、各自扩缩。代价是预填充 GPU 产生的 [[concepts/kv-cache|KV cache]] 必须通过高速网络传到解码 GPU。

## 关键特征

- **独立扩缩**：长提示多时加预填充节点，长输出多时加解码节点，按首 token 延迟和 token 间延迟两个指标分别优化
- **KV 传输**：NIXL（NVIDIA Inference Xfer Library）做显存到显存的非阻塞直传；LMCache 提供带多种存储后端的连接器。Ray Serve 同时提供 NIXLConnector 和 LMCacheConnectorV1
- **常与宽专家并行搭配**：大型 [[concepts/mixture-of-experts|MoE]] 模型（DeepSeek、gpt-oss）用分离式服务加跨节点专家并行
- **扩展到多模态**：[[entities/vllm|vLLM]] 还支持把编码（encode）阶段单独拆出

## 应用

- 编排层实现：[[entities/nvidia-dynamo|NVIDIA Dynamo]]、[[entities/llm-d|llm-d]]
- 引擎层支持：[[entities/vllm|vLLM]]、[[entities/sglang|SGLang]]、[[entities/tensorrt-llm|TensorRT-LLM]]
- 效果（llm-d README 引用合作方数据）：AWS 上 GPT-OSS / B200 比标准 vLLM 每秒 token 数最多高 70%；Oracle 上 AMD MI300X 吞吐提升 10–30%

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]]

## 相关概念

- [[concepts/kv-cache|KV cache]]
- [[concepts/speculative-decoding|推测解码]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]

## 相关实体

- [[entities/nvidia-dynamo|NVIDIA Dynamo]]
- [[entities/llm-d|llm-d]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]
- [[entities/tensorrt-llm|TensorRT-LLM]]
- [[entities/gpt-oss|gpt-oss]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Dynamo is the orchestration layer above inference engines — it doesn't replace SGLang, TensorRT-LLM, or vLLM, it turns them into a coordinated multi-node inference system." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
