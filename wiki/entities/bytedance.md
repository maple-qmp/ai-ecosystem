---
title: 字节跳动
type: entity
tags: [organization]
kind: company
layer: X
aliases: ["字节跳动", "ByteDance", "字节", "火山引擎", "Volcano Engine", "Volcengine", "ByteDance Seed"]
competitors: ["[[entities/alibaba]]", "[[entities/moonshot-ai]]", "[[entities/zhipu-ai]]", "[[entities/minimax]]", "[[entities/deepseek]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/bytedance-doubao-survey-2026-11]]", "[[sources/multimodal-embedding-models-survey-2026-11]]"]
---

# 字节跳动

## 描述

抖音和 TikTok 的母公司，大模型业务分三块。Seed 团队负责研发：[[entities/doubao|豆包大模型（Doubao-Seed）]]、图像模型 Seedream、视频模型 Seedance，以及 Seed-OSS、UI-TARS 等开放权重中小模型。云服务火山引擎通过火山方舟提供模型 API，2024-05 以极低价格开放豆包大模型商用，引发国内价格战；IDC 数据显示它在中国公有云 MaaS 市场份额第一（49.5%）。面向用户和开发者的产品有豆包 App（国内用户最多的 AI 助手，海外版 Dola）、Agent 搭建平台 Coze（扣子，2025-07 部分开源）和 AI IDE TRAE。四家公司里只有字节的主力模型不开放权重。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 公司
- **上游依赖**：—
- **竞争 / 替代**：[[entities/alibaba|阿里巴巴（通义）]]（云与 C 端助手都正面竞争）、[[entities/moonshot-ai|月之暗面]]、[[entities/zhipu-ai|智谱]]、[[entities/minimax|MiniMax]]、[[entities/deepseek|DeepSeek]]

## 与阿里生态的关系

- **没有股权往来，正面竞争**：火山引擎（豆包）对阿里云百炼（通义 / [[entities/qwen|Qwen]]），豆包 App 对千问 App，Coze 对百炼应用和 [[entities/agentscope|AgentScope]]
- **框架**：AgentScope（Python）把 Volcengine 列为内置模型提供方

## 开发者产品

- **火山方舟**：豆包大模型的 API 平台
- **Coze**：Agent 搭建平台；2025-07 开源 Coze Studio（可视化开发）和 Coze Loop（运维评测），Apache-2.0
- **TRAE**：AI IDE，Seed 2.0 Pro 与 Code 模型首发的产品之一，Seed 2.1 也会接入
- **Eino**：Go 语言的 LLM 应用框架，比 Coze 更早开源

## 时间线

- 2023-08 豆包 App 上线；海外版 Cici 同月上线（后改名 Dola）
- 2024-05-15 火山引擎开放豆包大模型商用，Pro 32K 输入 0.0008 元 / 千 token，引发价格战
- 2024-11 豆包 App 月活约 6000 万
- 2024-12 视觉模型降价约 85%
- 2025-01 豆包 1.5 Pro；开源 UI-TARS
- 2025-06-11 FORCE 大会：豆包大模型 1.6、Seedance 1.0 Pro
- 2025-07-29 Coze Studio、Coze Loop 开源
- 2025-08 特斯拉中国车机接入豆包；08-20 开源 Seed-OSS-36B
- 2025-11 Doubao-Seed-Code 与低价编码订阅
- 2025-12-18 冬季 FORCE 大会：豆包大模型 1.8、Seedance 1.5 Pro
- 2026-02-14 Seed 2.0 与 [[entities/seedance|Seedance]] 2.0；Dola 开始改用自研 Seed 模型（4 月全量）
- 2026-02-13 迪士尼就 Seedance 2.0 发停止侵权函；3 月中旬暂停海外发布（二手）
- 2026-04 日均 token 约 120 万亿
- 2026-05 豆包用户约 3.3 亿，推出付费订阅
- 2026-06-23 夏季 FORCE 大会：Seed 2.1，日均 token 超 180 万亿；IDC 称火山引擎 MaaS 份额 49.5%
- 2026-07-15 豆包 App 为符合新监管规定下线 AI Agent 功能

## 相关实体

- [[entities/doubao|豆包]]
- [[entities/verl|verl]]
- [[entities/seedance|Seedance / 即梦]]
- [[entities/kuaishou|快手]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/agentscope|AgentScope]]
- [[entities/minimax|MiniMax]]
- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "The Doubao chatbot was launched in August 2023." — [[sources/bytedance-doubao-survey-2026-11|字节跳动与豆包调研]]（Wikipedia）
