---
title: Agent Skills
type: concept
tags: [standard]
layer: L4
aliases: ["Agent Skills", "技能", "SKILL.md", "agentskills.io"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-05
sources: ["[[sources/openai-developers-survey-2026-11]]", "[[sources/claude-independent-modules-survey-2026-11]]"]
---

# Agent Skills

## 定义

一种给 [[concepts/ai-agent|AI Agent]] 打包能力的开放格式：一个技能就是一个文件夹，里面有说明文件 `SKILL.md`（frontmatter 写名称和描述，正文写操作步骤），加上可选的脚本、模板和参考资料。Agent 平时只看名称和描述，判断任务相关时才读全文，节省上下文。规范发布在 agentskills.io，由 [[entities/anthropic|Anthropic]] 发起，[[entities/openai|OpenAI]] 的 [[entities/codex-cli|Codex]] 和 ChatGPT 也按这个标准实现。

## 关键特征

- **按需加载（渐进披露）**：分三步——Discovery（启动时只加载各技能的名称和描述）、Activation（任务匹配时读入完整 `SKILL.md`）、Execution（按说明执行，必要时运行附带脚本或读取引用文件）
- **目录约定**：`SKILL.md` 必需，可选 `scripts/`、`references/`、`assets/`
- **可带代码**：脚本放在技能目录里，由 Agent 在本机或沙箱执行
- **写一次、多处用**：同一个技能目录可在 Claude Code、Codex、ChatGPT 等支持该标准的工具里使用
- **分发**：Codex 里可用 `$skill-installer` 安装；OpenAI 的 `openai/skills` 目录仓库已弃用，示例改放 `openai/plugins`，以“插件”（技能 + MCP 服务器 + 可选 UI）形式分发
- **Anthropic 的 skills 仓库**（`anthropics/skills`，约 18.7 万星）：多数示例技能是 Apache-2.0；驱动 Claude 文档能力的 docx / pdf / pptx / xlsx 四个技能是 source-available，协议限定按与 Anthropic 的服务协议使用，不能当开源代码拿去别处用。仓库还可作为 [[entities/claude-code|Claude Code]] 插件市场添加
- **治理**：规范仓库 `agentskills/agentskills`（Apache-2.0）；agentskills.io 称格式由 Anthropic 发起、作为开放标准发布、接受社区贡献，截至 2026-11 未见捐给 AAIF 的一手证据
- **MCP 通道**：MCP 的 Skills over MCP 扩展（Beta）让服务器以资源形式提供技能，见 [[concepts/mcp-extensions|MCP 扩展]]

## 应用

- 把团队的固定流程（发版、写周报、代码审查清单）写成技能
- 给 Agent 补领域知识和工具脚本，不必改 Agent 本身
- Java 生态中 [[entities/spring-ai-alibaba|Spring AI Alibaba]]、Spring AI 社区扩展也已支持

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 开放标准
- **独立性**：格式完全独立；ChatGPT 工作区技能、插件目录等分发渠道属于 OpenAI 服务

## 相关概念

- [[concepts/agents-md|AGENTS.md]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/mcp-extensions|MCP 扩展]]
- [[concepts/mcp-bundles|MCP Bundles（MCPB）]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]

## 相关实体

- [[entities/codex-cli|Codex CLI]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/anthropic|Anthropic]]
- [[entities/openai|OpenAI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Agent Skills are folders of instructions, scripts, and resources that AI agents can discover and use to perform at specific tasks." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]（openai/skills README）
- "The Agent Skills format was originally developed by Anthropic, released as an open standard, and has been adopted by a growing number of agent products." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（agentskills.io）
