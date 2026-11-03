---
title: Vercel 开源框架的服务依赖调研（2026-11）
type: source
tags: [notes]
source_note: "[[Vercel开源框架服务依赖调研-2026-11]]"
url: https://nextjs.org/docs/app/guides/self-hosting
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[entities/vercel]]"
  - "[[entities/nextjs]]"
  - "[[entities/vercel-ai-sdk]]"
  - "[[entities/workflow-devkit]]"
  - "[[entities/turborepo]]"
---

# Vercel 开源框架的服务依赖调研（2026-11）

## Summary

调研 [[entities/vercel|Vercel]] 维护的开源代码框架，逐个判断能否脱离 Vercel 平台使用。结论：绝大多数框架代码本身不绑定 Vercel，绑定发生在“默认值”上。[[entities/vercel-ai-sdk|AI SDK]] 的模型字符串默认走 AI Gateway，[[entities/turborepo|Turborepo]] 的远程缓存默认连 Vercel，[[entities/workflow-devkit|Workflow DevKit]] 的托管 World 在 Vercel 上。三者都能通过配置换成自建或第三方实现。[[entities/nextjs|Next.js]] 单实例 `next start` 基本零配置可用，多实例部署要自己补共享缓存、加密密钥和 deploymentId；Adapter API 已在 16.2 稳定。真正离不开 Vercel 的只有 `@vercel/*` 下那批服务客户端（Analytics、Blob、Edge Config 等）。

## Key Points

- **完全独立**：SWR、Satori、`@vercel/ncc`、`@vercel/nft`、`serve`、`ms`、Geist、Streamdown、AI Elements、Chat SDK、agent-browser
- **默认连 Vercel、可改配置**：AI SDK（`AI_SDK_DEFAULT_PROVIDER` 或直接传 provider 实例）、Turborepo（`TURBO_API` 指向自建缓存）、Workflow DevKit（Postgres World）、Flags SDK、`mcp-handler`
- **自托管需补组件**：Next.js 多实例要共享 `cacheHandler` / `cacheHandlers`、`NEXT_SERVER_ACTIONS_ENCRYPTION_KEY`、`deploymentId`、不缓冲的反向代理
- **Vercel 服务客户端**：`@vercel/analytics`、`@vercel/speed-insights`、`@vercel/blob`、`@vercel/edge-config`、`@vercel/functions`、`@vercel/oidc`、`@vercel/sandbox`、`@ai-sdk/gateway`；`@vercel/kv`、`@vercel/postgres` 已停用
- **Next.js Adapter API**：16 版 alpha（2025-10），16.2 稳定（2026-03）；OpenNext 的 AWS / Cloudflare / Netlify adapter 预计 2026 年底前发布

## Mentioned Pages

- [[entities/vercel|Vercel]]
- [[entities/nextjs|Next.js]]
- [[entities/vercel-ai-sdk|AI SDK]]
- [[entities/workflow-devkit|Workflow DevKit]]
- [[entities/turborepo|Turborepo]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
