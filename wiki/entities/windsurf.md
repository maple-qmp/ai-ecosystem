---
title: Windsurf（Devin Desktop）
type: entity
tags: [product]
kind: app
layer: L5
aliases: ["Windsurf", "Devin Desktop", "Codeium", "Windsurf Editor", "SWE-1.5"]
org: "Cognition AI"
released: ""
competitors: ["[[entities/cursor]]", "[[entities/github-copilot]]", "[[entities/claude-code]]"]
depends_on: ["[[entities/kimi]]", "[[entities/claude]]", "[[entities/gpt]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-06
sources: ["[[sources/ai-applications-survey-2026-11]]"]
---

# Windsurf（Devin Desktop）

## 描述

AI 代码编辑器，前身是代码补全插件 Codeium，公司 2025-04 改名 Windsurf。2025 年它经历了三方争夺：OpenAI 谈妥约 30 亿美元收购，但独家期 2025-07-11 到期作废；Google 随即以约 24 亿美元许可费与补偿聘走 CEO Varun Mohan 等人进入 DeepMind；2025-07-14 [[entities/devin|Devin]] 的开发商 Cognition 签约收购剩下的公司。之后 Cognition 的自研编程模型都先在这里上线：SWE-1.5（2025-10，基于未具名的开源基座模型）、SWE-1.6、SWE-1.7（基于 [[entities/kimi|Kimi]] K2.7）。2026 年初的 Windsurf 2.0 加入 Agent Command Center 并内嵌 Devin；2026-06-02 它升级为 Devin Desktop，默认界面变成管理本地与云端 Agent 的控制台，支持 Agent Client Protocol（ACP），并与 Windsurf 完全向后兼容。

## 生态位置

- **层级**：[[maps/L5-应用|L5-应用]] · 编程 Agent / AI 编辑器
- **上游依赖**：Cognition 自研 SWE 系列（SWE-1.7 基于 [[entities/kimi|Kimi]] K2.7）；第三方 [[entities/claude|Claude]]、[[entities/gpt|GPT]]
- **竞争 / 替代**：[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]、[[entities/claude-code|Claude Code]]

## 时间线

- 2025-04 Codeium 改名 Windsurf（二手报道）
- 2025-05 OpenAI 洽谈约 30 亿美元收购（二手报道）
- 2025-07-11 OpenAI 独家期到期；Google 以约 24 亿美元聘走 CEO 与核心研发（二手报道）
- 2025-07-14 Cognition 签约收购
- 2025-10-29 SWE-1.5 在 Windsurf 上线
- 2026 年初 Windsurf 2.0：Agent Command Center，内嵌 [[entities/devin|Devin]]（二手报道日期为 04-15）
- 2026-06-02 升级为 Devin Desktop，支持 ACP
- 2026-09-11 Fusion harness 上线 Devin Desktop

## 相关实体

- [[entities/devin|Devin]]
- [[entities/kimi|Kimi]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/openai|OpenAI]]

## 相关概念

- [[concepts/ai-agent|AI Agent]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "We’re excited to share that Cognition has signed a definitive agreement to acquire Windsurf, the agentic IDE." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition，2025-07-14）
- "End-to-end reinforcement learning (RL) on real task environments using our custom Cascade agent harness on top of a leading open-source base model." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition SWE-1.5，2025-10-29）
- "We’re excited to announce Devin Desktop - the next generation of Windsurf." — [[sources/ai-applications-survey-2026-11|AI 应用产品调研]]（Cognition，2026-06-02）
