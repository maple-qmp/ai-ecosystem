---
title: Stargate
type: entity
tags: [project]
kind: project
layer: L0
aliases: ["Stargate", "星际之门", "Stargate Project"]
org: "[[entities/openai|OpenAI]]"
released: "2025-01"
competitors: []
depends_on: ["[[entities/nvidia]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-05
updated: 2026-11-05
sources: ["[[sources/ai-compute-hardware-survey-2026-11]]"]
---

# Stargate

[[entities/openai|OpenAI]] 与 Oracle、SoftBank（及 MGX）合作的大型数据中心计划，把算力的计量单位从机架换成吉瓦（GW）。2025-09-23 宣布五个新站点——Oracle 主导的德州 Shackelford County、新墨西哥 Doña Ana County 与一个未公布的中西部站点，SoftBank 主导的俄亥俄 Lordstown 与德州 Milam County，当时口径为规划容量接近 7 GW、三年内投资超 4000 亿美元；2025-10-30 又宣布密歇根 Saline Township 园区（约 1 GW）。旗舰站点是德州 Abilene：规划 1.2 GW、约 100 万张 H100 等效算力，Larry Ellison 称最终将装入 45 万颗以上 GB200。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 数据中心项目
- **上游依赖**：[[entities/nvidia|NVIDIA]] GPU 供应、电力与土建；资金来自 Oracle、SoftBank、MGX
- **替代路径**：向 [[concepts/gpu-cloud|GPU 云]] 或三大云租用算力（OpenAI 同时在做：[[entities/aws|AWS]] 约 380 亿美元、[[entities/azure|Azure]] 2500 亿美元采购、[[entities/coreweave|CoreWeave]] 约 120 亿美元）

## 时间线

- 2025-01 项目公布
- 2025-09-23 宣布五个新站点，规划容量接近 7 GW、三年内投资超 4000 亿美元；据称从 30 多个州的 300 多份提案中选出
- 2025-10-30 宣布密歇根 Saline Township 园区（约 1 GW，Related Digital 与 Oracle 开发）
- 2026-04 Epoch AI 卫星追踪估计 Abilene 8 栋楼中 4 栋投运、约 0.3 GW 在运（此前估计 0.6 GW，后下调），7、8 号楼投运预期由 2026-07 推迟到 2026-11，完工预期 Q4 2026
- 2026-07-27 Epoch 追踪页给出 Abilene 当前约 50.9 万张 H100 等效、规划约 101.9 万张
- 2029 Epoch 预计整个计划容量超过 9 GW

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/nvidia|NVIDIA]]
- [[entities/coreweave|CoreWeave]]
- [[entities/aws|AWS]]
- [[entities/azure|Microsoft Azure]]

## 相关概念

- [[concepts/gpu-cloud|GPU 云]]
- [[concepts/scale-up-interconnect|超节点与纵向扩展互联]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Epoch AI 的卫星追踪（2026-04）估计 8 栋楼中 4 栋投运、约 0.3 GW 在运" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
- "规划 1.2 GW、约 100 万张 H100 等效算力，Larry Ellison 称最终将装入 45 万颗以上 GB200" — [[sources/ai-compute-hardware-survey-2026-11|AI 算力与硬件调研]]
