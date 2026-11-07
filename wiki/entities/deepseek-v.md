---
title: DeepSeek-V
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["DeepSeek-V", "DeepSeek-V3", "DeepSeek-V3.1", "DeepSeek-V3.2", "DeepSeek-V4", "DeepSeek V4"]
org: "[[entities/deepseek|DeepSeek]]"
released: "2024-12"
open_weights: true
competitors: ["[[entities/qwen]]", "[[entities/kimi]]", "[[entities/glm]]", "[[entities/minimax-m]]", "[[entities/gpt]]"]
depends_on: ["[[entities/ascend]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-07
sources: ["[[sources/open-weight-flagships-survey-2026-11]]", "[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# DeepSeek-V

## 描述

[[entities/deepseek|DeepSeek]] 的主线基座模型系列，全部以 MIT 许可开放权重。V3（2024-12）是大型 [[concepts/mixture-of-experts|MoE]]，也是推理模型 [[entities/deepseek-r1|DeepSeek-R1]] 的基座；V3.1（2025-08）把思考与非思考模式合进同一个模型，R1 线从此并入主线；V3.2 引入 DeepSeek 稀疏注意力（DSA）。V4（2026-04 预览）分 V4-Pro（1.6T 总参数 / 49B 激活）和 V4-Flash（284B / 13B），都支持 1M 上下文，用压缩稀疏注意力（CSA）与重度压缩注意力（HCA）组成的混合注意力，1M 长度下 V4-Pro 的单 token 推理 FLOPs 只有 V3.2 的 27%、[[concepts/kv-cache|KV Cache]] 只要 10%。V4.1-Flash（2026-09）改为因果编码器-解码器结构并原生多模态。V4 已被[[entities/ascend|昇腾]]、[[entities/cambricon|寒武纪]]等国产芯片适配：华为称昇腾 SuperNode 全系完成 V4 推理适配，并有团队称在昇腾 SuperPOD 上完成 V4 家族的全参数后训练；训练主体是否在昇腾上完成，各方口径仍有分歧。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重，MIT）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/qwen|Qwen]]、[[entities/kimi|Kimi]]、[[entities/glm|GLM]]、[[entities/minimax-m|MiniMax-M]]；闭源对手 [[entities/gpt|GPT]]

## 时间线

- 2024-12 DeepSeek-V3
- 2025-08-21 V3.1：思考 / 非思考混合；09-22 V3.1-Terminus
- 2025-09-29 V3.2-Exp：DeepSeek 稀疏注意力
- 2025-12-01 V3.2 与偏推理的 V3.2-Speciale
- 2026-04-24 V4 预览：V4-Pro、V4-Flash，1M 上下文
- 2026-07-31 V4-Flash 正式版；08-13 V4-Pro 正式版
- 2026-09-10 V4.1-Flash：编码器-解码器，原生多模态

## 相关实体

- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/qwen|Qwen]]
- [[entities/kimi|Kimi]]
- [[entities/vllm|vLLM]]
- [[entities/sglang|SGLang]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/kv-cache|KV Cache]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We present a preview version of **DeepSeek-V4** series, including two strong Mixture-of-Experts (MoE) language models — **DeepSeek-V4-Pro** with 1.6T parameters (49B activated) and **DeepSeek-V4-Flash** with 284B parameters (13B activated) — both supporting a context length of **one million tokens**." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（DeepSeek-V4 模型卡）
- "In the 1M-token context setting, DeepSeek-V4-Pro requires only **27% of single-token inference FLOPs** and **10% of KV cache** compared with DeepSeek-V3.2." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（DeepSeek-V4 模型卡）
