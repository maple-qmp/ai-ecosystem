---
title: Ollama
type: entity
tags: [product]
kind: app
layer: L3
aliases: ["Ollama", "Ollama Cloud", "ollama/ollama"]
released: ""
competitors: ["[[entities/lm-studio]]"]
depends_on: ["[[entities/llama-cpp]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/inference-engines-survey-2026-11]]", "[[sources/claude-independent-modules-survey-2026-11]]"]
---

# Ollama

## 描述

在本地或云端运行开放模型的工具，一条命令拉取并运行模型，同时提供 REST API 与 OpenAI、Anthropic 兼容接口，是开发者本地跑开放模型最常用的入口。主要用 Go 编写，早期通过 CGo 调用 [[entities/llama-cpp|llama.cpp]] 推理，2025 年中开始转向自研引擎（有评论认为因此重新引入了 llama.cpp 已修过的问题）。2026 年从本地工具扩展为平台：`ollama launch` 一键把本地或云端模型接到 [[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex]]、Copilot CLI、OpenCode 等编程 Agent；Ollama Cloud 提供带 `:cloud` 后缀的云端模型，后来改为按 token 计费；本地软件仍免费、MIT 协议。公司由 Jeffrey Morgan 和 Michael Chiang 创办（YC W21），2026-07 完成 6500 万美元 B 轮，称有约 890 万开发者使用。

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 本地部署工具
- **上游依赖**：[[entities/llama-cpp|llama.cpp]]（早期推理后端）、[[concepts/gguf|GGUF]] 模型格式；开放权重模型如 [[entities/llama|Llama]]、[[entities/qwen|Qwen]]、[[entities/gpt-oss|gpt-oss]]
- **下游**：[[entities/claude-code|Claude Code]] 等编程 Agent 通过 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点接入；官方 Python / JS 库
- **竞争 / 替代**：[[entities/lm-studio|LM Studio]]；直接用 [[entities/llama-cpp|llama.cpp]] 的 `llama serve`

## 接口

- **本地**：`http://localhost:11434`，原生 REST API、OpenAI 兼容、Anthropic Messages API 子集（不支持 token 计数、`tool_choice`、提示缓存等）
- **云端**：`OLLAMA_API_KEY` + `https://ollama.com/api/chat` 或 `https://ollama.com/v1/messages`，不需要安装 Ollama
- **集成**：`ollama launch claude`、`ollama launch codex`、`ollama launch openclaw` 等

## 时间线

- 2021 Y Combinator 冬季批次（公司页信息；多家报道称产品 2023 年推出）
- 2024-01-12 官方 Python SDK 首个版本
- 2025 年中 开始从 llama.cpp 转向自研推理引擎
- 2026-01 v0.14.0 加入 Anthropic 兼容接口，推出 `ollama launch`
- 2026-07-09 B 轮 6500 万美元，Theory Ventures 领投，Benchmark、8VC、Y Combinator 等参投；累计融资 8800 万美元；未披露估值
- 2026-08-31 云端模型改为按 token 计费的套餐

## 相关实体

- [[entities/llama-cpp|llama.cpp]]
- [[entities/lm-studio|LM Studio]]
- [[entities/claude-code|Claude Code]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/gpt-oss|gpt-oss]]

## 相关概念

- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/gguf|GGUF]]
- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Start building with open models. Access the latest releases locally or in the cloud with complete privacy." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Connect Anthropic clients and tools such as Claude Code to Ollama. Ollama supports a subset of the Anthropic Messages API." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
- "Run models in Ollama's cloud from your apps or terminal. No model or app download required." — [[sources/inference-engines-survey-2026-11|推理引擎与本地部署调研]]
