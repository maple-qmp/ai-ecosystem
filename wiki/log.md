<!-- llm-wiki-log-header-start -->
# Wiki 操作日志

每次摄入、Lint 运行和维护操作都会自动记录在这里。推荐使用**操作历史**面板获得更好的可视化呈现：
- Cmd+P → "查看摄入历史"
- 或从 设置 → 自动维护 → 操作历史 进入

---
> 操作日志，按时间倒序记录所有 wiki 操作。

## [2026-11-04] ingest | MCP 规范 2026-07-28 版

- 来源：官方规范、变更日志、扩展总览（`raw/MCP规范-2026-07-28.md`）
- 新建来源页 `sources/mcp-spec-2026-07-28`
- 新建 3 个概念页：`mcp-request-flow`（7 阶段流程、新旧对照、错误码、弃用清单）、`multi-round-trip-requests`、`mcp-extensions`
- 重写 `model-context-protocol`：去掉种子标记，补充版本演进表，有来源支撑
- 更新 L4 地图页和 `anthropic` 时间线

## [2026-11-04] init | 建立 AI 生态知识库骨架

- 新建 7 个层级地图页（`maps/`）、`overview`、`index`、`conventions`、`schema/config`
- 新建 **23 个实体页**和 **10 个概念页**，全部为种子页面（`origin: claude-seed`，`reviewed: false`），内容截至 2026-06，待用真实来源核实
- 新建 `templates/` 下的手写模板
