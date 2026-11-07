---
title: 寒武纪
type: entity
tags: [organization]
kind: company
layer: L0
aliases: ["寒武纪", "Cambricon", "寒武纪科技", "中科寒武纪", "思元", "MLU"]
released: "2016-03"
competitors: ["[[entities/ascend]]", "[[entities/kunlunxin]]", "[[entities/nvidia]]"]
depends_on: ["[[concepts/hbm]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-07
updated: 2026-11-07
sources: ["[[sources/cambricon-survey-2026-11]]", "[[sources/zhipu-ai-survey-2026-11]]", "[[sources/open-weight-flagships-survey-2026-11]]"]
---

# 寒武纪

## 描述

北京中科寒武纪科技股份有限公司，2016 年从中国科学院计算技术研究所的寒武纪课题组分拆成立，创始人陈云霁、陈天石兄弟等，陈天石任董事长兼 CEO。早期为华为麒麟手机芯片提供 NPU IP，2018 年合作终止后转向云端训练与推理加速卡，即思元（MLU）系列。2020 年登陆科创板（688256），2022 年被列入美国实体清单，此后依赖中芯国际代工。在 [[entities/nvidia|NVIDIA]] 对华出口受限后业绩快速增长：2025 年营收 64.97 亿元、同比增长 453%，首次实现年度盈利；2026 年前三季度营收 95.26 亿元、归母净利润 37.15 亿元。国产模型陆续适配寒武纪：[[entities/glm|GLM-4.6]] 首次在寒武纪芯片上做 FP8 / Int4 部署，[[entities/deepseek-v|DeepSeek-V4]] 也完成了适配。

## 生态位置

- **层级**：[[maps/L0-算力与硬件|L0-算力与硬件]] · 芯片厂商
- **上游依赖**：中芯国际代工、[[concepts/hbm|HBM]] 供应（均受出口管制制约）
- **下游**：[[entities/glm|GLM]]、[[entities/deepseek-v|DeepSeek-V]] 等国产模型的推理部署
- **竞争 / 替代**：[[entities/ascend|昇腾]]（[[entities/huawei|华为]]）、[[entities/kunlunxin|昆仑芯]]；替代对象是 [[entities/nvidia|NVIDIA]]

## 时间线

- 2008 中科院计算所启动寒武纪课题
- 2016-03-15 公司成立
- 2018 华为合作终止，转向云端芯片
- 2020-07-20 科创板上市（688256），募资约 3.69 亿美元
- 2022-12-15 被列入美国实体清单
- 2024 营收约 11.8 亿元，仍亏损；Q4 首次单季盈利
- 2025-09-30 [[entities/zhipu-ai|智谱]] GLM-4.6 首次在寒武纪芯片上做 FP8 / Int4 量化部署
- 2025-12 Bloomberg 报道 2026 年计划生产约 50 万颗加速器（含最多 30 万颗思元 590 / 690）
- 2026-02 宣布上市后首次分红
- 2026-03-12 2025 年报：营收 64.97 亿元，归母净利润 20.59 亿元，首次年度盈利
- 2026 DeepSeek-V4 发布后被昇腾与寒武纪适配
- 2026-10-23 三季报：前三季度营收 95.26 亿元（+107%）、归母净利润 37.15 亿元；三季末存货 116.65 亿元
- 2026 下半年 思元 690 量产（报道）；MLU692 三季度交付大型云厂商测试（摩根士丹利）

## 相关实体

- [[entities/huawei|华为]]
- [[entities/ascend|昇腾]]
- [[entities/kunlunxin|昆仑芯]]
- [[entities/nvidia|NVIDIA]]
- [[entities/glm|GLM]]
- [[entities/deepseek-v|DeepSeek-V]]

## 相关概念

- [[concepts/ai-accelerator|AI 加速器]]
- [[concepts/hbm|HBM]]
- [[concepts/quantization|量化]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Due to US sanctions, the company struggled with access to advanced manufacturing processes." — [[sources/cambricon-survey-2026-11|寒武纪调研]]（Wikipedia）
- "2026年1-9月公司营业收入95.26亿元，同比增长106.76%；归属于上市公司股东的净利润37.15亿元，同比增长131.49%" — [[sources/cambricon-survey-2026-11|寒武纪调研]]（东方财富转述三季报）
