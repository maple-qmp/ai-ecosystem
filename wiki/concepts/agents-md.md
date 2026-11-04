---
title: AGENTS.md
type: concept
tags: [standard]
layer: L4
aliases: ["AGENTS.md", "AGENTS.override.md"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# AGENTS.md

## 定义

放在代码仓库里、写给编码 Agent 看的 Markdown 说明文件，相当于“给 Agent 的 README”：构建命令、测试方法、代码风格、注意事项。由 [[entities/openai|OpenAI]] 随 [[entities/codex-cli|Codex]] 推出并联合多家工具厂商推广，2025-12 捐给 Linux Foundation 新成立的 Agentic AI Foundation（AAIF），与 [[concepts/model-context-protocol|MCP]]、goose 一起成为该基金会的三个创始项目。

## 关键特征

- **纯约定，没有 schema**：就是普通 Markdown，没有必填字段，任何 Agent 都能读
- **分层叠加**（以 Codex 为例）：先读 Codex 主目录（默认 `~/.codex`）里的全局文件，再从仓库根目录一路走到当前目录，每层取 `AGENTS.override.md`、`AGENTS.md` 或配置的备用文件名中的第一个，越靠近当前目录的越后读、优先级越高
- **备用文件名**：Codex 可通过 `project_doc_fallback_filenames` 兼容其他工具的同类文件
- **采用面**：AAIF 公告称已有 6 万多个开源项目和 Agent 框架采用，包括 Amp、Codex、Cursor、Devin、Factory、Gemini CLI、GitHub Copilot、Jules、VS Code

## 应用

- 在仓库根目录写通用规则，在子目录写模块级覆盖
- 团队共用一份 Agent 指令，不必为每个工具各写一份
- 作为 [[concepts/agent-harness|Agent Harness]] 上下文的一部分自动加载

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 约定 / 标准
- **独立性**：完全独立，由 AAIF 治理，与 OpenAI 服务无关
- **同类**：Claude Code 的 CLAUDE.md、Cursor 的 rules 文件

## 相关概念

- [[concepts/agent-skills|Agent Skills]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 相关实体

- [[entities/codex-cli|Codex CLI]]
- [[entities/claude-code|Claude Code]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/langsmith|LangSmith]]（Context Hub 管理 AGENTS.md 版本）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Codex reads `AGENTS.md` files before doing any work." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
