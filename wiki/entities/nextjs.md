---
title: Next.js
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["Next.js", "NextJS"]
org: "[[entities/vercel]]"
released: "2016-10"
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

# Next.js

## 描述

[[entities/vercel|Vercel]] 维护的 React 全栈框架，MIT 协议，支持服务端组件、流式渲染、ISR、Cache Components、Server Functions 和 Proxy（原 Middleware）。它是许多 AI 应用前端的默认选择，常与 [[entities/vercel-ai-sdk|AI SDK]] 搭配。框架可以脱离 Vercel 运行：`next start` 起 Node 服务、`output: 'standalone'` 打 Docker 镜像，或 `output: 'export'` 导出纯静态站点。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · Web 框架
- **上游依赖**：—（React、Turbopack）
- **竞争 / 替代**：Remix / React Router、Nuxt、SvelteKit、Astro

## 脱离 Vercel 部署

单实例 `next start` 加持久磁盘时，以下功能零配置可用：图片优化、Proxy、ISR、Cache Components、流式渲染、`after()`。

多实例或无状态容器部署要自己补：

- **共享缓存**：`cacheHandler`（ISR / 页面缓存）和 `cacheHandlers`（`'use cache'`）指向 Redis、S3 等共享存储，并实现 `refreshTags()` 让 `revalidateTag` 在所有实例生效
- **加密密钥**：所有实例设同一个 `NEXT_SERVER_ACTIONS_ENCRYPTION_KEY`
- **版本偏移**：配置 `deploymentId`，或使用不可变静态资源
- **流式**：nginx 等反向代理和负载均衡要关闭缓冲，否则 PPR 失去首字节优势
- **优雅退出**：发 `SIGTERM` 并留 10–30 秒排空，让 `after()` 回调执行完

部署到其他平台走 Adapter API：构建时输出带版本的应用描述，再由 adapter 转成平台格式。OpenNext 维护 AWS、Cloudflare、Netlify 的 adapter。

## 时间线

- 2016-10 首次发布
- 2023-05 Next.js 13.4，App Router 稳定
- 2025-10 Next.js 16，Adapter API 以 alpha 推出
- 2026-03 Next.js 16.2，Adapter API 稳定

## 相关实体

- [[entities/vercel|Vercel]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/turborepo|Turborepo]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Image Optimization through `next/image` works self-hosted with zero configuration when deploying using `next start`." — [[sources/vercel-oss-dependency-survey-2026-11|Vercel 开源框架服务依赖调研]]
- "By default, calling `revalidateTag()` on one instance only invalidates the cache on that instance." — [[sources/vercel-oss-dependency-survey-2026-11|Vercel 开源框架服务依赖调研]]
- "Cache Components works by default with Next.js and is not a CDN-only feature." — [[sources/vercel-oss-dependency-survey-2026-11|Vercel 开源框架服务依赖调研]]
