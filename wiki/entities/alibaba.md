---
title: 阿里巴巴（通义）
type: entity
tags: [organization]
kind: company
layer: X
aliases: ["阿里巴巴", "Alibaba", "Alibaba Group", "阿里云", "通义", "千问"]
competitors: ["[[entities/deepseek]]", "[[entities/meta-ai]]", "[[entities/bytedance]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-06
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]", "[[sources/moonshot-ai-survey-2026-11]]", "[[sources/zhipu-ai-survey-2026-11]]", "[[sources/minimax-survey-2026-11]]", "[[sources/open-weight-flagships-survey-2026-11]]", "[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/major-ai-orgs-survey-2026-11]]"]
---

# 阿里巴巴（通义）

## 描述

阿里巴巴集团及阿里云，2023 年起由蔡崇信任董事会主席、吴泳铭任 CEO。研发 [[entities/qwen|Qwen（通义千问）]] 系列，是全球下载量最大的开放权重模型家族之一，同时通过阿里云提供算力与模型服务。2025-02 宣布未来三年在云和 AI 基础设施上投入至少 3800 亿元，超过过去十年总和。C 端产品 2025-11-17 由通义 App 改版为“千问”App，接入 Qwen3-Max，2026-01 起接入外卖等阿里生态服务。在 Java Agent 开发方向开源了 [[entities/spring-ai-alibaba|Spring AI Alibaba]] 和 [[entities/agentscope|AgentScope]]（Java 版官方称在集团内 13+ 个业务单元生产使用）。阿里同时是多家中国模型公司的早期投资方：2023 年投资[[entities/zhipu-ai|智谱]]，2024-02 领投[[entities/moonshot-ai|月之暗面]]，2024-03 领投 [[entities/minimax|MiniMax]]；2026-05 起，阿里云百炼也上架了这三家的模型。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 公司
- **上游依赖**：—
- **竞争 / 替代**：[[entities/deepseek|DeepSeek]]、[[entities/meta-ai|Meta AI]]、[[entities/bytedance|字节跳动]]（火山引擎对阿里云百炼，豆包对千问）

## 与其他中国模型公司的关系

- **[[entities/moonshot-ai|月之暗面]]**：2024-02 领投约 10 亿美元，是主要股东；百炼上架 [[entities/kimi|Kimi]] K2.6；2026-07 有报道称阿里云为其提供 H200 集群，阿里否认
- **[[entities/zhipu-ai|智谱]]**：2023 年约 25 亿元融资的投资方之一；百炼上架 [[entities/glm|GLM]]-5.1
- **[[entities/minimax|MiniMax]]**：2024-03 领投 6 亿美元；百炼上架 [[entities/minimax-m|MiniMax]] M2.7
- **[[entities/bytedance|字节跳动]]**：没有股权关系，在云和 C 端助手上正面竞争
- **百炼第三方模型**：2026-05-20 阿里云峰会宣布百炼用统一 API 接入第三方模型，首批有 GLM-5.1、MiniMax M2.7、Kimi K2.6，以及多家公司的视频和多模态模型
- **框架侧**：[[entities/agentscope|AgentScope]]（Python）内置 Moonshot、Volcengine、MiniMax 提供方；[[entities/spring-ai-alibaba|Spring AI Alibaba]] 官方只单列 DashScope 等，其他模型通过 OpenAI 兼容接口或百炼接入

## 时间线

- 2023 投资智谱
- 2023 蔡崇信任董事会主席、吴泳铭任 CEO
- 2023-04 通义千问发布
- 2023 起陆续开源 Qwen 系列
- 2024-02 领投月之暗面
- 2024-03 领投 MiniMax
- 2025-02 宣布三年投入至少 3800 亿元建设云与 AI 基础设施
- 2025-04-28 Qwen3 全系 Apache 2.0
- 2025-06 开放 [[entities/qwen3-embedding|Qwen3-Embedding]] 与 Qwen3-Reranker
- 2025-11-17 通义 App 改版为“千问”App 公测，一周下载量破千万，23 天月活破 3000 万（官方口径，含 Web 与 PC）
- 2026-01 Qwen3-VL-Embedding / Reranker；千问 App 接入外卖等阿里生态服务
- 2026-02 Qwen3.5 开放权重，闭源 Qwen3.5-Plus
- 2026-03 Qwen 负责人林俊旸离职，阿里表示继续开源；阿里国际推出电商 Agent 平台 Accio Work
- 2026-04 Qwen3.6（Apache 2.0）
- 2026-05-20 百炼上架第三方模型（GLM-5.1、MiniMax M2.7、Kimi K2.6 等）
- 2026-06 被 [[entities/anthropic|Anthropic]] 指控蒸馏 Claude
- 2026-08-12 开放 Qwen3.8 旗舰权重（2.4T），改用带收入门槛的许可证，见 [[entities/qwen|Qwen]]；08-14 Qwen3.8-27B 以 Apache 2.0 开放

## 相关实体

- [[entities/qwen|Qwen]]
- [[entities/qwen3-embedding|Qwen3-Embedding]]
- [[entities/deepseek|DeepSeek]]
- [[entities/spring-ai-alibaba|Spring AI Alibaba]]
- [[entities/agentscope|AgentScope]]
- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/minimax|MiniMax]]
- [[entities/bytedance|字节跳动]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/java-agent-development|Java Agent 开发]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Former Qwen AI model division head, Lin Junyang, resigned in March 2026 after the release of Qwen3.5 and Qwen3.5-Plus" — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Wikipedia）
