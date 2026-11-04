---
title: Mastra Platform
type: entity
tags: [product]
kind: infra
layer: L4
aliases: ["Mastra Platform", "Mastra Cloud", "Mastra Observability"]
org: "[[entities/mastra-inc]]"
released: "2026-04"
competitors: ["[[entities/langsmith]]", "[[entities/vercel]]"]
depends_on: ["[[entities/mastra]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/mastra-ecosystem-survey-2026-11]]"]
---

# Mastra Platform

## 描述

[[entities/mastra-inc|Mastra 公司]]的闭源托管平台，给用 [[entities/mastra|Mastra]] 框架写的 Agent 提供部署、环境管理、可观测性、告警、数据库、workspaces 和托管版 Studio。2026-04 与 A 轮融资同周推出，部分文档和导出器名称中沿用旧称 Mastra Cloud。服务器默认以 serverless 方式运行，可加购常驻（Always-On）。计费上所有费用（包括模型 token 花费）都走同一个积分池，按观测事件、CPU 小时和出口流量计量。企业版也可部署在客户自己的基础设施上。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 平台（部署与可观测性）
- **上游依赖**：[[entities/mastra|Mastra]] 框架
- **竞争 / 替代**：[[entities/langsmith|LangSmith]]（观测、评测、部署）、Langfuse、Braintrust；托管运行时方向有 [[entities/vercel|Vercel]]

## 套餐（2026-07 说明）

- **Starter**：免费、按量付费；每月含 10 万观测事件、24 CPU 小时、10GB 出口流量；数据保留 15 天；项目与部署不限
- **Team**：250 美元 / 月；含 100 万事件、250 CPU 小时、100GB；保留 6 个月；多团队、SSO、SOC 2 文档；超量单价更低
- **Server Always-On**：每项目 100 美元，保持服务器常驻
- **Enterprise**：定制价格；RBAC、审计日志、SLA

## 时间线

- 2026-04 与 2200 万美元 A 轮同周推出
- 2026-05-13 观测计费维持上线时标准（Starter 每月 10 万事件，超出每 10 万 10 美元）
- 2026-07-17 发布计费说明，所有费用改走统一积分池
- 2026-10 密集上线观测功能：Thread View（10-12）、Metrics API（10-13）、Trace Imports（10-14）、Trace Queries（10-15）、Studio 级 SSO（10-19）、Span Queries（10-28）
- 2026-10-21 平台事故，次日发布事故报告

## 相关实体

- [[entities/mastra|Mastra]]
- [[entities/mastra-inc|Mastra 公司]]
- [[entities/langsmith|LangSmith]]
- [[entities/vercel|Vercel]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Everything runs on a single pool of credits, including model and token spend, so everything lives in the same place." — [[sources/mastra-ecosystem-survey-2026-11|Mastra 生态深度调研]]
