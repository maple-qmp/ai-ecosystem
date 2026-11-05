---
title: 月之暗面（Moonshot AI）
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["月之暗面", "Moonshot AI", "Moonshot", "北京月之暗面科技有限公司"]
released: "2023"
competitors: ["[[entities/zhipu-ai]]", "[[entities/minimax]]", "[[entities/deepseek]]", "[[entities/alibaba]]", "[[entities/bytedance]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/moonshot-ai-survey-2026-11]]"]
---

# 月之暗面（Moonshot AI）

## 描述

2023-03 在北京成立的 AI 公司，创始人杨植麟、周昕宇、吴育昕，产品品牌是 [[entities/kimi|Kimi]]。早期靠长上下文的 Kimi 助手出名，2025-07 起转向开放权重：Kimi K2（1T 总参数、32B 激活的 [[concepts/mixture-of-experts|MoE]]）及之后的 K2 Thinking、K2.5、K2.6、K3，都放在 Hugging Face 上。[[entities/alibaba|阿里巴巴]]在 2024-02 领投，腾讯在 2024-08 入股。2026-07 估值 350 亿美元。研究方面有 Mooncake 推理架构（获 USENIX FAST 最佳论文）、Muon 优化器的规模化、Kimi Delta Attention 线性注意力。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：—（报道称使用 NVIDIA 集群，未单列）
- **竞争 / 替代**：[[entities/zhipu-ai|智谱]]、[[entities/minimax|MiniMax]]、[[entities/deepseek|DeepSeek]]、[[entities/alibaba|阿里巴巴（通义）]]、[[entities/bytedance|字节跳动]]

## 与阿里生态的关系

- **资本**：阿里巴巴 2024-02 领投约 10 亿美元，是主要股东
- **分发**：2026-05-20 起阿里云百炼可用统一 API 调用 Kimi K2.6，同批还有智谱 GLM-5.1、MiniMax M2.7
- **框架**：[[entities/agentscope|AgentScope]] Python 版把 Moonshot 列为内置模型提供方；[[entities/spring-ai-alibaba|Spring AI Alibaba]] 未单列，需通过 OpenAI 兼容接口或百炼接入
- **算力**：2026-07 Bloomberg 报道阿里云为其提供 H200 集群，阿里否认

## 时间线

- 2023-03 在北京成立
- 2023-10 Kimi 助手上线，单次对话约 20 万汉字
- 2024-02 阿里巴巴领投约 10 亿美元，估值约 25 亿美元
- 2024-03 宣称支持 200 万汉字上下文
- 2024-08 腾讯、高榕参与 3 亿美元融资，估值约 33 亿美元
- 2025-01-20 Kimi k1.5 推理模型
- 2025-07-11 开源 Kimi K2
- 2025-10 报道约 6 亿美元融资（IDG 领投）
- 2025-11-06 开源 Kimi K2 Thinking
- 2026-01-27 Kimi K2.5 与 Kimi Code
- 2026-02-23 [[entities/anthropic|Anthropic]] 指控其与 DeepSeek、MiniMax 用欺诈账号蒸馏 Claude
- 2026-03 报道考虑香港上市；[[entities/cursor|Cursor]] Composer 2 被报道基于 K2.5
- 2026-04-20 Kimi K2.6
- 2026-05-07 融资 20 亿美元，估值 200 亿美元
- 2026-05-20 Kimi K2.6 上架阿里云百炼
- 2026-06-12 Kimi K2.7 Code
- 2026-07-16 Kimi K3（2.8T），许可证改为 Kimi K3 License
- 2026-07-30 新一轮融资，估值 350 亿美元
- 2026-09-10 Anthropic 第二份蒸馏报告；09-22 报道网信办展开调查
- 2026-10-23 Kimi K3.1 Pro

## 相关实体

- [[entities/kimi|Kimi]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/minimax|MiniMax]]
- [[entities/deepseek|DeepSeek]]
- [[entities/anthropic|Anthropic]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "If the Licensee or any of its affiliates operates a Model as a Service business, and the aggregate revenue of the Licensee and its affiliates exceeds 20 million US dollars (or the equivalent in other currencies) in total over any consecutive 12 months, the Licensee must enter into a separate agreement with Moonshot AI before using the Software or its derivative works for any commercial purpose." — [[sources/moonshot-ai-survey-2026-11|月之暗面与 Kimi 调研]]（Kimi K3 License 第 2 条）
