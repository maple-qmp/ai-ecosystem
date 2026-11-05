---
title: Groq
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["Groq", "LPU", "Language Processing Unit", "GroqCloud"]
competitors: ["[[entities/nvidia]]", "[[entities/cerebras]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# Groq

自研推理专用芯片 LPU（Language Processing Unit）的公司，架构特点是用大容量片上 SRAM 替代 [[concepts/hbm|HBM]]、配确定性调度，强项是低延迟的 token 生成，只做推理不做训练。对外产品是 GroqCloud——提供 OpenAI 兼容的推理 API，官方 Python SDK 由 Stainless 生成。2025 年底 [[entities/nvidia|NVIDIA]] 以报道约 200 亿美元的非排他许可拿到其推理技术，创始人 Jonathan Ross 与总裁 Sunny Madra 加入 NVIDIA，而 Groq 作为公司独立存续、继续运营 GroqCloud。这笔交易的性质（收购、人才收购还是单纯许可）在业内仍有争论。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 公司
- **上游依赖**：—（自研芯片，刻意绕开 HBM 供应）
- **竞争 / 替代**：[[entities/nvidia|NVIDIA]] 的推理 GPU、[[entities/cerebras|Cerebras]]；在 API 层与各家托管推理服务竞争

## 时间线

- 2016 成立，创始人 Jonathan Ross（Google TPU 早期工程师之一）
- 2023-11-02 官方 Python SDK 首个 PyPI 版本
- 2025-12 下旬 与 NVIDIA 达成非排他推理技术许可，报道金额约 200 亿美元；Ross 与 Madra 加入 NVIDIA，公司独立存续
- 2026 参议员 Warren 与 Blumenthal 就该交易是否规避并购申报规则致信 FTC
- 2026 NVIDIA 基于该许可推出 Groq 3 LPX 推理系统（256 颗 LPU、液冷）
- 2026-08-26 `groq` SDK 1.7.0

## 相关实体

- [[entities/nvidia|NVIDIA]]
- [[entities/cerebras|Cerebras]]
- [[entities/vllm|vLLM]]
- [[entities/openai|OpenAI]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Groq Python library provides convenient access to the Groq REST API from any Python 3.10+ application." — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "2025-12 下旬 NVIDIA 与 Groq 达成非排他的推理技术许可，报道金额约 200 亿美元" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
