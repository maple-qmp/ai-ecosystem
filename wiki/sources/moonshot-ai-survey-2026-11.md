---
title: 月之暗面与 Kimi 时间线调研（2026-11）
type: source
tags: [notes]
source_note: "[[月之暗面-Kimi调研-2026-11]]"
url: https://huggingface.co/moonshotai
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/moonshot-ai]]"
  - "[[entities/kimi]]"
  - "[[entities/alibaba]]"
  - "[[entities/agentscope]]"
---

# 月之暗面与 Kimi 时间线调研（2026-11）

## Summary

整理 [[entities/moonshot-ai|月之暗面（Moonshot AI）]]从 2023-03 成立到 2026-11 的公司、融资和 [[entities/kimi|Kimi]] 模型时间线。2025-07 开源 Kimi K2（1T 总参数、32B 激活），此后 K2 Thinking、K2.5、K2.6、K2.7 Code 延续 1T / 32B 规格并保持 Modified MIT。2026-07 发布 K3（2.8T / 104B），许可证改为对 MaaS 厂商设收入门槛的自定义协议。估值从 2024-02 的 25 亿美元涨到 2026-07 的 350 亿美元。模型日期和许可证以 Hugging Face 模型卡为准（2026-11-05 读取）。

## Key Points

- **成立与股东**：2023-03 北京，创始人杨植麟等；[[entities/alibaba|阿里巴巴]] 2024-02 领投，腾讯 2024-08 入股
- **K2（2025-07-11）**：1T / 32B [[concepts/mixture-of-experts|MoE]]，开放权重，Modified MIT（月活过亿或月收入超 2000 万美元的产品须标注 “Kimi K2”）
- **K2 Thinking（2025-11-06）**：[[concepts/reasoning-model|推理]]与工具调用交替进行，原生 INT4 [[concepts/quantization|量化]]
- **Kimi Linear（2025-10-30）**：Kimi Delta Attention（KDA）混合线性注意力，后成为 K3 架构基础
- **K2.5（2026-01-27）**：原生多模态，Agent Swarm（多子 Agent 并行）；同期推出 CLI 编码 Agent Kimi Code
- **K2.6（2026-04-20）/ K2.7 Code（2026-06-12）**：Agent Swarm 扩到 300 子 Agent；编码专用版
- **K3（2026-07-16）**：2.8T / 104B，1M 上下文；Kimi K3 License 要求 12 个月收入超 2000 万美元的 MaaS 厂商另签协议
- **K3.1 Pro（2026-10-23）**：K3 的后训练升级
- **与阿里生态**：阿里是大股东；2026-05-20 起阿里云百炼上架 Kimi K2.6；[[entities/agentscope|AgentScope]]（Python）内置 Moonshot 提供方
- **争议**：2026-02 与 2026-09 两次被 [[entities/anthropic|Anthropic]] 指控蒸馏 Claude

## Mentioned Pages

- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/kimi|Kimi]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/anthropic|Anthropic]]
- [[entities/cursor|Cursor]]
- [[entities/qwen|Qwen]]
- [[entities/deepseek|DeepSeek]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/quantization|量化]]
- [[concepts/ai-agent|AI Agent]]
