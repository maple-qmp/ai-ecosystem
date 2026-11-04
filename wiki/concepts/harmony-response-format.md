---
title: harmony 响应格式
type: concept
tags: [standard]
layer: L3
aliases: ["harmony 响应格式", "harmony response format", "OpenAI Harmony", "openai-harmony"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# harmony 响应格式

## 定义

[[entities/openai|OpenAI]] 为开放权重模型 [[entities/gpt-oss|gpt-oss]] 定义的对话结构格式，规定提示词如何拼接、模型输出如何切分。gpt-oss 只在这个格式上训练过，官方明确说不用它模型就不能正常工作。OpenAI 同时开源了渲染与解析库 `openai/harmony`（Rust 内核，带 Python 和 JavaScript 绑定，Apache-2.0）。

## 关键特征

- **角色**：system、developer、user、assistant，另有工具角色；system 放模型身份、推理强度、可用通道，developer 放指令和函数工具定义
- **通道（channel）**：assistant 的输出分到 `analysis`（思维链）、`commentary`（工具调用及调用前的说明）、`final`（给用户看的回答）三个通道；工具调用必须走 commentary
- **推理强度**：在 system 消息里写 low / medium / high
- **思维链处理**：analysis 通道的内容不应直接展示给用户，多轮对话中通常只保留 final 内容
- **与 Responses API 对应**：结构上和 OpenAI Responses API 的输出项一一对应，便于推理服务把 gpt-oss 包装成 Responses 兼容接口

## 应用

- 推理引擎（[[entities/vllm|vLLM]]、Ollama、LM Studio、Transformers）在聊天模板里实现 harmony，用户一般不用手写
- 自己写推理服务或做微调数据时，用 harmony 库渲染和解析，避免格式错误导致输出质量下降
- 让 [[entities/codex-cli|Codex CLI]] 这类只认 Responses API 的工具接上本地 gpt-oss

## 生态位置

- **层级**：[[maps/L3-训练与推理|L3-训练与推理]] · 模型输入输出格式
- **独立性**：格式与库都完全独立，不依赖 OpenAI 服务

## 相关概念

- [[concepts/reasoning-model|推理模型]]
- [[concepts/transformer|Transformer]]

## 相关实体

- [[entities/gpt-oss|gpt-oss]]
- [[entities/openai|OpenAI]]
- [[entities/vllm|vLLM]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "gpt-oss should not be used without using the harmony format as it will not work correctly." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
