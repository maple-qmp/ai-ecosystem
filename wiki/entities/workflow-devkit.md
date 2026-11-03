---
title: Workflow DevKit
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Workflow DevKit", "WDK", "useworkflow"]
org: "[[entities/vercel]]"
released: "2025-10"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/vercel-oss-dependency-survey-2026-11]]"]
---

# Workflow DevKit

## 描述

[[entities/vercel|Vercel]] 开源的持久化工作流框架（npm 包 `workflow`），用 `"use workflow"` 和 `"use step"` 指令把普通 TypeScript 异步函数变成可暂停、可重试、崩溃后可恢复的工作流，适合长时间运行的 [[concepts/ai-agent|AI Agent]]。存储和队列抽象为可替换的“World”，因此运行时不绑定某一平台。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 框架
- **上游依赖**：—
- **竞争 / 替代**：Temporal、Inngest、Trigger.dev

## 脱离 Vercel 使用

- **Vercel World**：托管选项，部署到 Vercel 时自动使用
- **Postgres World**（`@workflow-worlds/postgres`）：自托管方案，PostgreSQL 存储加 pg-boss 队列；用 `WORKFLOW_TARGET_WORLD` 和 `DATABASE_URL` 两个环境变量选用；兼容性测试 E2E 304/312 通过
- **本地 World**：开发用
- **自定义 World**：实现 World 接口即可接其他存储
- 观测面板 `@workflow/web` 可直接读取 Postgres World，不需要 Vercel

## 时间线

- 2025-10 发布（beta）

## 相关实体

- [[entities/vercel|Vercel]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/nextjs|Next.js]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

