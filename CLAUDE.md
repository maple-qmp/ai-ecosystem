# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 这是什么

这是一个 Obsidian 知识库（不是代码项目），主题是 **AI 技术生态地图**，正文用中文写。它由 Obsidian 插件 **Karpathy LLM Wiki**（`karpathywiki`）驱动：素材放进 `raw/`，插件摄入后在 `wiki/` 下生成或合并页面。你手写的页面也必须遵守插件的格式，否则插件下次合并时会覆盖或清理掉你写的内容。

## 结构与数据流

```
raw/                 原始素材（剪藏、规范摘录），插件摄入的输入
wiki/
  sources/           每份素材对应一个来源页（type: source）
  entities/          实体：组织、模型、产品、框架（type: entity）
  concepts/          概念、方法、标准（type: concept）
  maps/              7 个层级地图页 L0–L5 + X，人工整理（插件不自动生成）
  overview.md        首页：分层表、Mermaid 图、Dataview 维护看板
  index.md / log.md  目录 / 倒序操作日志，由插件维护格式
  conventions.md     本库规则（插件的 LLM 也会读）
  schema/config.md   插件的页面模板与合并规则
templates/           Templater 模板（手写新页用）
```

规则只以 `wiki/conventions.md` 和 `wiki/schema/config.md` 为准，动手前先读这两份。其中最容易出错的几条：

- **`tags` 只能用插件词表里的值**，写了词表外的值会被插件删掉。实体可用：person, organization, project, product, event, place, other；概念可用：theory, method, field, phenomenon, standard, term, other。生态分类一律写在 `layer`（L0–L5 / X）和 `kind` 字段里。
- 链接写完整路径：`[[entities/slug|显示名]]`、`[[concepts/slug|…]]`、`[[sources/slug|…]]`、`[[maps/L4-开发工具与Agent|…]]`。文件名用小写短横线 slug，中文名放 `title` 和 `aliases`。
- `org` 写所属组织；`depends_on` 只写**技术上游**（芯片、框架、基座模型），不要写所属公司。
- `origin: claude-seed` 表示凭训练知识生成、尚未核实；`origin: source` 表示依据 `sources` 中的素材写成。`reviewed: true` 只能由用户设置。
- 不得改写任何页面的 `## 我的判断` 一节。
- 事件（发布、融资、新版本）写进相关实体的「时间线」，不单独建页。

## 摄入一份素材的完整步骤

参照 MCP 2026-07-28 专题（`raw/MCP规范-2026-07-28.md` → `wiki/sources/mcp-spec-2026-07-28.md` → `wiki/concepts/mcp-*.md`）：

1. 素材存进 `raw/`。
2. 建 `wiki/sources/<slug>.md`，`sources:` 列出由它产生的页面。
3. 新建或更新 entity / concept 页：补 `sources`，`来源摘录` 只放原文逐字引用。
4. 同步更新：`index.md` 加条目，`log.md` 顶部加一条日志，所属 `maps/` 页的手工列表加链接。

## 渲染陷阱（都已经踩过）

- **Mermaid**：flowchart / graph 中，节点文字一律加引号（`A["…"]`、`B{"…？"}`），连线文字用 `-->|"…"|`。不加引号时，中文标点、`/`、`·` 会让旧版 Mermaid 解析失败；`-. 文字 .-` 里的 `2.1` 这类点号在所有版本都会出错。时序图无此问题。
- **Dataview**：列名里有空格必须加引号，例如 `AS "超过 90 天未更新"`。
- `schema/config.md` 里的示例链接要包在反引号里，否则会产生断链和图谱里的幽灵节点。模板里同样不要放 `[[maps/]]` 这类空链接。

## 验证（需要 Obsidian 正在运行）

用 `obsidian` CLI（`/opt/homebrew/bin/obsidian`），第一个参数写 `vault="AI生态"`：

```bash
# 未解析的链接（应为 {}）
obsidian vault="AI生态" eval code="JSON.stringify(Object.fromEntries(Object.entries(app.metadataCache.unresolvedLinks).filter(([k,v])=>Object.keys(v).length)))"
```

```bash
# 截图当前界面
obsidian vault="AI生态" dev:screenshot path=/tmp/shot.png
```

检查 Mermaid 或 Dataview 是否真的渲染成功，要用 `eval` 把页面以 `{state:{mode:'preview'}}` 打开，逐步滚动后检查 `.mermaid svg` 或 `.block-language-dataview` 的内容。长页面是懒渲染的，必须滚动到底才能看到全部块。Dataview 显示 “No results to show” 不算错误。eval 环境里拿不到 `require('obsidian')`，也拿不到 `loadMermaid`。

## 注意事项

- `.obsidian` 是指向 `../.obsidian` 的软链接，**与同一 iCloud 目录下的其他库共用**。不要修改它，包括插件设置、书签、排除规则。共享配置里的“排除文件”规则会把 `wiki/overview`、`wiki/index`、`wiki/log`、`wiki/conventions` 从搜索和图谱中隐藏，用户已决定保持现状。
- 路径中有空格和中文（`~/Library/Mobile Documents/iCloud~md~obsidian/Documents/AI生态`），Shell 命令里要加引号。
- Git：只有 `master` 分支，没有远程仓库，直接在 `master` 上提交。`.gitignore` 排除了 `.obsidian`、`.trash` 等目录。
