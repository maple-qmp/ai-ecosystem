---
title: Turborepo
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Turborepo", "turbo"]
org: "[[entities/vercel]]"
released: "2021-12"
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

# Turborepo

## 描述

JavaScript / TypeScript monorepo 构建系统，用 Rust 编写，MIT 协议，2021-12 被 [[entities/vercel|Vercel]] 收购。它按任务图并行执行构建、测试、lint，并把任务输出按内容哈希缓存在本地或远程。本地缓存完全离线可用；远程缓存默认连 Vercel，但接口是公开规范。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 构建工具
- **上游依赖**：—
- **竞争 / 替代**：Nx、Bazel、moonrepo

## 脱离 Vercel 使用

- Remote Cache 有公开的 OpenAPI 规范（`/artifacts/{hash}` 的 GET / HEAD / PUT 等端点，Bearer token 认证）
- 用环境变量 `TURBO_API`、`TURBO_TOKEN`、`TURBO_TEAM` 指向自建服务器，社区实现如 ducktors/turborepo-remote-cache（可落到 S3、GCS、本地磁盘）
- 不配远程缓存时只用本地缓存，不发任何请求到 Vercel

## 时间线

- 2021-12 被 Vercel 收购并开源
- 2024 从 Go 完全迁移到 Rust（Turborepo 2.0）

## 相关实体

- [[entities/vercel|Vercel]]
- [[entities/nextjs|Next.js]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

