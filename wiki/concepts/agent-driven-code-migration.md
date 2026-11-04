---
title: Agent 驱动的代码迁移
type: concept
tags: [method]
layer: L4
aliases: ["Agent 驱动的代码迁移", "AI 辅助代码迁移", "AI 重写", "agent-driven code migration"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/bun-survey-2026-11]]"]
---

# Agent 驱动的代码迁移

## 定义

让多个编程 Agent 并行工作，把大型代码库从一种语言或框架整体移植到另一种。人负责设计流程和验收标准，Agent 负责逐文件翻译、修编译错误和评审。目前规模最大的公开案例是 [[entities/bun|Bun]] 2026-07 从 Zig 到 Rust 的重写：[[entities/jarred-sumner|Jarred Sumner]] 用预发布版 [[entities/claude|Claude]] Fable 5，在 [[entities/claude-code|Claude Code]] 中跑约 50 个动态工作流、最多 64 个并行 Claude，11 天合并约 100 万行改动。

## 关键特征

- **先机械翻译，后重构**：第一版贴近原代码逐行移植，行为对齐后再改成地道写法、减少 `unsafe`
- **以现有测试套件为准**：不跳过、不删除测试，全部通过才算完成；Bun 在六个平台上跑完整套件
- **实现与评审分离**：每处改动由一个 Agent 实现，另两个独立上下文的 Agent 对抗式评审（"The implementer doesn't review. The reviewer doesn't implement."）
- **编译器做反馈回路**：目标语言的类型和所有权检查比风格指南更能拦住错误
- **成本可量化**：Bun 合并前约 59 亿未缓存输入 token、6.9 亿输出 token，按 API 价约 16.5 万美元；作者估计人工团队需约一年

## 应用

- 内存安全迁移：C / C++ / Zig → Rust（Bun 的主要动机是消除 use-after-free、double-free 和泄漏）
- 工具链移植：Bun 的 `bun check` 是 typescript-go 的移植；Bun 早期本身也是 esbuild 转译器的移植
- 框架升级、API 替换等大范围机械改动

## 争议与局限

- Bun 重写引入 19 个已知回归（均已修复），约 4% 代码仍在 `unsafe` 块中
- Zig 作者 Andrew Kelley 认为测试套件过去没拦住的 bug，换成未经人工审读的代码同样拦不住，并质疑性能提升的归因
- 审读百万行生成代码的成本、长期可维护性和项目治理（开源社区对 AI 代码的接受度）仍无定论

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 方法
- **依赖**：编程 Agent 与 [[concepts/agent-harness|Agent Harness]]（并行工作流、子 Agent、长时执行）

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-harness|Agent Harness]]
- [[concepts/javascript-runtime|JavaScript 运行时]]

## 相关实体

- [[entities/bun|Bun]]
- [[entities/jarred-sumner|Jarred Sumner]]
- [[entities/claude-code|Claude Code]]
- [[entities/claude|Claude]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "I used a pre-release version of Claude Fable 5 for much of the Rust rewrite." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "The implementer doesn't review. The reviewer doesn't implement." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Compiler errors are a better feedback loop than a style guide." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "This rewrite introduced 19 known regressions, each of which has been fixed." — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "The main issue here had nothing to do with the language features of Zig vs Rust" — [[sources/bun-survey-2026-11|Bun 深度调研]]
