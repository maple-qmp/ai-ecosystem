---
title: Anthropic
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["Anthropic", "Anthropic PBC"]
released: "2021-01"
competitors: ["[[entities/openai]]", "[[entities/google-deepmind]]"]
depends_on: ["[[entities/aws]]", "[[entities/aws-trainium]]", "[[entities/google-tpu]]", "[[entities/nvidia]]", "[[entities/azure]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-06
sources: ["[[sources/bun-survey-2026-11]]", "[[sources/claude-independent-modules-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]", "[[sources/major-ai-orgs-survey-2026-11]]"]
---

# Anthropic

## 描述

AI 安全与研究公司，2021 年由 Dario Amodei、Daniela Amodei 等前 OpenAI 成员创立，总部位于旧金山。主力产品是 [[entities/claude|Claude]] 模型家族与 [[entities/claude-code|Claude Code]]，并提出了开放协议 [[concepts/model-context-protocol|MCP]]。2025-12 收购 JavaScript 运行时 [[entities/bun|Bun]]（开发公司 [[entities/oven|Oven]]），作为 Claude Code 和 Claude Agent SDK 的基础设施。以安全研究（如 Constitutional AI、可解释性）为核心定位。主要投资方包括 Amazon（累计 80 亿美元，[[entities/aws|AWS]] 是其主要云）、Google 和 2025-11 加入的 [[entities/microsoft|Microsoft]] 与 [[entities/nvidia|NVIDIA]]；模型同时跑在 [[entities/aws-trainium|AWS Trainium]]、[[entities/google-tpu|Google TPU]] 和 NVIDIA GPU 上，是唯一同时上架 AWS、Google Cloud、Azure 三大云的前沿模型。2026-05 H 轮投后估值 9650 亿美元、年化收入超过 470 亿美元；2026-10-26 公开 S-1，申请在 Nasdaq 以代码 ANT 上市。2026 年因拒绝取消“不得用于大规模监控和全自主武器”的合同限制，被美国国防部列为“供应链风险”。

## 开源与依赖分级

Anthropic 的核心产品是专有的，可独立使用的部分集中在标准、基础设施和研究工具（详见 [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]）：

- **完全独立**：[[concepts/model-context-protocol|MCP]]（已捐给 AAIF）、[[concepts/agent-skills|Agent Skills]] 格式、[[concepts/mcp-bundles|MCP Bundles]]、[[entities/sandbox-runtime|Sandbox Runtime]]、[[entities/bun|Bun]]、[[concepts/claude-constitution|Claude 宪法]]（CC0）、[[entities/circuit-tracer|circuit-tracer]] 与 jacobian-lens、[[entities/petri|Petri / Bloom]]（已交给 Meridian Labs）、hh-rlhf 等数据集
- **需要 Claude、可不经 Anthropic**：[[entities/claude-code|Claude Code]]、[[entities/claude-agent-sdk|Claude Agent SDK]]、claude-code-action 等，可走 Amazon Bedrock、Google Cloud、Microsoft Foundry、Claude Platform on AWS
- **可接非 Claude 模型但官方不支持**：通过 [[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点（Ollama、DeepSeek、GLM 等）
- **离不开 Anthropic**：claude.ai 与桌面端、云端会话、Developer Platform 服务端功能、订阅登录、文档技能（docx / pdf / pptx / xlsx，source-available）

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：[[entities/aws|AWS]]（[[entities/aws-trainium|Trainium]]）、[[entities/google-tpu|Google TPU]]、[[entities/nvidia|NVIDIA]] GPU、[[entities/azure|Azure]]
- **竞争 / 替代**：[[entities/openai|OpenAI]]、[[entities/google-deepmind|Google DeepMind]]

## 时间线

- 2021-01 成立
- 2022-04 融资 5.8 亿美元，其中 5 亿来自 FTX
- 2023-03 发布 Claude
- 2023-09 Amazon 宣布投资（首期 12.5 亿美元，2024-03 补足 40 亿）
- 2023-10 Google 投资 5 亿美元并承诺再投 15 亿
- 2024-11 发布 MCP；Amazon 再投 40 亿美元，累计 80 亿
- 2025-03 E 轮 35 亿美元、估值 615 亿；Google 再投 10 亿
- 2025 推出 Claude Code（2025-05 面向公众）
- 2025-05 开源 [[entities/circuit-tracer|circuit-tracer]]
- 2025-07 与美国国防部签 2 亿美元两年合同，约定不得用于大规模监控美国人和全自主武器
- 2025-09 F 轮 130 亿美元、估值 1830 亿；同意支付 15 亿美元和解盗版书训练数据诉讼；停止向中、俄、伊朗、朝鲜控股的实体销售
- 2025-10 与 Google Cloud 合作，最多使用 100 万颗 [[entities/google-tpu|TPU]]
- 2025-11-18 [[entities/microsoft|Microsoft]] 与 [[entities/nvidia|NVIDIA]] 分别承诺投资最多 50 亿、100 亿美元，Anthropic 承诺购买 300 亿美元 Azure 算力
- 2025-10 开源 [[entities/sandbox-runtime|Sandbox Runtime]] 与 [[entities/petri|Petri]]
- 2025-12 MCP 捐给 Linux Foundation 下新成立的 Agentic AI Foundation；[[concepts/agent-skills|Agent Skills]] 作为开放标准发布
- 2025-12-03 宣布收购 [[entities/bun|Bun]]（金额未披露），同时宣布 Claude Code 年化收入达 10 亿美元
- 2026-01 发布新版 [[concepts/claude-constitution|Claude 宪法]]，CC0 协议；成立 Labs 部门
- 2026-02-12 G 轮 300 亿美元、估值 3800 亿（GIC 与 Coatue 领投），年化收入 140 亿美元
- 2026-02-23 指控 [[entities/deepseek|DeepSeek]]、[[entities/moonshot-ai|月之暗面]]、[[entities/minimax|MiniMax]] 用约 2.4 万个虚假账号蒸馏 Claude
- 2026-02-27 拒绝国防部删除使用限制的要求后，被列为“供应链风险”
- 2026-03 成立智库 Anthropic Institute
- 2026-03-31 Claude Code npm 包误带 source map，源码外泄
- 2026-04-07 Project Glasswing：Mythos Preview 只给受信机构
- 2026-05 H 轮 650 亿美元、估值 9650 亿，年化收入超过 470 亿美元；与 [[entities/xai|xAI]] 签约使用 Colossus 1 数据中心
- 2026-05-07 Petri 与 Bloom 交给非营利组织 Meridian Labs
- 2026-05-18 收购 Stainless
- 2026-06 指控 [[entities/alibaba|阿里云]]蒸馏 Claude
- 2026-06-01 秘密提交上市申请
- 2026-06-09 发布 Claude Fable 5 与 Mythos 5
- 2026-07 与 [[entities/amd|AMD]] 合作 2 GW MI450 GPU，AMD 最多投资 50 亿美元
- 2026-07-28 MCP 发布无状态版规范，见 [[concepts/mcp-request-flow|MCP 请求流程]]
- 2026-08 与 Nscale 签约（约 450 亿美元，西弗吉尼亚 460 MW）
- 2026-09-22 起发布 Claude 5.5 系列（Opus / Sonnet / Haiku），见 [[entities/claude|Claude]]
- 2026-10 宣布拿出 5% 股份设立公益基金；国防部停止使用其产品
- 2026-10-26 公开 S-1，申请 Nasdaq 上市（代码 ANT），2026 上半年收入 163 亿美元

## 相关实体

- [[entities/claude|Claude]]
- [[entities/claude-code|Claude Code]]
- [[entities/bun|Bun]]
- [[entities/oven|Oven]]
- [[entities/claude-agent-sdk|Claude Agent SDK]]
- [[entities/sandbox-runtime|Sandbox Runtime（srt）]]
- [[entities/circuit-tracer|circuit-tracer]]
- [[entities/petri|Petri]]
- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/microsoft|Microsoft]]
- [[entities/aws|AWS]]
- [[entities/google-tpu|Google TPU]]

## 相关概念

- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/claude-constitution|Claude 宪法]]
- [[concepts/frontier-safety-frameworks|前沿模型安全框架]]（Responsible Scaling Policy）
- [[concepts/california-sb-53|加州 SB 53]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Bun will remain open source and MIT-licensed, and we will continue to invest in making it the runtime" — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Claude Code reached $1 billion in run-rate revenue in only 6 months" — [[sources/bun-survey-2026-11|Bun 深度调研]]
- "Released under CC0 1.0." — [[sources/claude-independent-modules-survey-2026-11|Claude 独立模块调研]]（Claude 宪法）
- "We have raised $30 billion in Series G funding led by GIC and Coatue, valuing Anthropic at $380 billion post-money." — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Anthropic G 轮公告）
- "Anthropic has raised $65 billion in Series H funding led by Altimeter Capital, Dragoneer, Greenoaks, and Sequoia Capital, valuing the company at $965 billion post-money." — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Anthropic H 轮公告）
- "Anthropic has committed to purchase $30 billion of Azure compute capacity and to contract additional compute capacity up to one gigawatt." — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Microsoft 博客，2025-11-18）
