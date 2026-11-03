<!-- llm-wiki-log-header-start -->
# Wiki 操作日志

每次摄入、Lint 运行和维护操作都会自动记录在这里。推荐使用**操作历史**面板获得更好的可视化呈现：
- Cmd+P → "查看摄入历史"
- 或从 设置 → 自动维护 → 操作历史 进入

---
> 操作日志，按时间倒序记录所有 wiki 操作。

## [2026-11-04] ingest | LangChain 生态深度调研

- 来源：LangChain / LangGraph 1.0 公告、Interrupt 2026 汇总、2026-08 与 2026-10 通讯、Deep Agents 文档、Fortune 融资报道、Wikipedia（`raw/LangChain生态深度调研-2026-11.md`）
- 新建来源页 `sources/langchain-ecosystem-survey-2026-11`
- 重写 `langchain`：去掉种子标记，补 1.0 变化（create_agent、中间件、标准内容块、langchain-classic）与时间线
- 新建 4 个实体页：`langchain-inc`（公司与融资）、`langgraph`、`langsmith`（产品模块与时间线）、`deep-agents`
- 新建概念页 `agent-harness`；`ai-agent` 补链接与来源
- 更新 L4、X 地图页

## [2026-11-04] ingest | Vercel 开源框架的服务依赖调研

- 来源：Next.js 自托管文档、Adapter API 公告、AI SDK / Workflow DevKit / Turborepo 文档等（`raw/Vercel开源框架服务依赖调研-2026-11.md`）
- 新建来源页 `sources/vercel-oss-dependency-survey-2026-11`
- 新建 5 个实体页：`vercel`（含开源模块四级依赖分级）、`nextjs`、`vercel-ai-sdk`、`workflow-devkit`、`turborepo`
- 更新 L4、X 地图页

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


## [2026-11-04 05:08] Wiki 维护报告


> Wiki 状态概览：共 46 个页面，7 个缺失别名，重复 0 个，断链 7 个（其中 0 个涉及重复页面），孤立 1 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 1 个。本次 Lint 耗时 3 秒

> 检测到 7 个页面缺少别名

### 缺失别名的页面（程序检测）[共 7 个]

- [[entities/vllm]]
- [[entities/pytorch]]
- [[entities/openai]]
- [[entities/langchain]]
- [[entities/cursor]]
- [[entities/cuda]]
- [[entities/claude-code]]

### 断链（程序检测）[共 7 个]

- [[overview]] → **maps/L0-算力与硬件\**（页面不存在）
- [[overview]] → **maps/L1-数据\**（页面不存在）
- [[overview]] → **maps/L2-基础模型\**（页面不存在）
- [[overview]] → **maps/L3-训练与推理\**（页面不存在）
- [[overview]] → **maps/L4-开发工具与Agent\**（页面不存在）
- [[overview]] → **maps/L5-应用\**（页面不存在）
- [[overview]] → **maps/X-横切主题\**（页面不存在）

### 标签越界（程序检测）[共 1 个]

- [[sources/mcp-spec-2026-07-28]] — 无效：mcp, specification

### 孤立页面（程序检测）[共 1 个]

- [[conventions]] — 无其他 Wiki 页面链接至此




## [2026-11-04 05:25] Wiki 维护报告


> Wiki 状态概览：共 46 个页面，0 个缺失别名，重复 0 个，断链 0 个（其中 0 个涉及重复页面），孤立 0 个（其中 0 个是重复页面），空洞 0 个，无来源引证 0 个，标签越界 0 个。本次 Lint 耗时 4 秒

未检测到重复、断链、空洞、孤立页面或无来源引证。


