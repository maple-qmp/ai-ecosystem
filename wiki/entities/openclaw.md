---
title: OpenClaw
type: entity
tags: [project]
kind: app
layer: L4
aliases: ["OpenClaw", "Clawdbot", "Moltbot", "Warelay", "openclaw"]
org: "OpenClaw Foundation"
released: "2025-11"
competitors: ["[[entities/hermes-agent]]"]
depends_on: ["[[entities/pi-agent]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/agent-frameworks-comparison-survey-2026-11]]", "[[sources/ai-applications-survey-2026-11]]", "[[sources/inference-engines-survey-2026-11]]"]
---

# OpenClaw

## 描述

开源的常驻个人 AI 助理，MIT 协议，运行在用户自己的电脑上，通过 WhatsApp、Telegram、Slack、Discord、iMessage、Signal、Teams 等 20 多个聊天渠道交互。由 Peter Steinberger 开发，2025-11 以 Warelay 首发，先后叫 Clawdbot、Moltbot，2026-01 底改名 OpenClaw，随后成为 2026 年增长最快的开源项目之一。核心是本地 **Gateway**：管理会话、工具、事件和渠道连接的控制面，CLI、TUI 和 Control UI 都连到它；模型与 Agent harness 都是可替换插件（Claude、Codex、本地模型等），Agent 组件来自 [[entities/pi-agent|Pi]]。能力以 SKILL.md [[concepts/agent-skills|技能]]和插件扩展，经 ClawHub 分发；伴随 App 提供语音、Canvas、摄像头、屏幕等设备能力。2026-02 起由非营利的 OpenClaw Foundation 管理。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 常驻自主助理（兼具 L5 应用属性）
- **上游依赖**：[[entities/pi-agent|Pi]] 的 Agent 组件；Node.js；任意托管或本地模型
- **竞争 / 替代**：[[entities/hermes-agent|Hermes Agent]]
- **托管与集成**：[[entities/kimi-app|Kimi]] 的 Kimi Claw 一键部署常驻 OpenClaw；[[entities/ollama|Ollama]] 有 `ollama launch openclaw`
- 横向比较见 [[concepts/agent-framework-selection|AI Agent 框架选型]]

## 安全

- 主会话的工具默认在宿主机上运行，除非配置沙箱；DM 渠道默认对陌生发送者做配对验证
- 2026-01 底 Cisco AI 安全团队报告第三方技能在用户不知情时做数据外泄和提示注入
- 2.0 发布后 The Register 指出：没有网络与文件系统安全边界、Secret Store 不加密、沙箱默认不开启
- 2026-03 中国限制国企和政府机关在办公电脑上运行 OpenClaw，同时多地政府出台扶持相关产业的措施

## 时间线

- 2025-11-24 以 Warelay 首发；2025-12 改称 CLAWDIS；2026-01 初改称 Clawdbot
- 2026-01-27 因 [[entities/anthropic|Anthropic]] 商标投诉改名 Moltbot；同日面向 AI Agent 的社交网络 Moltbook 上线
- 2026-01-29 npm 包 `openclaw` 首发；约 2026-01-30 改名 OpenClaw
- 2026-02-14 Steinberger 宣布加入 [[entities/openai|OpenAI]]，项目移交 OpenClaw Foundation
- 2026-02 中旬 [[entities/moonshot-ai|月之暗面]]推出 Kimi Claw 公测
- 2026-03-02 GitHub 24.7 万星
- 2026-04-03 Anthropic 阻止 OpenClaw 使用 Claude 订阅（社区报告，未核实）
- 2026-05 [[entities/microsoft|Microsoft]] “Project Lobster” 测试基于 OpenClaw 的桌面环境 ClawPilot（报道）
- 2026-08-30 OpenClaw 2.0（v2026.8.1）：共享云会话、新 UI、更快安装
- 2026-11-05 v2026.11.1；GitHub 约 39.4 万星，npm 周下载约 260 万

## 相关实体

- [[entities/pi-agent|Pi]]
- [[entities/hermes-agent|Hermes Agent]]
- [[entities/kimi-app|Kimi]]
- [[entities/ollama|Ollama]]
- [[entities/openai|OpenAI]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-framework-selection|AI Agent 框架选型]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/agent-memory|Agent 记忆]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "OpenClaw is an open-source AI assistant that runs on your own computer and meets you in the channels you already use." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "OpenClaw was first published in November 2025 under the name Warelay." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]（Wikipedia）
- "Skills are stored as directories containing a SKILL.md file with metadata and instructions." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]（Wikipedia）
