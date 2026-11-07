---
title: AI Agent 框架横向对比调研（2026-11）
captured: 2026-11-07
tags: [notes]
---

# AI Agent 框架横向对比调研（2026-11）

一句话：横向比较 8 个主流 Agent 框架 / harness：Claude Agent SDK、OpenAI Agents SDK、Deep Agents、Pi、OpenCode、OpenClaw、Hermes Agent、DeepSeek Harness，维度为设计理念、核心架构、功能特性、适用场景、上手难度、社区生态与维护活跃度。资料来自官方仓库 README、官方文档与官网、npm / PyPI 元数据（2026-11-07 读取）、Wikipedia 以及第三方评测。本会话 GitHub API 不可用，星数取自 GitHub 网页（2026-11-07 抓取），只作量级参考。

## 原始链接

- Claude Agent SDK：https://github.com/anthropics/claude-agent-sdk-python ；https://docs.anthropic.com/en/docs/claude-code/sdk
- OpenAI Agents SDK：https://github.com/openai/openai-agents-python ；https://github.com/openai/openai-agents-js
- Deep Agents：https://github.com/langchain-ai/deepagents ；https://github.com/langchain-ai/deepagentsjs ；https://docs.langchain.com/oss/python/deepagents/overview
- Pi：https://github.com/earendil-works/pi ；https://pi.dev
- Pi 二手综述：https://www.eesel.ai/blog/pi-coding-agent ；https://composio.dev/blog/pi-agent-vs-claude-code
- OpenCode：https://github.com/anomalyco/opencode ；https://opencode.ai/docs/ ；https://docs.opencode.ai/docs/server/ ；https://opencode.ai/docs/agents/
- OpenCode 二手综述：https://rywalker.com/research/opencode ；https://www.shareuhack.com/en/posts/opencode-anthropic-legal-controversy-2026
- OpenClaw：https://github.com/openclaw/openclaw ；https://en.wikipedia.org/wiki/OpenClaw ；https://www.neowin.net/news/openclaws-founder-peter-steinberger-is-joining-openai/
- Hermes Agent：https://github.com/NousResearch/hermes-agent ；https://hermes-agent.nousresearch.com/docs/ ；https://hermesatlas.com/reports/state-of-hermes-april-2026 （社区报告，非官方）
- DeepSeek Harness：https://github.com/deepseek-ai/deepseek-harness ；https://www.deepseek.com/en/harness/ ；https://deepinfra.com/blog/deepseek-harness-review ；https://thenewstack.io/deepseek-harness-open-source-plugins/
- npm 元数据：https://registry.npmjs.org/<包名> ；周下载量：https://api.npmjs.org/downloads/point/last-week/<包名> （2026-11-07 读取，统计区间 2026-10-31 至 2026-11-06）
- PyPI 元数据：https://pypi.org/pypi/<包名>/json ；下载量：https://pypistats.org/api/packages/<包名>/recent

## 包与仓库元数据（2026-11-07 读取）

| 框架 | 主包 | 最新版本 | 首发 | 协议 | 周下载量 | GitHub 星数（网页） |
|---|---|---|---|---|---|---|
| Claude Agent SDK | npm `@anthropic-ai/claude-agent-sdk` / PyPI `claude-agent-sdk` | 0.3.319（2026-11-06）/ 0.2.179（2026-11-06） | npm 2025-09-27；PyPI 2025-09-28（改名前的 Claude Code SDK 更早） | TS 版：见 README（Anthropic 商业条款）；Python 版 MIT | npm 1848 万；PyPI 870 万 | 未抓取 |
| OpenAI Agents SDK | PyPI `openai-agents` / npm `@openai/agents` | 0.24.0（2026-10-15）/ 0.21.0（2026-10-20） | PyPI 2025-03-04；npm 2025-06-03 | MIT | PyPI 483 万；npm 245 万 | 未抓取 |
| Deep Agents | PyPI `deepagents` / npm `deepagents` | 0.7.34（2026-11-05）/ 1.16.3（2026-11-06） | PyPI 2025-07-29；npm 2025-08-03 | MIT | PyPI 203 万；npm 67 万 | 未抓取 |
| Pi | npm `@earendil-works/pi-coding-agent`（旧包 `@mariozechner/pi-coding-agent`） | 1.5.0（2026-11-02） | 旧包 2025-11-12；新包 2026-05-07 | MIT | 新包 606 万；旧包 36 万 | 约 12.1 万 |
| OpenCode | npm `opencode-ai`；SDK `@opencode-ai/sdk` | 1.19.5（2026-10-28） | 2025-05-31 | MIT | CLI 360 万；SDK 3657 万 | 约 22.5 万 |
| OpenClaw | npm `openclaw` | 2026.11.1（2026-11-05） | 2026-01-29 | MIT | 260 万 | 约 39.4 万 |
| Hermes Agent | 官方用安装脚本；PyPI `hermes-agent`（0.19.0，无项目链接，归属未核实）；npm `hermes-agent` 为非官方桥接 | npm 桥接标注 0.23.0（2026-11-06） | 2026-02-25（GitHub） | MIT | PyPI 8.7 万 | 约 26.1 万 |
| DeepSeek Harness | npm `@deepseek-ai/dsh` | 0.2.2-rc.1（2026-11-04） | 2026-08-10（npm）；仓库 2026-08-13 | MIT | 84 万 | 约 27.6 万 |

版本节奏（npm 各次级版本的首个正式版日期）：

- Pi（`@earendil-works/pi-coding-agent`）：0.74.0 2026-05-07 → 0.87.0 2026-09-21 → 0.99.0 2026-09-29 → 1.0.0 2026-10-01 → 1.5.0 2026-11-02
- OpenCode（`opencode-ai`）：0.1.0 2025-06-12 → 1.0.0 2025-10-31 → 1.14 2026-04 → 1.19.0 2026-10-11
- OpenClaw（`openclaw`）：日历版本号，2026.1.29 → 2026.8.1（2026-08-31，即 2.0）→ 2026.11.1（2026-11-05）
- OpenAI Agents SDK（`@openai/agents`）：0.1.0 2025-08-28 → 0.21.0 2026-10-20
- Deep Agents（npm `deepagents`）：1.1.0 2025-11-05 → 1.16.0 2026-10-26

其他发现：

- PyPI `deepagents-cli` 0.3.0（2026-08-24）已标为 DEPRECATED，提示改用 Managed Deep Agents（`managed-deepagents`，命令 `mda`）
- PyPI 上的 `deepseek-harness`（0.3.1）是第三方项目（HenryZ838978，“Protocol-aware client for DeepSeek V4-Pro / V4-Flash / Vision”），不是官方 DeepSeek Harness；npm `deepseek-harness` 0.0.1 是占位包

## 官方原文摘录

Claude Agent SDK（已在 `raw/Claude独立可用模块调研-2026-11.md` 收录，此处不重复）。

OpenAI Agents SDK（已在 `raw/OpenAI-Developers独立可用模块调研-2026-11.md` 收录）。

Deep Agents：

- PyPI summary："Production-ready, extensible agent harness with a built-in filesystem and context management, sub-agent delegation, skills, and long-term memory."
- npm description："Deep Agents - a library for building controllable AI agents with LangGraph"

Pi：

- README："Pi is a minimal, extensible agent harness that you can make your own."
- pi.dev："Pi is a minimal agent harness. Adapt Pi to your workflows, not the other way around."
- pi.dev："Extensions are TypeScript modules with access to tools, commands, keyboard shortcuts, events, and the full TUI."
- pi.dev："RPC: JSON protocol over stdin/stdout for non-Node integrations."
- npm description："Coding agent CLI with read, bash, edit, write tools and session management"
- Mario Zechner 设计文章（转引自 eesel）："There does not appear to be a need for 10,000 tokens of system prompt"
- Armin Ronacher RFC 0015（转引自 eesel）："Pi remains MIT licensed and that will not change."
- 包结构（README）：`pi-ai`（多厂商统一 LLM API）、`pi-agent-core`（工具调用与状态管理的 Agent 运行时）、`pi-coding-agent`（交互式编码 Agent CLI）、`pi-tui`（差分渲染的终端 UI 库）、`pi-durable`（对话、任务、文档的持久运行时）、`pi-telemetry`、`chord`
- pi.dev 列出“不内置、靠扩展实现”的功能：子 Agent（用 tmux 跑多个 Pi 实例或写扩展）、权限弹窗（用容器或自己写确认流程）、计划模式（写到文件或做成扩展）、待办（TODO.md）、后台 bash（tmux）。MCP 现已内置（Codemode）

OpenCode：

- README："The open source AI coding agent."
- 文档："It's available as a terminal-based interface, desktop app, or web app."
- 服务端文档："The `opencode serve` command runs a headless HTTP server that exposes an OpenAPI endpoint that an opencode client can use."
- 服务端文档："When you run `opencode` it starts a TUI and a server. Where the TUI is the client that talks to the server."
- Agents 文档：内置 build（"Default coding agent."）、plan（"Explores and plans without editing normal project files."）、general、explore；权限规则 "`permissions` is an ordered list of matching rules."，取值 allow / ask / deny，"The last matching rule wins"

OpenClaw：

- README："OpenClaw is an open-source AI assistant that runs on your own computer and meets you in the channels you already use."
- README：Gateway 是 "the local control plane for sessions, tools, events, and channel connections."
- README：模型与 Agent harness 都是可替换的插件（举例 Claude、Codex、本地模型）；致谢中提到 Mario Zechner 与 pi
- README：项目由非营利的 OpenClaw Foundation 开发，基金会雇用核心团队并签署发布；捐助方（含 Amazon、OpenAI、Red Hat 等）不拥有也不指导项目
- README：DM 渠道默认对陌生发送者做配对（`openclaw pairing approve <channel> <code>`）；主会话的工具默认在宿主机上运行，除非配置沙箱
- Wikipedia："OpenClaw was first published in November 2025 under the name Warelay."
- Wikipedia："Skills are stored as directories containing a SKILL.md file with metadata and instructions."

Hermes Agent：

- README："The self-improving AI agent built by Nous Research."
- README（学习循环）："Agent-curated memory with periodic nudges. Autonomous skill creation after complex tasks."
- README（消息）："Telegram, Discord, Slack, WhatsApp, Signal, and CLI" 由单个 gateway 进程提供
- README（调度）："Built-in cron scheduler with delivery to any platform."
- README（子 Agent）："Spawn isolated subagents for parallel workstreams."
- README：六种终端后端（local、Docker、SSH、Modal、Daytona、Vercel Sandbox）；支持批量轨迹生成与轨迹压缩，用于训练工具调用模型；可用 `hermes import-agent openclaw` 从 OpenClaw、Claude Code、Codex CLI、Cursor 导入设置、记忆与技能
- 文档："Works with Nous Portal, OpenRouter, OpenAI, or any endpoint."；技能兼容 agentskills.io 开放标准

DeepSeek Harness：

- README："DeepSeek Harness (`dsh`) is an open-source agent harness developed by DeepSeek AI."
- README："It is built on an everything-is-a-plugin architecture and powered by Cordis."
- README："DeepSeek Harness is in developer preview and iterating rapidly." / "THERE WILL BE COMPATIBILITY-BREAKING CHANGES."
- README 安装：`npx @deepseek-ai/dsh web`，Web UI 默认 `http://127.0.0.1:3080`；源码方式 `pnpm install`、`pnpm run build`、`pnpm dsh web`
- 官网："DeepSeek Harness is now in public preview worldwide and open source"；提供 macOS（Apple silicon）与 Windows 桌面版；可在聊天中用 “Creator mode” 创建插件；官方插件包括 Agent teams、Auto approval reviewer、Scheduled tasks、Voice input、Terminal、Agent loop、Subagents；社区插件用 GitHub topic `dsh-plugin`
- npm `@deepseek-ai/dsh` description："dsh CLI: profile launch, plugin management, and configuration inspection"

## 第三方评测要点

- DeepInfra 评测（2026-09-09，测试版本 0.1.1-rc.2）：2026-08-13 发布；"everything is a plugin: the model adapter, the tool registry, the session log, and the agent loop itself"（作者转引 README）；可替换会话存储（JSONL、SQLite）、执行（本地、E2B）、shell、子 Agent 提供方（含 subagent-claude-code、subagent-codex、subagent-acp）；模式有 Standard、Minimal、Creator、PTC（Code Mode，模型写一段 TypeScript 程序代替逐个工具调用）；hooks-claude-code / hooks-codex 桥可复用现有 hooks.json，读取 AGENTS.md 与 CLAUDE.md，作为 MCP 客户端；沙箱分 Read Only / Workspace Write / Full access，作者实测 Workspace Write 只限制写不限制读，FAQ 称沙箱不覆盖网络与进程；提供方目录含 Anthropic、OpenAI、Bedrock、Azure 及任意 OpenAI 兼容端点；结论 "dsh is less a product than a chassis"，日常使用更推荐 OpenCode
- eesel（Pi 综述）：仓库 2025-08-09 以 `badlogic/pi-mono` 创建；2025-11-30 Zechner 发布设计文章；2026-04-08 Earendil（Armin Ronacher 的公司）收购 Pi，Zechner 成为股东，同时发布云端 Agent 平台 Lefos；2026-04-30 v0.71.0 移除 Gemini CLI 与 Antigravity 登录；2026-05-07 npm 包迁到 `@earendil-works`；2026-09-29 v0.99.0 加入 MCP（此前明确拒绝 MCP）；2026-10-01 Pi 1.0 与实验性 Pi Durable；支持 30 多家提供方；会话以带 parent id 的 JSONL 树保存，`/tree`、`/fork`；不做逐次工具审批；2025-12 Pi + Claude Opus 4.5 在 Terminal-Bench 2.0 排第 7
- OpenCode 二手资料（rywalker、shareuhack 等）：2025-06 发布，由 SST 团队（Jay V、Frank Wang、Dax Raad、Adam Elmore）的公司 Anomaly 开发，仓库从 `sst/opencode` 迁到 `anomalyco/opencode`；75+ 提供方（经 Models.dev）；2026-01 加入 ChatGPT Plus/Pro 的 Codex OAuth 登录；2026-01-09 Anthropic 在服务端阻止第三方工具使用 Claude 订阅 OAuth，OpenCode 同日移除 Claude Pro/Max 支持；2026-02-19 Anthropic 条款明确订阅 OAuth 不得用于第三方工具；商业化：Go 订阅（10 美元/月）、Zen 按量付费、企业版；称月活开发者 750 万、Zen 年化收入数百万美元（均未经核实）
- OpenClaw（Wikipedia 等）：2025-11-24 以 Warelay 首发，之后叫 CLAWDIS、Clawdbot；2026-01-27 因 Anthropic 商标投诉改名 Moltbot，同日 Moltbook 上线；约 2026-01-30 改名 OpenClaw；2026-01-28/29 Cisco 报告第三方技能做数据外泄与提示注入；2026-02-14 Steinberger 宣布加入 OpenAI，项目移交 OpenClaw Foundation；2026-03 中国限制国企和政府机关在办公电脑上运行 OpenClaw；2026-08-30 OpenClaw 2.0（v2026.8.1）发布，The Register 指出其缺乏网络与文件系统安全边界、Secret Store 不加密、沙箱默认不开启
- Hermes Agent（hermesatlas 社区报告，2026-04-11）：2026-02-25 发布；MIT 协议 Python；会话存 SQLite + FTS5；2026-04-03 Anthropic 阻止 OpenClaw 使用 Claude 订阅后，Nous 推广迁移命令，迁移流量激增；Nous Research 由 Teknium 等联合创办，Paradigm、a16z 领投。其他二手资料：v0.20.0 “Herald” 2026-08-03

## 待核实

- Pi 被 Earendil 收购的日期（2026-04-08）与 Lefos 平台，只见于二手资料
- OpenCode 的融资、Zen 收入、750 万月活
- Anthropic 2026-04-03 阻止 OpenClaw 使用 Claude 订阅，只见于 Hermes 社区报告
- Hermes Agent 当前官方版本号（只见 npm 非官方桥接标注 0.23.0）；PyPI `hermes-agent` 是否为官方发布
- DeepSeek Harness 约 27.6 万星、发布仅三个月，增长异常快，星数只作参考
- 各项目 GitHub 星数均为网页抓取，未经 API 核对
