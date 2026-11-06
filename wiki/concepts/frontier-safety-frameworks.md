---
title: 前沿模型安全框架
type: concept
tags: [standard]
layer: X
aliases: ["前沿模型安全框架", "Frontier Safety Frameworks", "Responsible Scaling Policy", "RSP", "负责任扩展政策", "Preparedness Framework", "准备度框架", "ASL"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-policy-survey-2026-11]]"]
---

# 前沿模型安全框架

## 定义

前沿 AI 实验室自愿发布的风险管理政策，规定模型能力达到哪些危险阈值（生物化学武器、网络攻击、AI 自主研发等）时必须配套哪些防护措施，否则不得训练或部署。代表是 [[entities/anthropic|Anthropic]] 的 Responsible Scaling Policy（RSP）和 [[entities/openai|OpenAI]] 的 Preparedness Framework。2025–2026 年，[[concepts/california-sb-53|加州 SB 53]]、纽约 RAISE Act 和[[concepts/eu-ai-act|欧盟 AI Act]] 实践准则开始要求开发者公开这类框架。

## 关键特征

### Anthropic RSP

- **版本**：1.0（2023-09-19）、2.0（2024-10-15）、2.1、2.2（2025-05-14）、3.0（2026-02-24，全面重写）、3.1–3.4（2026-04 至 2026-07-08，3.4 为当前版本）
- **AI 安全等级（ASL）**：能力越过阈值（如 CBRN、AI 研发自动化）时须满足相应的部署与安保标准；ASL-3 部署防护包括访问控制、实时分类器、异步监控和越狱快速响应
- **v3 的变化**：分开列出 Anthropic 自己的承诺和对全行业的建议；新增公开的前沿安全路线图（Frontier Safety Roadmap，目标不具约束力）；每 3–6 个月发布风险报告（Risk Report），特定情况下需外部审查；评论认为 v3 删去了部分硬性承诺（二手）
- 保留负责任扩展官（RSO）、董事会监督和匿名举报渠道（二手）

### OpenAI Preparedness Framework

- 2023-12 发布 beta 版；第 2 版 2025-04-15 发布，截至 2026 年中仍是现行版本（二手）
- **跟踪类别**：生物与化学、网络安全、AI 自我改进。v2 把原“模型自主”拆开：AI 自我改进升为跟踪类别，长程自主、自主复制与适应列为研究类别
- **两级阈值**：
  - High：显著增加现有的严重危害途径，部署前须有足以把风险降到足够低的防护
  - Critical：带来性质全新、无先例的严重危害途径，无论是否计划部署，开发期间就须有防护
- **安全顾问组（SAG）**：OpenAI 领导层组成的内部跨部门小组，负责监督框架，并就所需防护给出建议
- **边际风险条款**：如果能严格确认其他开发者发布了缺少可比防护的同级系统，OpenAI 可以调整防护要求，但须同时满足三个条件：评估认为不会实质增加总体风险；公开承认作了调整；防护仍须比对方更严，以免安全上的“逐底竞争”
- 2026-05-28 OpenAI 另发布针对加州和欧盟法律要求的 Frontier Governance Framework（二手）
- Preparedness 团队还与 SWE-bench 作者合作推出了 [[concepts/swe-bench|SWE-bench Verified]]

## 应用

- 新模型发布时的系统卡和风险报告依据；能力评测（含[[concepts/benchmark-contamination|饱和]]后的新基准）决定防护等级
- 作为满足 SB 53“前沿 AI 框架”和欧盟实践准则安全章的基础

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 安全与政策
- **关系**：企业自律 → 州法 / 欧盟规则把“公开框架”变成法定义务

## 相关概念

- [[concepts/california-sb-53|加州 SB 53]]
- [[concepts/eu-ai-act|欧盟《人工智能法》]]
- [[concepts/us-federal-ai-policy|美国联邦 AI 行政令]]
- [[concepts/claude-constitution|Claude 宪法]]
- [[concepts/swe-bench|SWE-bench]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/claude|Claude]]
- [[entities/gpt|GPT]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Critical capability thresholds mean capabilities that present a meaningful risk of a qualitatively new threat vector for severe harm with no ready precedent." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "in order to avoid a race to the bottom on safety, we keep our safeguards at a level more protective than the other AI developer, and share information to validate this claim." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "We believe that risk governance in this rapidly evolving domain should be proportional, iterative, and exportable." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "Our new RSP introduces a requirement to develop and publish a Frontier Safety Roadmap." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
- "Version 3.0 is a comprehensive rewrite of the RSP." — [[sources/ai-policy-survey-2026-11|AI 政策法规调研]]
