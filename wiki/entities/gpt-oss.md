---
title: gpt-oss
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["gpt-oss", "gpt-oss-120b", "gpt-oss-20b", "gpt-oss-safeguard"]
org: "[[entities/openai]]"
released: "2025-08"
open_weights: true
competitors: ["[[entities/llama]]", "[[entities/qwen]]", "[[entities/deepseek-r1]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# gpt-oss

## 描述

[[entities/openai|OpenAI]] 在 2025-08 发布的开放权重推理模型家族，Apache-2.0 协议，是 OpenAI 自 GPT-2 以来第一次放出语言模型权重。两个尺寸都是 [[concepts/mixture-of-experts|混合专家（MoE）]]结构：gpt-oss-120b 总参数 117B、每 token 激活 5.1B；gpt-oss-20b 总参数 21B、激活 3.6B。MoE 权重以 MXFP4 [[concepts/quantization|量化]]后训练，所以 120b 能放进单张 80GB GPU，20b 在 16GB 内存里就能跑。属于[[concepts/reasoning-model|推理模型]]，推理强度可设 low / medium / high。模型只按 [[concepts/harmony-response-format|harmony 响应格式]]训练，不用这个格式输出会出错。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/deepseek-r1|DeepSeek-R1]]

## 脱离 OpenAI 使用

完全独立：下载权重后在本地或自有集群推理，不需要 OpenAI 账号。

- **推理引擎**：Hugging Face Transformers、[[entities/vllm|vLLM]]、Ollama、LM Studio
- **官方参考实现**（`openai/gpt-oss` 仓库）：PyTorch 版仅供教学，需 4×H100；Triton 版支持 MXFP4，可在单张 80GB GPU 上跑 120b；Apple Metal 版用于 Apple Silicon
- **工具参考实现**：模型训练时用过的浏览器工具和无状态 Python 工具
- **微调**：官方 Cookbook 有基于 [[entities/hugging-face|Hugging Face]] Transformers 的微调指南
- **接 Agent**：可作为 [[entities/codex-cli|Codex CLI]] `--oss` 模式和 [[entities/openai-agents-sdk|Agents SDK]] 的本地模型

## gpt-oss-safeguard

2025-10-29 发布的研究预览，120b 和 20b 两个尺寸，分别由对应的 gpt-oss 微调而来，同为 Apache-2.0。用途是按策略做内容安全分类：输入“开发者写的策略 + 待判定内容”，输出判定结果和推理过程。策略在推理时给出，改规则不用重训。与 Discord、SafetyKit、ROOST 合作开发。官方提示两点局限：有几万条标注数据时，专门训练的分类器在复杂高风险场景可能更准；对平台全量内容逐条跑，成本和延迟偏高。

## 时间线

- 2025-08 发布 gpt-oss-120b、gpt-oss-20b，同时开源 harmony 渲染库
- 2025-10-29 发布 gpt-oss-safeguard（研究预览）

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/gpt|GPT]]
- [[entities/vllm|vLLM]]
- [[entities/hugging-face|Hugging Face]]
- [[entities/codex-cli|Codex CLI]]

## 相关概念

- [[concepts/harmony-response-format|harmony 响应格式]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/quantization|量化]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "production, general purpose, high reasoning use cases that fit into a single 80GB GPU" — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]（gpt-oss README，描述 120b）
- "gpt-oss should not be used without using the harmony format as it will not work correctly." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]（harmony README）
