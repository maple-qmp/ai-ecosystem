---
title: MCP 扩展
type: concept
tags: [standard]
layer: L4
aliases: ["MCP Extensions", "MCP Apps", "MCP Tasks", "Skills over MCP"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources:
  - "[[sources/mcp-spec-2026-07-28]]"
---

# MCP 扩展

## 定义

[[concepts/model-context-protocol|MCP]] 核心协议之外的可选能力。2026-07-28 版在 `ClientCapabilities` / `ServerCapabilities` 中正式加入 `extensions` 字段：客户端在每个请求的能力里声明扩展，服务端在 `server/discover` 中声明。扩展标识格式为 `{厂商前缀}/{扩展名}`，官方扩展使用 `io.modelcontextprotocol/` 前缀，第三方用自己拥有的反向域名（如 `com.example/`）。

## 关键特征

- **生命周期**：Experimental → Beta → Stable，或从 Beta 晋升进核心规范。标识符不随阶段变化
- **官方仓库**：放在 GitHub `modelcontextprotocol` 组织下以 `ext-` 开头的仓库

## 官方扩展一览（截至 2026-11）

| 扩展 | 仓库 | 阶段 | 用途 |
|---|---|---|---|
| OAuth Client Credentials | `ext-auth` | Stable | 机器对机器认证 |
| Enterprise-Managed Authorization | `ext-auth` | Stable | 企业统一访问控制 |
| MCP Apps | `ext-apps` | Stable | 服务器在对话中内嵌交互式 UI（图表、表单、播放器） |
| MCP Tasks | `ext-tasks` | Beta，目标进入核心 | 长任务：任务句柄、轮询、中途补充输入、可恢复 |
| Skills over MCP | `ext-skills` | Beta | 通过 MCP 资源发现并读取 Agent Skills |

## Tasks 要点

- 双方声明 `io.modelcontextprotocol/tasks` 后，服务端可以对任意受支持的请求返回 `resultType: "task"`（含 `taskId`、TTL、建议轮询间隔），不需要客户端逐个请求开启
- `tasks/get` 轮询，`tasks/update` 提交中途输入，`tasks/cancel` 协作式取消；不再有 `tasks/result` 和 `tasks/list`
- 状态：`working`、`input_required`、`completed`、`failed`、`cancelled`
- 流程图见 [[concepts/mcp-request-flow|MCP 请求流程]]的阶段 6

## 应用

- CI、批处理、审批流这类长操作（Tasks）
- 在对话里渲染交互式界面（Apps）
- 把技能包作为 MCP 资源分发（Skills）
- 企业 SSO 与服务账号接入（ext-auth）

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]]
- [[concepts/multi-round-trip-requests|多轮往返请求（MRTR）]]
- [[concepts/ai-agent|AI Agent]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]

## 我的判断

## 来源摘录
