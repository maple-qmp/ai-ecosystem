---
title: 使用约定
type: conventions
created: 2026-11-04
updated: 2026-11-04
---

# 使用约定

本库是 **AI 技术生态地图**。LLM 在摄入、更新、查询时须遵守以下规则：

## 分层（`layer` 字段，必填）

| 值 | 含义 |
|---|---|
| L0 | 算力与硬件 |
| L1 | 数据 |
| L2 | 基础模型 |
| L3 | 训练与推理 |
| L4 | 开发工具与 Agent |
| L5 | 应用 |
| X | 横切：组织、人物、安全、政策、论文 |

组织（公司/实验室）默认放 `X`，只有业务高度集中于某一层时才归到该层（如 NVIDIA → L0）。

## 实体细分（`kind` 字段）

`lab` · `company` · `model-family` · `model` · `infra` · `framework` · `app` · `dataset` · `benchmark` · `person`

`tags` 仍只用插件词表（organization / product / project / person …），生态分类一律写在 `kind` 和 `layer` 里，避免被插件清理。

## 关系字段

- `org`：所属组织
- `depends_on`：上游依赖（下层能力）
- `competitors`：同层竞品或替代品
- `open_weights`：模型是否开放权重
- `status`：active / deprecated / rumor

## 规则

1. **实体优先于事件**：发布会、融资等事件写进相关实体的「时间线」，不单独建页。
2. **一物一页**：新建前先查 `index.md` 和 aliases，存在就合并。
3. **事实与观点分开**：观点只写在「我的判断」。LLM 不得改写这一节。
4. **来源标记**：`origin` 取值为 `claude-seed`（Claude 凭训练知识生成）或 `source`（依据 `sources` 中的素材写成）。**种子页面**：`origin: claude-seed` 的页面未经来源核实；摄入相关素材时优先补充其 `sources`。人工核实后设 `reviewed: true`。
5. **新页必须链接**：至少链接所属层的地图页 `maps/…` 和一个相关页面。
6. **文件名**：小写短横线 slug；中文名放在 `title` 和 `aliases`。
7. **Mermaid 写法**：flowchart / graph 中，节点文字一律加双引号 `A["文字"]`、`B{"判断？"}`，连线文字用 `-->|"文字"|`，不要用 `-- 文字 -->` 或 `-. 文字 .-`。否则中文标点、`/`、`·` 和版本号里的 `.` 会在部分 Obsidian 版本（尤其是手机端）中导致整张图渲染失败。
8. **兼容插件**：每个实体页和概念页都要写 `aliases`，至少包含正式名称；正文第一行写实际内容，不放提示框；来源页的 `tags` 只能用 paper / article / book / transcript / clippings / notes / other；表格里不写带显示名的双链（插件不识别转义竖线，会报断链），需要显示名时改用列表。
