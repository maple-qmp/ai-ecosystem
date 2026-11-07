---
title: LongMemEval
type: concept
tags: [method]
layer: X
aliases: ["LongMemEval", "长期交互记忆评测"]
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-06
updated: 2026-11-06
sources: ["[[sources/context-memory-survey-2026-11]]"]
---

# LongMemEval

## 定义

由 Di Wu 等提出的长期交互记忆基准，包含 500 个问题，测试信息提取、多会话推理、知识更新、时间推理和无法回答时的拒答。论文与作者仓库是本页依据。

## 关键特征

- **任务构造**：把证据嵌入带时间的多轮历史，再要求助手回答；并非只搜索单个关键词。
- **分阶段分析**：索引将历史变成可存储条目，检索选择候选，读取阶段根据证据生成回答。
- **指标分离**：可计算中间检索 Recall@k 等指标，也需要检查最终问答质量；召回正确不等于回答正确。
- **更新与时间**：测试用户事实改变及时间关系，超出简单事实回忆。
- **局限**：主要针对交互记忆，不足以证明企业权限隔离、工具执行或任务恢复可靠。论文中商业系统实测发生在 2024 年，不能当作当前产品性能。

## 应用

可用五类能力指导自建知识库助手测试集。比较厂商自报成绩时应核对数据版本、使用模型、预算、是否读入完整历史及评分器；本次仅借鉴方法，没有复现排行榜。

## 生态位置

- 层级：[[maps/X-横切主题|X-横切主题]]
- 研究依据与详细设计：[[sources/context-memory-survey-2026-11|专题来源索引]]

## 相关概念

- [[concepts/agent-memory|Agent 记忆]]
- [[concepts/observational-memory|观察式记忆]]
- [[concepts/ai-application-evaluation|AI 应用评测]]
- [[concepts/benchmark-contamination|基准污染与饱和]]

## 相关实体

- [[entities/mastra|Mastra]]

## 我的判断

<!-- 仅由用户填写。 -->

## 来源摘录

本页采用来源转述；逐字摘录与原始链接见 [[sources/context-memory-survey-2026-11|专题来源索引]]。
