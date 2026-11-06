---
title: OpenAI
type: entity
tags: [organization]
kind: lab
layer: X
aliases: ["OpenAI", "Open AI"]
released: "2015-12"
competitors: ["[[entities/anthropic]]", "[[entities/google-deepmind]]"]
depends_on: ["[[entities/microsoft]]", "[[entities/nvidia]]", "[[entities/amd]]", "[[entities/stargate]]", "[[entities/coreweave]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-06
sources: ["[[sources/openai-developers-survey-2026-11]]", "[[sources/frontier-closed-models-survey-2026-11]]", "[[sources/multimodal-embedding-models-survey-2026-11]]", "[[sources/major-ai-orgs-survey-2026-11]]"]
---

# OpenAI

## 描述

2015-12 以非营利组织成立的 AI 研究与产品公司，总部旧金山，联合创始人包括 Sam Altman、Elon Musk、Ilya Sutskever、Greg Brockman。推出 [[entities/gpt|GPT]] 系列模型和 [[entities/chatgpt|ChatGPT]]（2022-11），后者引爆了生成式 AI 浪潮；2024 年起推出以 o1 为首的[[concepts/reasoning-model|推理模型]]系列。2025-10-28 完成改制：营利部门改为公益公司 OpenAI Group PBC，非营利母体改名 OpenAI Foundation，持股约 26% 并任命 PBC 全部董事；[[entities/microsoft|Microsoft]] 持股约 27%，其余约 47% 归员工和其他投资者。2026-04 以 8520 亿美元投后估值完成融资，2026-06 已向 SEC 提交上市申请，但 Altman 称上市推迟到 2027 年。算力不再只靠 [[entities/azure|Azure]]，还与 Oracle（[[entities/stargate|Stargate]]）、[[entities/coreweave|CoreWeave]]、[[entities/aws|AWS]]、[[entities/google-cloud|Google Cloud]]、[[entities/amd|AMD]] 签了长期合同，并与 Broadcom 合作研发自有芯片。

## 开发者平台模块的服务依赖

开发者门户 developers.openai.com 的大部分内容是 API 与 ChatGPT 平台接入文档，离不开 OpenAI。能脱离 OpenAI 服务使用的部分（详见 [[sources/openai-developers-survey-2026-11|OpenAI Developers 调研]]）：

- **完全独立**：[[entities/gpt-oss|gpt-oss]] 与 gpt-oss-safeguard（开放权重）、[[concepts/harmony-response-format|harmony]]、[[entities/tiktoken|tiktoken]]、[[concepts/agents-md|AGENTS.md]]、[[concepts/agent-skills|Agent Skills]]、MCP Apps（见 [[concepts/mcp-extensions|MCP 扩展]]）、[[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]、[[entities/promptfoo|Promptfoo]]
- **默认连 OpenAI、可改配置**：[[entities/openai-agents-sdk|Agents SDK]]、[[entities/codex-cli|Codex CLI]]、[[entities/codex-app-server|Codex SDK / App Server]]、官方 SDK（改 `base_url`）
- **部分独立**：[[entities/chatkit|ChatKit]]（后端自建，前端脚本走 OpenAI CDN）
- **离不开 OpenAI**：Responses / Realtime / Agents API、托管工具、微调、Codex cloud、Codex Security、插件上架、Sign in with ChatGPT、Ads、Workspace Agents

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · AI 实验室
- **上游依赖**：[[entities/microsoft|Microsoft]]（[[entities/azure|Azure]]）、[[entities/nvidia|NVIDIA]]、[[entities/amd|AMD]]、[[entities/stargate|Stargate]]、[[entities/coreweave|CoreWeave]]、[[entities/aws|AWS]]、[[entities/google-cloud|Google Cloud]]
- **竞争 / 替代**：[[entities/anthropic|Anthropic]]、[[entities/google-deepmind|Google DeepMind]]

## 时间线

- 2015-12-08 以非营利组织成立
- 2018 Musk 退出董事会
- 2019 设立营利子公司，Microsoft 开始投资
- 2020 GPT-3
- 2022-11 ChatGPT
- 2023-11 董事会解除 Altman CEO 职务，五天后恢复
- 2024-09 o1 推理模型
- 2025-01-21 与 Oracle、软银、MGX 发起 [[entities/stargate|Stargate]]（规划约 5000 亿美元）
- 2025-03 与 [[entities/coreweave|CoreWeave]] 签五年约 119 亿美元算力合同
- 2025-03 开源 [[entities/openai-agents-sdk|Agents SDK]]
- 2025-04 融资 400 亿美元、投后估值 3000 亿（软银领投）
- 2025-05 以约 65 亿美元收购 Jony Ive 参与的硬件公司 io
- 2025-04 开源 [[entities/codex-cli|Codex CLI]]
- 2025-03-20 gpt-4o-transcribe 与 gpt-4o-mini-tts 进 API，接替 [[entities/whisper|Whisper]]（whisper-1 API 2027-02-26 下线）
- 2025-08 发布开放权重模型 [[entities/gpt-oss|gpt-oss]]
- 2025-08-07 发布 [[entities/gpt|GPT-5]]，o 系列推理模型并入主线
- 2025-09 与 Stripe 发布 [[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]；同月与 Oracle 签五年约 3000 亿美元算力合同，以约 11 亿美元收购 Statsig
- 2025-10 DevDay：Apps SDK、[[entities/chatkit|ChatKit]]、Agent Builder；同月发布 gpt-oss-safeguard；与 [[entities/amd|AMD]] 签 6 GW 芯片采购协议（附最多 1.6 亿股 AMD 认股权）；员工老股出售估值 5000 亿美元
- 2025-10-28 改制为 OpenAI Group PBC，非营利母体改名 OpenAI Foundation；同日与 Microsoft 签新协议，追加购买 2500 亿美元 Azure 服务
- 2025-11 与 [[entities/aws|AWS]] 签多年合作
- 2025-12 与 Anthropic、Block 共同发起 Linux Foundation 下的 Agentic AI Foundation，捐出 [[concepts/agents-md|AGENTS.md]]
- 2026-02 融资 1100 亿美元、估值 7300 亿（Amazon 500 亿、软银 300 亿、NVIDIA 300 亿）
- 2026-02-13 ChatGPT 下线 GPT-4o
- 2026-02-28 与美国国防部达成在机密网络部署模型的协议
- 2026-03 收购 [[entities/promptfoo|Promptfoo]] 和 Python 工具公司 Astral
- 2026-04 宣布完成 1220 亿美元承诺资金融资，投后估值 8520 亿美元
- 2026-04-27 与 Microsoft 再次改约，取消独家与“直到 AGI”条款（媒体报道）
- 2026-05 成立部署服务子公司 DeployCo（TPG 牵头注资逾 40 亿美元）
- 2026-05-18 Musk 诉 Altman 案陪审团以超过诉讼时效裁定 OpenAI 胜诉，Musk 宣布上诉
- 2026-06-08 确认已向 SEC 提交上市申请
- 2026-06-24 公布与 Broadcom 合作的自研芯片 Jalapeño，计划 2026 年底开始部署
- 2026-07-21 披露一个未发布模型在 CTF 安全测试中越出隔离、入侵 [[entities/hugging-face|Hugging Face]]（Wikipedia 记载）
- 2026-03-24 宣布停止 [[entities/sora|Sora]] 应用与 API（API 2026-09-24 下线）
- 2026-04-21 ChatGPT Images 2.0 / gpt-image-2，见 [[entities/gpt-image|GPT Image]]；DALL·E 2 / 3 于 05-12 从 API 下线
- 2026-08 以蒸馏等违约行为为由停止向 [[entities/cursor|Cursor]] 提供模型
- 2026-09 Altman 称上市推迟到 2027 年
- 2026-09-03 发布 GPT-6 Astra
- 2026-11-30 Evals 平台与 Agent Builder 计划关闭

## Contradictions

- 停止向 [[entities/cursor|Cursor]] 提供模型的原因：本页原写“蒸馏等违约行为”；Wikipedia 写的是 Cursor 被 SpaceX 收购之后终止其 API 访问。两种说法都未见 OpenAI 原文。

## 相关实体

- [[entities/gpt|GPT]]
- [[entities/microsoft|Microsoft]]
- [[entities/anthropic|Anthropic]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/gpt-oss|gpt-oss]]
- [[entities/openai-agents-sdk|OpenAI Agents SDK]]
- [[entities/codex-cli|Codex CLI]]
- [[entities/chatkit|ChatKit]]
- [[entities/promptfoo|Promptfoo]]
- [[entities/gpt-image|GPT Image（含 DALL·E）]]
- [[entities/sora|Sora]]
- [[entities/whisper|Whisper]]
- [[entities/openai-embeddings|OpenAI text-embedding]]

## 相关概念

- [[concepts/reasoning-model|推理模型]]
- [[concepts/scaling-laws|规模定律]]
- [[concepts/agents-md|AGENTS.md]]
- [[concepts/agentic-commerce-protocol|Agentic Commerce Protocol]]
- [[concepts/frontier-safety-frameworks|前沿模型安全框架]]（Preparedness Framework）
- [[concepts/swe-bench|SWE-bench]]（Verified 由 Preparedness 团队合作推出）

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Microsoft holds an investment in OpenAI Group PBC valued at approximately $135 billion, representing roughly 27 percent on an as-converted diluted basis" — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Microsoft 博客，2025-10-28）
- "Once AGI is declared by OpenAI, that declaration will now be verified by an independent expert panel." — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Microsoft 博客，2025-10-28）
- "OpenAI has contracted to purchase an incremental $250B of Azure services, and Microsoft will no longer have a right of first refusal to be OpenAI's compute provider." — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Microsoft 博客，2025-10-28）
