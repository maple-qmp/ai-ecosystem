---
title: MCP Bundles（MCPB）
type: concept
tags: [standard]
layer: L4
aliases: ["MCP Bundles", "MCPB", ".mcpb", "Desktop Extensions", "DXT"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/claude-independent-modules-survey-2026-11]]"]
---

# MCP Bundles（MCPB）

## 定义

一种打包本地 [[concepts/model-context-protocol|MCP]] 服务器的文件格式：`.mcpb` 是一个 zip 包，里面放服务器的全部代码和依赖，再加一份描述服务器及其能力的 `manifest.json`。用户双击安装，宿主应用读取清单、弹出配置界面、启动服务器，类似 Chrome 的 `.crx` 或 VS Code 的 `.vsix`。由 [[entities/anthropic|Anthropic]] 提出，原名 Desktop Extensions（DXT），后改名并移到 modelcontextprotocol 组织，MIT 协议。

## 关键特征

- **清单驱动**：`manifest.json` 写名称、版本、入口命令、运行时、需要用户填写的参数（如 API key、目录路径）及其类型，宿主据此生成配置表单并把值注入环境变量或参数
- **自带依赖**：服务器连同依赖一起打包，用户不用自己装 Node、Python 包
- **工具链**：`npm install -g @anthropic-ai/mcpb`，`mcpb init` 引导生成清单，`mcpb pack` 打包；2026-10 为 2.1.2
- **宿主实现开源**：仓库里同时放着 Claude 桌面端加载和校验 bundle 的代码，其他应用可以照着实现
- **改名对照**：`dxt` CLI → `mcpb`，`.dxt` → `.mcpb`，`@anthropic-ai/dxt` → `@anthropic-ai/mcpb`

## 应用

- 把本地 MCP 服务器做成面向普通用户的一键安装包
- 给支持本地 MCP 的桌面应用加“扩展商店”式的安装流程
- 可与 [[entities/sandbox-runtime|Sandbox Runtime]] 搭配，限制装进来的服务器能访问的文件和网络

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 开放格式
- **独立性**：格式、CLI、校验代码都不依赖 Anthropic 服务；Claude 桌面端只是其中一个宿主

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/mcp-extensions|MCP 扩展]]
- [[concepts/agent-skills|Agent Skills]]

## 相关实体

- [[entities/anthropic|Anthropic]]
- [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/claude-code|Claude Code]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "MCP Bundles (`.mcpb`) are zip archives containing a local MCP server and a `manifest.json` that describes the server and its capabilities." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
- "The format is spiritually similar to Chrome extensions (`.crx`) or VS Code extensions (`.vsix`)" — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]
