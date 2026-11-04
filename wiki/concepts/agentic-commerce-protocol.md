---
title: Agentic Commerce Protocol
type: concept
tags: [standard]
layer: L4
aliases: ["Agentic Commerce Protocol", "ACP", "Agentic Checkout Spec", "Delegated Payment Spec"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-04
sources: ["[[sources/openai-developers-survey-2026-11]]"]
---

# Agentic Commerce Protocol

## 定义

让 AI Agent 代用户向商家下单的开放协议，2025-09 由 [[entities/openai|OpenAI]] 与 Stripe 联合发布，Apache-2.0，规范站 agenticcommerce.dev。它是 ChatGPT “Instant Checkout” 的底层协议：Agent 负责收集买家、配送和支付信息并展示结账界面，订单状态和扣款仍在商家自己的系统里完成。注意与同样缩写为 ACP 的 Agent Communication Protocol 不是一回事。

## 关键特征

- **商品 Feed 规范**：商家定期提供 CSV 或 JSON 商品数据（标识、描述、价格、库存、图片、配送），也可经 API 或 SFTP 提交
- **Agentic Checkout Spec**：商家实现一组结账会话端点（创建、更新、完成），Agent 调用它们；商家负责校验、算税、风控、决定接单或拒单
- **Delegated Payment Spec**：Agent 方生成一次性的委托支付请求，限定最高金额和有效期，交给商家指定的支付服务商（PSP）换取支付令牌；Stripe 的 Shared Payment Token 是首个兼容实现
- **商家是记账主体**：OpenAI 不是 merchant of record，商家用自己的 PSP 收款

## 应用

- 商家在 ChatGPT 内支持即时购买
- 其他 Agent 平台或支付服务商按同一规范接入（规范本身不限定 Agent 方是 ChatGPT）

## 生态位置

- **层级**：[[maps/L4-开发工具与Agent|L4-开发工具与Agent]] · 协议
- **独立性**：规范开源、可独立实现；但目前主要的 Agent 方实现是 ChatGPT，商家接入 ChatGPT 需走 OpenAI 的审核与上线流程
- **同类**：Google 的 Agent Payments Protocol（AP2）

## 相关概念

- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/agent2agent-protocol|Agent2Agent 协议（A2A）]]

## 相关实体

- [[entities/openai|OpenAI]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "OpenAI is not the merchant of record in the Agentic Commerce Protocol." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
- "The checkout session is rendered in the OpenAI UI, but the actual checkout state and payment processing occurs on the merchant's systems." — [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]
