---
title: MiniMax 时间线调研（2026-11）
type: source
tags: [notes]
source_note: "[[MiniMax调研-2026-11]]"
url: https://huggingface.co/MiniMaxAI
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/minimax]]"
  - "[[entities/minimax-m]]"
  - "[[entities/alibaba]]"
  - "[[entities/agentscope]]"
---

# MiniMax 时间线调研（2026-11）

## Summary

整理 [[entities/minimax|MiniMax（稀宇科技）]]从 2021-12 成立到 2026-11 的公司、上市、消费产品与模型时间线。MiniMax 有两条线：Talkie / 星野、海螺视频等消费产品，以及开放权重的大模型（见 [[entities/minimax-m|MiniMax-M]]）。模型路线先做长上下文：MiniMax-01 / M1 用线性与 Softmax 混合注意力，456B 参数、1M 上下文。M2 系列改为 10B 激活的小模型，主打编码与 Agent。M3 是约 428B / 23B 的原生多模态模型，用自研稀疏注意力 MSA，许可证收紧为社区许可。2026-01-09 在港交所上市。模型日期和许可证以 Hugging Face 模型卡为准（2026-11-05 读取）。

## Key Points

- **成立**：2021-12 上海，创始团队来自商汤，CEO 闫俊杰；早期获米哈游投资
- **股东**：[[entities/alibaba|阿里巴巴]] 2024-03 领投 6 亿美元（估值约 25 亿美元），腾讯、红杉中国、IDG 参与
- **MiniMax-01 / M1（2025-01 / 06）**：456B / 45.9B，Lightning Attention 混合架构，原生 1M 上下文；M1 是 Apache-2.0 的[[concepts/reasoning-model|推理模型]]
- **M2 系列（2025-10 至 2026-04）**：230B / 10B，Modified MIT；M2.1 同时推出 Agent 产品 MiniMax Code
- **上市（2026-01-09）**：港交所 0100，募资约 48.2 亿港元，首日收盘约翻倍
- **M3（2026-06-01）**：约 428B / 23B，原生多模态，1M 上下文，MSA 稀疏注意力；改用 MiniMax 社区许可证（非商用免费，商用需通知，年收入超 2000 万美元需书面授权）
- **M3.1-Flash（2026-10）**：面向编码、Agent、计算机操作与网络安全
- **生成模型**：海螺视频、Speech、Music，2026-07 开源 H3 音视频生成
- **争议**：2025-09 被迪士尼等起诉版权侵权；2026-02 被 [[entities/anthropic|Anthropic]] 指控蒸馏 Claude
- **与阿里生态**：2026-05-20 起阿里云百炼上架 M2.7；[[entities/agentscope|AgentScope]] 2026-09 起内置 `MiniMaxChatModel`（默认 M3）

## Mentioned Pages

- [[entities/minimax|MiniMax]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/anthropic|Anthropic]]
- [[entities/kimi|Kimi]]
- [[entities/glm|GLM]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/ai-agent|AI Agent]]
