---
title: MiniMax
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["MiniMax", "稀宇科技", "上海稀宇科技", "海螺AI", "Hailuo AI"]
released: "2021"
competitors: ["[[entities/moonshot-ai]]", "[[entities/zhipu-ai]]", "[[entities/deepseek]]", "[[entities/bytedance]]", "[[entities/alibaba]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/minimax-survey-2026-11]]"]
---

# MiniMax

## 描述

2021-12 在上海成立的 AI 公司（稀宇科技），创始团队来自商汤，CEO 闫俊杰，公司名取自博弈论的 Minimax 算法。业务有两条线：一是消费产品，包括海外的 Talkie、国内的星野、视频生成平台海螺 AI（Hailuo），以及语音和音乐；二是开放平台和开放权重的语言模型（见 [[entities/minimax-m|MiniMax-M]]）。[[entities/alibaba|阿里巴巴]]在 2024-03 领投。2026-01-09 在港交所上市（代码 0100），是继[[entities/zhipu-ai|智谱]]之后第二家上市的中国大模型公司。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室（已上市）
- **上游依赖**：—
- **竞争 / 替代**：[[entities/moonshot-ai|月之暗面]]、[[entities/zhipu-ai|智谱]]、[[entities/deepseek|DeepSeek]]、[[entities/bytedance|字节跳动]]（视频生成方向直接竞争）、[[entities/alibaba|阿里巴巴（通义）]]

## 与阿里生态的关系

- **资本**：阿里巴巴 2024-03 领投 6 亿美元
- **分发**：2026-05-20 起阿里云百炼可用统一 API 调用 MiniMax M2.7
- **框架**：[[entities/agentscope|AgentScope]]（Python）2026-09 起内置 `MiniMaxChatModel`，默认模型 MiniMax-M3；[[entities/spring-ai-alibaba|Spring AI Alibaba]] 未单列

## 时间线

- 2021-12 在上海成立
- 2022-04 abab1；2022-10 abab3 与首个消费应用 Glow
- 2023-03 Glow 在国内应用商店下架
- 2023-06 海外版 Talkie；2023-09 国内版星野
- 2024-03 阿里巴巴领投 6 亿美元，估值约 25 亿美元；海螺 AI 上线
- 2024-04-17 abab 6.5 系列
- 2024-09 视频模型 video-01
- 2025-01 MiniMax-01 开放权重
- 2025-06 MiniMax-M1
- 2025-09 迪士尼、环球、华纳兄弟探索在美起诉海螺 AI 侵犯版权
- 2025-10 MiniMax-M2
- 2025-12 MiniMax-M2.1 与 MiniMax Code
- 2026-01-09 港交所上市（0100），发行价 165 港元，募资约 48.2 亿港元
- 2026-02 MiniMax-M2.5；[[entities/anthropic|Anthropic]] 指控其参与蒸馏 Claude
- 2026-03 / 04 MiniMax-M2.7
- 2026-05-20 M2.7 上架阿里云百炼
- 2026-06-01 MiniMax-M3，许可证改为社区许可
- 2026-07 开源 MiniMax-H3 音视频生成
- 2026-08 MiniMax-Music3
- 2026-09 AgentScope 内置 MiniMax 模型
- 2026-10 MiniMax-M3.1-Flash

## 相关实体

- [[entities/minimax-m|MiniMax-M]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/bytedance|字节跳动]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "MiniMax chat models supported via `MiniMaxChatModel` (MiniMax-M3 by default)." — [[sources/minimax-survey-2026-11|MiniMax 调研]]（AgentScope README）
