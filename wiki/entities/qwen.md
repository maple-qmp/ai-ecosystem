---
title: Qwen
type: entity
tags: [product]
kind: model-family
layer: L2
aliases: ["Qwen", "通义千问", "Tongyi Qianwen", "QwQ", "Qwen3", "Qwen3.8"]
org: "[[entities/alibaba|阿里巴巴（通义）]]"
released: "2023-04"
open_weights: true
competitors: ["[[entities/deepseek-v]]", "[[entities/kimi]]", "[[entities/glm]]", "[[entities/minimax-m]]", "[[entities/doubao]]", "[[entities/llama]]", "[[entities/mistral-models]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/open-weight-flagships-survey-2026-11]]"]
---

# Qwen

## 描述

[[entities/alibaba|阿里云]]的模型家族，中文名通义千问，2023-04 内测、2023-09 通过监管后公开，最早基于 [[entities/llama|Llama]] 架构。家族覆盖从小参数稠密模型到 2.4T 的 [[concepts/mixture-of-experts|MoE]]，以及视觉（VL）、全模态（Omni）、推理（QwQ）等分支；宽松许可的小模型是社区微调最常用的基座之一，AI Singapore 2025-11 起用它替换 Llama。开放策略多次变化：Qwen3（2025-04）全系 Apache 2.0；Qwen3.5 到 3.7 的旗舰（Plus / Max）闭源；Qwen3.8 旗舰（2026-08）重新开放权重，但改用带收入门槛的自定义许可证，27B 等小模型仍是 Apache 2.0。Qwen App 2026-05 用户达 2.34 亿，中国区 Apple Intelligence 也接入了 Qwen。

## 生态位置

- **层级**：[[maps/L2-基础模型|L2-基础模型]] · 模型家族（开放权重为主，部分旗舰闭源）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/deepseek-v|DeepSeek-V]]、[[entities/kimi|Kimi]]、[[entities/glm|GLM]]、[[entities/minimax-m|MiniMax-M]]、[[entities/doubao|豆包]]（闭源）、[[entities/llama|Llama]]、[[entities/mistral-models|Mistral 模型]]

## 许可证

- Qwen3 全系、Qwen3.8-27B：Apache 2.0
- **Qwen3.8-Max License**（Qwen3.8-2.4T-A95B）：
  - 商用产品月活超过 1 亿或月收入超过 2000 万美元，须在界面显著标出模型名
  - 做“模型即服务”或“AI 工作助手”（编码、办公类）业务、连续 12 个月收入超过 5000 万美元，商用前须另签许可；内部使用不受限
- 对比：[[entities/glm|GLM-5.3]] 的同类门槛是 100 亿美元，[[entities/kimi|Kimi K3]] 是 2000 万美元

## 时间线

- 2023-04 通义千问内测；2023-09 公开
- 2023-08 / 12 Qwen-7B；Qwen-72B、1.8B 开放权重
- 2024-06 Qwen2
- 2024-11 QwQ-32B-Preview 推理模型（Apache 2.0）
- 2025-01-29 Qwen2.5-Max（闭源）
- 2025-04-28 Qwen3 全系 Apache 2.0
- 2026-02 Qwen3.5（开放）与 Qwen3.5-Plus（闭源）
- 2026-03 Qwen 负责人林俊旸离职
- 2026-04 Qwen3.5-Omni、Qwen3.6-Plus（闭源）
- 2026-05 / 06 Qwen3.7 Max / Plus（闭源）
- 2026-08-03 Qwen3.8-Max 云端版
- 2026-08-12 Qwen3.8-2.4T-A95B 开放权重（2.4T 总参数、95B 激活）
- 2026-08-14 Qwen3.8-27B（Apache 2.0）
- 2026-08-26 Qwen3.8-Flash；开放 Qwen3.8-Flash-Next
- 2026-09-18 Qwen3.8-Omni-Flash

## 相关实体

- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/spring-ai-alibaba|Spring AI Alibaba]]
- [[entities/llama|Llama]]
- [[entities/deepseek-v|DeepSeek-V]]
- [[entities/kimi|Kimi]]
- [[entities/glm|GLM]]
- [[entities/doubao|豆包]]
- [[entities/hugging-face|Hugging Face]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/lora|LoRA]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "If the licensee or any of its affiliates conducts a Model as a Service or AI Work Assistant business, and the aggregate revenue of the licensee and its affiliates exceeds US$50,000,000 (or the equivalent amount in any other currencies) during any consecutive twelve (12) months, the licensee shall obtain a separate license from Qwen before Using the Software or its derivative works for any commercial purpose." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（Qwen3.8-Max License）
