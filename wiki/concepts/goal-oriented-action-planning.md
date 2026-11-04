---
title: 目标导向行动规划（GOAP）
type: concept
tags: [method]
layer: L4
aliases: ["目标导向行动规划（GOAP）", "Goal-Oriented Action Planning", "GOAP"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/java-agent-ecosystem-survey-2026-11]]"]
---

# 目标导向行动规划（GOAP）

## 定义

源自游戏 AI 的规划方法：给 Agent 一组带前置条件和效果的动作，再给一个目标，由规划器在运行时搜索一条能达成目标的动作序列。[[entities/embabel|Embabel]] 把它用作 Agent 框架的默认规划器：流程不是让 LLM 每一步自由决定，也不是开发者预先画好的固定图，而是由代码中的规划器根据当前条件推导。

## 关键特征

- **声明式**：开发者只写 goals、actions、conditions（在 Embabel 中是类型化领域对象）
- **运行时规划**：条件变化时可重新规划出新路径
- **可解释、可复现**：规划结果和执行轨迹可检查
- **LLM 只负责单个动作**：规划本身由确定性算法完成
- **可替换**：Embabel 的规划器可插拔，也支持 Utility AI（按效用分数选动作）

## 应用

- [[entities/embabel|Embabel]]：默认规划器，可与显式状态机混用

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]]
- 与 [[entities/langgraph|LangGraph]] 式“预先定义状态图”、ReAct 式“LLM 逐步决定”是三种不同的 Agent 控制流思路

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/java-agent-development|Java Agent 开发]]

## 相关实体

- [[entities/embabel|Embabel]]
- [[entities/langgraph|LangGraph]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "a planner searches for a sequence of actions that satisfies the goal." — [[sources/java-agent-ecosystem-survey-2026-11|Java Agent 开发生态调研]]
