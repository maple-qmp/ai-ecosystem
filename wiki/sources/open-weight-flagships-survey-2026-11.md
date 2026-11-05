---
title: 开放权重旗舰模型时间线调研：Llama / Muse、Qwen、DeepSeek、Mistral（2026-11）
type: source
tags: [notes]
source_note: "[[开放权重旗舰模型时间线调研-2026-11]]"
url: https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/llama]]"
  - "[[entities/muse]]"
  - "[[entities/meta-ai]]"
  - "[[entities/qwen]]"
  - "[[entities/alibaba]]"
  - "[[entities/deepseek]]"
  - "[[entities/deepseek-v]]"
  - "[[entities/deepseek-r1]]"
  - "[[entities/mistral-ai]]"
  - "[[entities/mistral-models]]"
---

# 开放权重旗舰模型时间线调研：Llama / Muse、Qwen、DeepSeek、Mistral（2026-11）

## Summary

核实 [[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/deepseek|DeepSeek]] 三个种子页和 [[entities/mistral-ai|Mistral AI]]，新增 [[entities/muse|Meta Muse]]、[[entities/deepseek-v|DeepSeek-V]] 和 [[entities/mistral-models|Mistral 模型]]。版本日期与许可证取 Hugging Face 模型卡和 API 元数据，公司事件取 Wikipedia（2026-11-05 读取）。Meta 在 Llama 4（2025-04）之后停更，2026-04 以闭源的 Muse Spark 取代。DeepSeek 一直用 MIT，V4（2026-04 预览）做到 1.6T 参数、1M 上下文。Qwen 和 Mistral 的最大模型改用自定义许可证：Qwen3.8 对年收入超过 5000 万美元的模型服务商要求另签许可，Mistral Large 4 使用 Mistral Ecosystem Open-Weight License。

## Key Points

- **Llama**：2023-02 到 2025-04 共四代；Llama 4 改为 [[concepts/mixture-of-experts|MoE]] 与原生多模态，LMArena 成绩争议；许可证被 FSF 认定为非自由
- **Muse**：Meta Superintelligence Labs 2026-04 发布 Muse Spark，替代 Llama 驱动 Meta AI；开放权重版的细节只见于二手报道
- **Qwen**：开放策略多次变化，Qwen3 全系 Apache 2.0，3.5～3.7 的旗舰闭源，Qwen3.8 旗舰（2.4T / 95B 激活）重新开放但许可证加门槛；27B 等小模型仍是 Apache 2.0
- **DeepSeek**：V3（2024-12）、R1（2025-01）、V3.1 混合思考、V3.2 稀疏注意力、V4（1.6T / 49B，1M 上下文，KV cache 只要 V3.2 的 10%）、V4.1-Flash（编码器-解码器）；2026-05 估值 520 亿美元
- **Mistral**：欧洲估值最高的 AI 公司（2026-09 约 247 亿美元）；Mistral Large 4 是 1T / 49B 激活的 MoE，在自建欧洲机房训练
- **许可证收紧是共同趋势**：GLM-5.3（100 亿美元）、Kimi K3（2000 万美元）、Qwen3.8（5000 万美元）都对大型模型服务商设门槛；DeepSeek 仍是标准 MIT
- **国产芯片**：DeepSeek V4 被华为、寒武纪适配，计划在内蒙古部署 16 万张昇腾 950DT

## Mentioned Pages

- [[entities/llama|Llama]]
- [[entities/muse|Meta Muse]]
- [[entities/meta-ai|Meta AI]]
- [[entities/qwen|Qwen]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-v|DeepSeek-V]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/mistral-ai|Mistral AI]]
- [[entities/mistral-models|Mistral 模型]]
- [[entities/glm|GLM]]
- [[entities/kimi|Kimi]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/kv-cache|KV Cache]]
- [[concepts/reasoning-model|推理模型]]
