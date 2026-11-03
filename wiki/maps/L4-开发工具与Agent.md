---
title: L4-开发工具与Agent
type: map
layer: L4
created: 2026-11-04
updated: 2026-11-04
---

# L4-开发工具与Agent

> SDK、Agent 框架、RAG、评测、可观测性、协议

← 返回 [[overview|生态总览]]

## 手工整理

### 框架

- [[entities/langchain|LangChain]]

### 概念

- [[concepts/rag|检索增强生成（RAG）]]
- [[concepts/ai-agent|AI Agent]]
- [[concepts/model-context-protocol|Model Context Protocol（MCP）]]
  - [[concepts/mcp-request-flow|MCP 请求流程（2026-07-28）]]
  - [[concepts/multi-round-trip-requests|多轮往返请求（MRTR）]]
  - [[concepts/mcp-extensions|MCP 扩展]]

## 自动列表（Dataview）

```dataview
TABLE WITHOUT ID file.link AS 条目, kind AS 类型, org AS 所属, released AS 发布, choice(reviewed, "✅", "⏳") AS 已核实
FROM "wiki/entities" OR "wiki/concepts"
WHERE layer = "L4"
SORT kind ASC, file.name ASC
```
