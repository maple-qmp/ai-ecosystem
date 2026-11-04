---
title: X-横切主题
type: map
layer: X
created: 2026-11-04
updated: 2026-11-04
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
- [[entities/mistral-ai|Mistral AI]]

### 公司

- [[entities/microsoft|Microsoft]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/vercel|Vercel]]
- [[entities/langchain-inc|LangChain 公司]]
- [[entities/mastra-inc|Mastra 公司]]
- [[entities/jetbrains|JetBrains]]

### 概念

- [[concepts/scaling-laws|规模定律]]

## 自动列表（Dataview）

```dataview
TABLE WITHOUT ID file.link AS 条目, kind AS 类型, org AS 所属, released AS 发布, choice(reviewed, "✅", "⏳") AS 已核实
FROM "wiki/entities" OR "wiki/concepts"
WHERE layer = "X"
SORT kind ASC, file.name ASC
```
