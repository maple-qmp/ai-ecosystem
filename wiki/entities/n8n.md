---
title: n8n
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["n8n", "n8n.io", "n8n GmbH"]
org: "n8n GmbH"
released: "2019-04"
competitors: ["[[entities/dify]]", "[[entities/coze]]"]
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/lowcode-agent-platforms-survey-2026-11]]"]
---

# n8n

## 描述

柏林公司 n8n 的工作流自动化平台（GitHub 约 21 万星），Jan Oberhauser 2019 年创立，最初是 Zapier 一类集成自动化工具的可自托管替代，后来转型为构建 AI Agent 和工作流的平台。它把可视化画布和自定义代码（JavaScript、Python、npm 包）结合，可以自托管或用云服务；README 称有 1500 多个集成。协议是 fair-code 的 Sustainable Use License，允许自用和自托管，但限制把它作为商业服务转售，并非 OSI 意义的开源。2025-10 的 C 轮（1.8 亿美元，估值 25 亿美元）时，投资方称平台上超过 80% 的工作流嵌入了 AI Agent；n8n 自己的立场是在确定性流程里嵌入 Agent，并配合人工审批，而不是追求完全自主。2025-12 发布 2.0，重点是更安全的默认设置、可靠性和性能，并把工作流的“保存”和“发布”分开。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 低代码 Agent 平台
- **上游依赖**：—（Node.js 平台；接入 OpenAI、Anthropic、Google 及开源模型）
- **竞争 / 替代**：[[entities/dify|Dify]]、[[entities/coze|Coze / 扣子]]；Zapier、Make 等自动化 SaaS（本库无页面）

## 时间线

- 2019-04-24 npm 包 n8n 首次发布
- 2025-10-09 C 轮 1.8 亿美元，估值 25 亿美元，Accel 领投，累计融资 2.4 亿美元；当年用户增长 6 倍、收入增长 10 倍
- 2025-12-08 2.0.0 beta；2025-12-15 2.0 稳定版
- 2026-11-04 npm 最新版 2.46.6

## Contradictions

- 集成数量：README 写 1500+，仓库简介写 400+，口径不同。
- 2026-05 估值 52 亿美元仅见单一聚合站，未核实。

## 相关实体

- [[entities/dify|Dify]]
- [[entities/coze|Coze / 扣子]]
- [[entities/nvidia|NVIDIA]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Fair-code platform to build and deploy AI agents and workflows." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "Combine a visual canvas with custom code, run it self-hosted or in the cloud, and connect to 1500+ integrations." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
- "Pure autonomy creates magic when it works but proves too unpredictable for business-critical workflows." — [[sources/lowcode-agent-platforms-survey-2026-11|低代码 Agent 平台调研]]
