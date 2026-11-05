---
title: LM Studio
type: entity
tags: [product]
kind: app
layer: L3
aliases: ["LM Studio", "lms", "llmster", "Element Labs"]
released: "2023"
competitors: ["[[entities/ollama]]"]
depends_on: ["[[entities/llama-cpp]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]"]
---

# LM Studio

## 描述

在个人电脑上下载和运行开放模型的桌面应用，带图形界面，由纽约布鲁克林的 Element Labs 开发，Yagil Burowski 于 2023 年创办。它有两套推理引擎：[[concepts/gguf|GGUF]] 模型走定制的 [[entities/llama-cpp|llama.cpp]] 分支，MLX 模型走 Apple MLX（仅 Apple Silicon），两类模型可同时加载。应用内置本地 API 服务器，提供 OpenAI 兼容接口（`http://localhost:1234/v1`），2026 年起也提供 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点，可以把 [[entities/claude-code|Claude Code]] 指向本地模型。2025-07 起个人和工作使用都免费，另有付费的企业 / 团队版。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 本地部署工具
- **上游依赖**：[[entities/llama-cpp|llama.cpp]]（定制分支）、Apple MLX
- **竞争 / 替代**：[[entities/ollama|Ollama]]

## 主要组件

- **桌面应用**：模型搜索下载、对话界面、本地 API 服务器
- **`lms`**：命令行工具，基于 lmstudio.js，随 0.2.22 及以后版本附带；可查看状态、启动服务器、加载模型
- **`llmster`**：0.4 加入的无界面守护进程，用于服务器部署
- **SDK**：lmstudio.js、`lmstudio` Python 包

## 时间线

- 2023 Element Labs 成立，推出 LM Studio
- 2025-07-08 宣布个人和工作使用均免费，无需申请
- 2026 年初 0.4：加入 `llmster`（多数报道称 2026-01）
- 2026 年初 0.4.x：加入 Anthropic 兼容的 `/v1/messages` 端点（报道称 0.4.1 或 0.4.9，说法不一）

## 相关实体

- [[entities/llama-cpp|llama.cpp]]
- [[entities/ollama|Ollama]]
- [[entities/claude-code|Claude Code]]

## 相关概念

- [[concepts/gguf|GGUF]]
- [[concepts/quantization|量化]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "`lms` ships with LM Studio 0.2.22 and newer." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
