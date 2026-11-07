---
title: ChatKit
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["ChatKit", "OpenAI ChatKit", "chatkit-js", "chatkit-python"]
org: "[[entities/openai]]"
released: "2025-10"
competitors: ["[[entities/vercel-ai-sdk]]"]
depends_on: ["[[entities/openai-agents-sdk]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-07
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# ChatKit

## 描述

[[entities/openai|OpenAI]] 在 2025-10 DevDay 推出的嵌入式聊天界面套件，用来把 Agent 对话界面放进自己的网站。分前后端两部分：前端 `chatkit-js`（Web Component 与 React 绑定，Apache-2.0），后端 `chatkit-python`（服务端 SDK，负责存储、权限、工具和后端函数，Apache-2.0，1.6.5 版依赖 `openai` 与 [[entities/openai-agents-sdk|Agents SDK]]）。界面内置流式输出、线程管理、附件、工具调用过程展示和可交互的小部件（widget）。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · UI 框架
- **上游依赖**：[[entities/openai-agents-sdk|OpenAI Agents SDK]]（自托管后端）
- **竞争 / 替代**：[[entities/vercel-ai-sdk|AI SDK]] UI 与 AI Elements、assistant-ui、CopilotKit

## 脱离 OpenAI 使用

只能部分脱离。

- **托管路径**（不可脱离）：在 Agent Builder 里建工作流，后端调 OpenAI 的 ChatKit sessions 接口换客户端密钥。Agent Builder 计划 2026-11-30 关闭，这条路径只留给存量用户过渡
- **自托管路径**（后端可脱离）：用 chatkit-python 在自己的服务器上实现后端，可以 "connect to any agentic service"，新项目官方推荐这条。模型由后端决定，社区有接 [[entities/litellm|LiteLLM]]、Gemini 的例子（非官方）
- **仍然连 OpenAI 的部分**：官方示例从 `cdn.platform.openai.com` 加载 `chatkit.js`；前端用 `api: { url, domainKey }` 指向自家后端，`domainKey` 是否必须在 OpenAI 后台登记，官方页面未写明

## 时间线

- 2025-10 DevDay 发布，与 Agent Builder 一起推出
- 2026-05 chatkit-python v1.6.5
- 2026-11-30 Agent Builder 计划关闭，托管路径随之结束

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/vercel-ai-sdk|AI SDK]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "connect to any agentic service, including one built with the Agents SDK" — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
- "scheduled to shut down on November 30, 2026" — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]（Agent Builder）
