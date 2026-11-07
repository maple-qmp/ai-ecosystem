---
title: Computer Use
type: concept
tags: [method]
layer: L4
aliases: ["Computer Use", "computer use", "电脑操作", "计算机使用", "Computer-Using Agent", "CUA", "GUI Agent"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/ai-applications-expansion-survey-2026-11]]"]
---

# Computer Use

## 定义

让模型像人一样操作图形界面的能力：模型看屏幕截图，输出移动鼠标、点击、键盘输入等动作，循环执行直到任务完成，不需要目标软件提供 API。[[entities/anthropic|Anthropic]] 在 2024-10-22 随升级版 Claude 3.5 Sonnet 推出 computer use 公测，是第一个把这一能力作为通用 API 提供的前沿厂商；[[entities/openai|OpenAI]] 2025-01 推出基于 Computer-Using Agent（CUA）模型的 Operator。它是 [[concepts/ai-agent|AI Agent]] 从“调用工具”扩展到“操作任意软件”的关键一步，也是 [[concepts/ai-browser|AI 浏览器]]和桌面 Agent 的底层能力。

## 关键特征

- **感知—动作循环**：截图 → 模型判断 → 鼠标 / 键盘动作 → 新截图；每一步都要视觉理解和规划，速度慢、成本高于 API 调用
- **通用但脆弱**：能操作没有 API 的旧系统，但界面变化、弹窗、验证码都会让它出错，所以产品普遍加入人工确认、权限分级和沙箱
- **安全风险**：网页内容可能注入恶意指令（提示注入），Agent 又握有登录态和支付能力，因此浏览器 Agent 常限制敏感操作
- **评测**：主流基准是 OSWorld。Claude 3.5 Sonnet 首发时仅截图类别 14.9%（放宽步数 22.0%），Operator 首发自报 32.6%（50 步）；到 2026 年 OSWorld-Verified 头部成绩约 80%，开放权重的 Kimi K2.6 约 73%；另有长程桌面工作流的 OSWorld 2.0（二手报道）

## 应用

- **API 工具**：Claude 的 computer use 工具；[[entities/gpt|GPT]] 系列的 computer use 能力
- **浏览器 Agent**：ChatGPT Atlas 的 agent 模式、Perplexity Comet、Chrome 的 Gemini auto browse，见 [[concepts/ai-browser|AI 浏览器]]
- **桌面与办公 Agent**：[[entities/claude-app|Claude Cowork]] 2026-03 加入 computer use 研究预览；[[entities/notion-ai|Notion AI]] 2026-10 让 Agent 自带计算机和浏览器；[[entities/microsoft-365-copilot|Microsoft 365 Copilot]] 的 Copilot Cowork
- **框架**：[[entities/mastra|Mastra]] 的 Sandboxes / Workspaces 提供 computer use 能力

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]（能力与工具）；产品形态落在 [[maps/L5-应用|L5-应用]]
- **上游**：多模态[[concepts/reasoning-model|推理模型]]（视觉理解 + 规划）

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/ai-browser|AI 浏览器]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]（对照：MCP 走结构化接口，computer use 走图形界面）

## 相关实体

- [[entities/claude|Claude]]
- [[entities/claude-app|Claude 应用]]
- [[entities/chatgpt|ChatGPT]]
- [[entities/perplexity|Perplexity]]
- [[entities/notion-ai|Notion AI]]
- [[entities/microsoft-365-copilot|Microsoft 365 Copilot]]
- [[entities/kimi|Kimi]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "by looking at a screen, moving a cursor, clicking buttons, and typing text." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
- "Claude 3.5 Sonnet scored 14.9% in the screenshot-only category." — [[sources/ai-applications-expansion-survey-2026-11|AI 应用扩容调研]]
