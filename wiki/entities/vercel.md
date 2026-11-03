---
title: Vercel
type: entity
tags: [organization]
kind: company
layer: X
aliases: ["Vercel", "Vercel Inc."]
released: "2015"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: claude-seed
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/vercel-oss-dependency-survey-2026-11]]"]
---

# Vercel

## 描述

美国前端云平台公司，前身为 ZEIT（2015 年由 Guillermo Rauch 创立，2020 年更名）。商业模式是“开源框架 + 托管平台”：维护 [[entities/nextjs|Next.js]]、[[entities/vercel-ai-sdk|AI SDK]]、[[entities/turborepo|Turborepo]]、[[entities/workflow-devkit|Workflow DevKit]] 等开源框架，同时出售托管、AI Gateway、Remote Cache、Blob、Sandbox 等服务，以及 v0 应用生成器。框架代码大多不绑定平台，绑定主要体现在默认配置上。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 公司；开源框架见 [[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- **上游依赖**：—
- **竞争 / 替代**：Netlify、Cloudflare、AWS Amplify（托管平台层面）

## 开源模块对 Vercel 服务的依赖

依据 [[sources/vercel-oss-dependency-survey-2026-11|Vercel 开源框架服务依赖调研]]，分四级。

### 1. 完全独立（不调用任何 Vercel 服务）

- SWR：React 数据请求 hooks，纯客户端库
- Satori：HTML/CSS 转 SVG，`@vercel/og` 的底层
- `@vercel/ncc`：把 Node 项目编译成单文件
- `@vercel/nft`：Node 文件依赖追踪，Next.js standalone 输出依赖它
- `serve`、`ms`：静态文件服务器、时间字符串工具
- Geist：字体与设计系统
- Streamdown、AI Elements：面向 AI 流式输出的 Markdown 渲染和 React 组件（基于 shadcn/ui）
- Chat SDK（`chat`）：一套代码对接 Slack、Teams、Discord 等的聊天机器人框架，MIT
- agent-browser：面向 AI Agent 的浏览器自动化 CLI，Apache-2.0

### 2. 默认连 Vercel，改配置即可脱离

- [[entities/vercel-ai-sdk|AI SDK]]：模型字符串默认走 AI Gateway
- [[entities/turborepo|Turborepo]]：远程缓存默认连 Vercel
- [[entities/workflow-devkit|Workflow DevKit]]：托管 World 在 Vercel，可换 Postgres World
- Flags SDK（`flags`）：可接 LaunchDarkly、Statsig 等 provider；Flags Explorer 属 Vercel 工具栏
- `mcp-handler`（原 `@vercel/mcp-adapter`）：在 Next.js 等框架里挂 [[concepts/model-context-protocol|MCP]] 服务器，SSE 续传需自备 Redis

### 3. 自托管可用，多实例要自己补组件

- [[entities/nextjs|Next.js]]：见其页面的“脱离 Vercel 部署”一节

### 4. Vercel 服务的客户端（离开 Vercel 无意义）

- `@vercel/analytics`、`@vercel/speed-insights`、`@vercel/blob`、`@vercel/edge-config`
- `@vercel/functions`（`waitUntil` 等）、`@vercel/oidc`、`@vercel/sandbox`
- `@ai-sdk/gateway`、Vercel CLI、v0
- `@vercel/kv`、`@vercel/postgres` 已停用，分别迁往 Upstash、Neon

## 时间线

- 2015 以 ZEIT 名义创立
- 2016-10 发布 Next.js
- 2020-04 更名 Vercel
- 2021-12 收购 Turborepo
- 2023-06 发布 AI SDK
- 2025-07 收购 NuxtLabs，Nuxt 与 Nitro 仍保持 MIT 和平台中立
- 2025-10 发布 Workflow DevKit；Next.js 16 推出 Adapter API（alpha）
- 2026-03 Next.js 16.2，Adapter API 稳定

## 相关实体

- [[entities/nextjs|Next.js]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/turborepo|Turborepo]]
- [[entities/workflow-devkit|Workflow DevKit]]
- [[entities/langchain|LangChain]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

