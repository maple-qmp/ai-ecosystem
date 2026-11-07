---
title: DeepSeek Harness
type: entity
tags: [project]
kind: framework
layer: L4
aliases: ["DeepSeek Harness", "dsh", "deepseek-harness", "@deepseek-ai/dsh"]
org: "[[entities/deepseek]]"
released: "2026-08"
competitors: ["[[entities/opencode]]", "[[entities/claude-code]]", "[[entities/pi-agent]]", "[[entities/codex-cli]]"]
depends_on: ["[[entities/deepseek-v]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/agent-frameworks-comparison-survey-2026-11]]", "[[sources/open-weight-flagships-survey-2026-11]]"]
---

# DeepSeek Harness

## 描述

[[entities/deepseek|DeepSeek]] 开源的 [[concepts/agent-harness|Agent harness]]（命令 `dsh`），MIT 协议，2026-08-13 发布，目前是开发者预览版，官方明确会有破坏性变更。架构口号是“一切皆插件”：基于插件框架 Cordis，模型适配器、工具注册表、会话日志乃至 Agent 循环本身都是插件，按 profile 组合；会话存储（JSONL、SQLite）、执行环境（本地、E2B 沙箱）、shell、子 Agent 提供方都可替换。提供 Web UI（`npx @deepseek-ai/dsh web`，默认 `127.0.0.1:3080`）、无界面单任务模式（适合 CI）以及 macOS、Windows 桌面版，可在聊天中用 Creator 模式编写插件。默认使用 DeepSeek 模型，也可配置 Anthropic、OpenAI、Bedrock、Azure 及任意 OpenAI 兼容端点；能把任务委派给 [[entities/claude-code|Claude Code]]、[[entities/codex-cli|Codex]] 或 ACP Agent，并复用它们的 hooks 配置与 AGENTS.md、CLAUDE.md。

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · harness / 编码 Agent
- **上游依赖**：默认 [[entities/deepseek-v|DeepSeek-V]] 系列模型；Node.js
- **竞争 / 替代**：[[entities/opencode|OpenCode]]、[[entities/claude-code|Claude Code]]、[[entities/pi-agent|Pi]]、[[entities/codex-cli|Codex CLI]]
- **集成**：[[entities/ollama|Ollama]] 的 `ollama launch` 支持 DeepSeek Harness
- 横向比较见 [[concepts/agent-framework-selection|AI Agent 框架选型]]

## 关键特性

- **模式**：Standard（完整编码 Agent）、Minimal（持久 bash + 文本替换编辑器）、Creator（运行时自省、编写预设）、PTC（Code Mode：模型写一段 TypeScript 程序代替逐个工具调用）
- **官方插件**：Agent teams、自动审批审查员、定时任务、语音输入、终端、Agent loop、子 Agent（部分为实验性）；社区插件用 GitHub topic `dsh-plugin`
- **沙箱**：只读 / 工作区写 / 完全访问三档。第三方评测发现“工作区写”只限制写入、不限制读取，FAQ 称沙箱不覆盖网络和进程
- **其他限制**：发布前一周撤下自带 TUI，终端界面只能靠树外插件；委派给其他 Agent 时不继承父上下文；暂不接受外部 PR
- **同名项目**：PyPI 上的 `deepseek-harness` 是第三方的 DeepSeek API 客户端，不是本项目

## 时间线

- 2026-08-10 npm 包 `@deepseek-ai/dsh` 首发
- 2026-08-13 仓库公开，开发者预览（v0.1）
- 2026-09-09 DeepInfra 评测 0.1.1-rc.2，称其“与其说是产品，不如说是底盘”，日常使用更推荐 OpenCode
- 2026-11-04 0.2.2-rc.1；npm 周下载约 84 万，GitHub 约 27.6 万星（发布不到三个月，星数仅供参考）

## 相关实体

- [[entities/deepseek|DeepSeek]]
- [[entities/deepseek-v|DeepSeek-V]]
- [[entities/opencode|OpenCode]]
- [[entities/claude-code|Claude Code]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/pi-agent|Pi]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/agent-framework-selection|AI Agent 框架选型]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agents-md|AGENTS.md]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "DeepSeek Harness (`dsh`) is an open-source agent harness developed by DeepSeek AI." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "It is built on an everything-is-a-plugin architecture and powered by Cordis." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
- "DeepSeek Harness is in developer preview and iterating rapidly." — [[sources/agent-frameworks-comparison-survey-2026-11|Agent 框架横向对比调研]]
