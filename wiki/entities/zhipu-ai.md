---
title: 智谱（Z.ai）
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["智谱", "智谱AI", "Zhipu AI", "Z.ai", "智谱华章", "Knowledge Atlas"]
released: "2019"
competitors: ["[[entities/moonshot-ai]]", "[[entities/minimax]]", "[[entities/deepseek]]", "[[entities/alibaba]]", "[[entities/bytedance]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-07
sources: ["[[sources/zhipu-ai-survey-2026-11]]"]
---

# 智谱（Z.ai）

## 描述

北京智谱华章科技股份有限公司，2019 年从清华大学知识工程实验室（KEG）孵化，核心人物唐杰；国际品牌 2025-07 起改为 Z.ai，英文公司名 Knowledge Atlas Technology。它研发 [[entities/glm|GLM]] 模型家族：早期的 ChatGLM-6B 是国内最早被广泛本地部署的开源对话模型之一，2025 年起的 GLM-4.5、GLM-5 系列以 MIT 协议开放权重。2026-01-08 在港交所上市（代码 2513），是中国第一家上市的大模型公司。2025-01 被列入美国实体清单，此后积极适配华为昇腾、[[entities/cambricon|寒武纪]]、摩尔线程等国产芯片。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室（已上市）
- **上游依赖**：—（NVIDIA H20 与多种国产芯片）
- **竞争 / 替代**：[[entities/moonshot-ai|月之暗面]]、[[entities/minimax|MiniMax]]、[[entities/deepseek|DeepSeek]]、[[entities/alibaba|阿里巴巴（通义）]]、[[entities/bytedance|字节跳动]]

## 与阿里生态的关系

- **资本**：阿里巴巴是 2023 年约 25 亿元融资的投资方之一（同轮有[[entities/tencent|腾讯]]、美团、蚂蚁、小米、红杉中国）
- **分发**：2026-05-20 起阿里云百炼可用统一 API 调用 GLM-5.1
- **框架**：[[entities/agentscope|AgentScope]] 与 [[entities/spring-ai-alibaba|Spring AI Alibaba]] 都没有单列智谱，可通过 OpenAI 兼容接口或百炼接入

## 时间线

- 2019 成立，清华 KEG 孵化
- 2022-05 GLM 论文发表于 ACL
- 2023-03 开源 ChatGLM-6B
- 2023 获阿里巴巴、腾讯、美团等约 25 亿元投资
- 2024-05 沙特 Prosperity7 参与 4 亿美元融资，估值约 30 亿美元
- 2024-07 视频生成产品“清影”；2024-10 手机 Agent AutoGLM
- 2025-01 被列入美国实体清单
- 2025-04 起旗舰模型改用 MIT 许可
- 2025-07 启用 Z.ai 国际品牌；07-28 GLM-4.5
- 2025-08 宣布适配华为昇腾
- 2026-01-08 港交所上市（2513）
- 2026-02 GLM-5；下旬因算力紧张限制新用户注册，股价一度跌约 23%
- 2026-04-07 GLM-5.1 开源，API 涨价 10%
- 2026-05-20 GLM-5.1 上架阿里云百炼
- 2026-06-16 GLM-5.2
- 2026-07-02 发布桌面编码应用 ZCode；07-14 港交所公告更改英文名称
- 2026-08 GLM-5.3，许可证收紧；市值约 620 亿美元
- 2026-09 NIST CAISI 评估称 GLM-5.3 是网络能力最强的开放权重模型

## 相关实体

- [[entities/glm|GLM]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/minimax|MiniMax]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "China's first major LLM company to make initial public offering, on the Hong Kong Stock Exchange in January 2026." — [[sources/zhipu-ai-survey-2026-11|智谱与 GLM 调研]]（Wikipedia）
