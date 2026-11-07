---
title: DeepSeek
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["DeepSeek", "深度求索", "杭州深度求索"]
released: "2023-07"
competitors: ["[[entities/alibaba]]", "[[entities/openai]]", "[[entities/moonshot-ai]]", "[[entities/zhipu-ai]]", "[[entities/minimax]]"]
depends_on: ["[[entities/nvidia]]", "[[entities/ascend]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-07
sources: ["[[sources/moonshot-ai-survey-2026-11]]", "[[sources/open-weight-flagships-survey-2026-11]]", "[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# DeepSeek

## 描述

总部位于杭州的中国 AI 公司，2023-07 从量化基金幻方（High-Flyer）孵化独立，创始人兼 CEO 梁文锋个人持股约 84%（2024-05）。只做开放权重模型，2025-01 起全部使用 MIT 等自由许可证，但不公开训练数据。代表作是 [[entities/deepseek-v|DeepSeek-V]] 系列基座和 [[entities/deepseek-r1|DeepSeek-R1]] 推理模型；R1 发布后其应用登顶美国 App Store，NVIDIA 股价单日下跌 18%。因美国芯片管制，公司长期围绕算力效率做算法优化，自建萤火集群和 3FS 文件系统等训练栈；2026 年开始转向华为昇腾。2026-05 完成 70 亿美元 A 轮，投后估值 520 亿美元，并在准备最早 2027 年 IPO。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：[[entities/nvidia|NVIDIA]]（早期 A100 集群）；[[entities/ascend|华为昇腾]]（2026 起）
- **竞争 / 替代**：[[entities/alibaba|阿里巴巴（通义）]]、[[entities/openai|OpenAI]]、[[entities/moonshot-ai|月之暗面]]、[[entities/zhipu-ai|智谱]]、[[entities/minimax|MiniMax]]

## 时间线

- 2023-04-14 幻方宣布成立 AGI 实验室
- 2023-07-17 实验室独立为 DeepSeek
- 2024-12 DeepSeek-V3
- 2025-01-20 DeepSeek-R1 与同名聊天应用；01-27 登顶美国 App Store
- 2025-03 起其聊天应用被解放军用于非作战岗位（NYT 报道）
- 2025-08 V3.1；2025-12 V3.2
- 2026-02-23 [[entities/anthropic|Anthropic]] 指控其与月之暗面、MiniMax 用欺诈账号蒸馏 Claude
- 2026-04-24 DeepSeek-V4 预览（1.6T，1M 上下文）
- 2026-05 A 轮 70 亿美元，投后估值 520 亿美元
- 2026-07 报道准备 IPO
- 2026-08 发布开源 Agent 框架 [[entities/deepseek-harness|DeepSeek Harness]]（MIT，开发者预览）
- 2026-09 报道计划在内蒙古建含 16 万张昇腾 950DT 的数据中心；V4.1-Flash 发布

## 相关实体

- [[entities/deepseek-v|DeepSeek-V]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[entities/qwen|Qwen]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/minimax|MiniMax]]

## 相关概念

- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/reasoning-model|推理模型]]
- [[concepts/agent-harness|Agent Harness]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We present a preview version of **DeepSeek-V4** series, including two strong Mixture-of-Experts (MoE) language models — **DeepSeek-V4-Pro** with 1.6T parameters (49B activated) and **DeepSeek-V4-Flash** with 284B parameters (13B activated) — both supporting a context length of **one million tokens**." — [[sources/open-weight-flagships-survey-2026-11|开放权重旗舰模型调研]]（DeepSeek-V4 模型卡）
