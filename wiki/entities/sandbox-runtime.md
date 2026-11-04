---
title: Sandbox Runtime（srt）
type: entity
tags: [project]
kind: infra
layer: L4
aliases: ["Sandbox Runtime", "Anthropic Sandbox Runtime", "srt", "@anthropic-ai/sandbox-runtime"]
org: "[[entities/anthropic]]"
released: "2025-10"
competitors: []
depends_on: []
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]"]
---

# Sandbox Runtime（srt）

## 描述

[[entities/anthropic|Anthropic]] 开源的轻量沙箱工具，在操作系统层面限制任意进程能读写哪些文件、能连哪些网络，不需要容器。它是 [[entities/claude-code|Claude Code]] 沙箱功能的底层，但完全独立：不需要 Claude 模型，也不连 Anthropic 服务，可以拿来隔离任何 Agent、本地 [[concepts/model-context-protocol|MCP]] 服务器、构建脚本或普通命令。Apache-2.0，npm 包 `@anthropic-ai/sandbox-runtime`，目前标为 Beta 研究预览（2026-10 为 0.0.81）。

## 原理

核心观点是**文件隔离和网络隔离缺一不可**：只隔离文件，进程可以把数据发出去；只隔离网络，进程可以改配置或读走 SSH 密钥再想别的办法外传。

- **文件系统**：读默认放开，可先禁止一大片（如 `/Users`）再放行具体路径；写默认全部禁止，只能显式放行（如 `.`、`/tmp`），`denyWrite` 优先于 `allowWrite`
- **网络**：默认全部禁止，按域名放行；沙箱内的进程不能直接联网，所有流量都被逼着走主机上的两个代理——HTTP/HTTPS 走 HTTP 代理，其他 TCP 走 SOCKS5 代理，代理按白名单 / 黑名单逐个请求放行
- **各平台的实现**：
  - macOS：用 `sandbox-exec` 加动态生成的 Seatbelt 配置，配置只允许连到本机某个端口，代理就监听在那里；还能读取系统的沙箱违规日志做实时告警
  - Linux：用 bubblewrap，**直接去掉进程的网络命名空间**，代理监听在挂载进沙箱的 Unix socket 上，进程只能通过这个文件通道联网
  - Windows：在专用本地账户 `srt-sandbox` 下运行，用 Windows Filtering Platform 按该账户的 SID 拦截出站连接（只放行到代理端口的回环连接），再配合写受限令牌和显式 ACL
- 限制作用于整个进程树，子进程继承同样的约束

## 用法

- **CLI**：`srt <命令>`，配置在 `~/.srt-settings.json`；配置文件存在但无效时直接报错退出，不会悄悄回退到默认值
- **给 MCP 服务器加沙箱**：在 `.mcp.json` 里把 `command` 从 `npx` 改成 `srt`，原命令放进 `args`
- **库**：`SandboxManager.initialize(config)` 启动代理，再包装要执行的命令
- **热更新**：`--control-fd` 从文件描述符逐行读取新配置，网络规则下一次连接即生效；文件规则已写进 Seatbelt 配置或 bubblewrap 参数，运行中不能改
- **只用代理**：`srt proxy` 只跑过滤代理，给在别处运行工作负载的宿主使用

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · Agent 安全基础设施
- **上游依赖**：操作系统自带的沙箱机制（Seatbelt、bubblewrap、WFP）
- **竞争 / 替代**：容器与微虚拟机方案（Docker、gVisor、Firecracker）、托管沙箱服务；[[entities/codex-cli|Codex CLI]] 自带的沙箱；[[entities/openai-agents-sdk|OpenAI Agents SDK]] 的沙箱 Agent（本地版在 Linux 上不做系统级隔离）

## 时间线

- 2025-10 开源，随 Claude Code 沙箱功能一同发布
- 2026 年加入 Windows 支持、`--control-fd` 热更新和 `srt proxy`
- 2026-10-20 发布 0.0.81

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/codex-cli|Codex CLI]]

## 相关概念

- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "A lightweight sandboxing tool for enforcing filesystem and network restrictions on arbitrary processes at the OS level, without requiring a container." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "Both filesystem and network isolation are required for effective sandboxing." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "The network namespace of the sandboxed process is removed entirely, so all network traffic must go through the proxies running on the host (listening on Unix sockets that are bind-mounted into the sandbox)" — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（Linux）
