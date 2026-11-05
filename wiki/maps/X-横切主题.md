---
title: X-横切主题
type: map
layer: X
created: 2026-11-04
updated: 2026-11-05
---

# X-横切主题

> 组织与人物、安全对齐、政策法规、开源社区、关键论文

← 返回 [[overview|生态总览]]

## 手工整理

### AI 实验室

- [[entities/anthropic|Anthropic]]
- [[entities/openai|OpenAI]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/meta-ai|Meta AI]]
- [[entities/deepseek|DeepSeek]]
- [[entities/moonshot-ai|月之暗面（Moonshot AI）]]
- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/minimax|MiniMax]]
- [[entities/mistral-ai|Mistral AI]]
- [[entities/xai|xAI（SpaceX Super Intelligence）]]

### 公司

- [[entities/microsoft|Microsoft]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/bytedance|字节跳动]]（含火山引擎）
- [[entities/vercel|Vercel]]
- [[entities/langchain-inc|LangChain 公司]]
- [[entities/mastra-inc|Mastra 公司]]
- [[entities/jetbrains|JetBrains]]
- [[entities/oven|Oven]]（已并入 Anthropic）

### 安全与可解释性

- [[concepts/claude-constitution|Claude 宪法]]
- [[entities/circuit-tracer|circuit-tracer]]（含 jacobian-lens）
- [[entities/petri|Petri / Bloom]]

### 评测基准

- [[concepts/swe-bench|SWE-bench]]（含 Verified、Pro）
- [[concepts/chatbot-arena|Chatbot Arena（LMArena / Arena）]]
- [[concepts/humanitys-last-exam|Humanity's Last Exam]]
- [[concepts/gpqa|GPQA]]
- [[concepts/mmlu|MMLU / MMLU-Pro]]
- [[concepts/arc-agi|ARC-AGI]]
- [[concepts/terminal-bench|Terminal-Bench]]
- [[concepts/tau-bench|τ-bench]]
- [[concepts/benchmark-contamination|基准污染与饱和]]

### 政策法规

- [[concepts/eu-ai-act|欧盟《人工智能法》]]
- [[concepts/china-generative-ai-measures|中国生成式 AI 管理办法与备案]]
- [[concepts/us-federal-ai-policy|美国联邦 AI 行政令]]
- [[concepts/california-sb-53|加州 SB 53]]（含纽约 RAISE Act）
- [[concepts/frontier-safety-frameworks|前沿模型安全框架]]（Anthropic RSP、OpenAI Preparedness）

### 人物

- [[entities/jarred-sumner|Jarred Sumner]]

### 概念

- [[concepts/scaling-laws|规模定律]]

## 自动列表（Dataview）

```dataview
TABLE WITHOUT ID file.link AS 条目, kind AS 类型, org AS 所属, released AS 发布, choice(reviewed, "✅", "⏳") AS 已核实
FROM "wiki/entities" OR "wiki/concepts"
WHERE layer = "X"
SORT kind ASC, file.name ASC
```
