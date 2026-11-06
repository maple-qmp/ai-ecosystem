---
title: Microsoft
type: entity
tags: [organization]
kind: company
layer: X
aliases: ["Microsoft", "微软", "Microsoft AI", "MAI"]
competitors: ["[[entities/google-deepmind]]", "[[entities/aws]]", "[[entities/google-cloud]]"]
depends_on: ["[[entities/nvidia]]", "[[entities/azure]]"]
status: active
as_of: 2026-11
origin: source
reviewed: false
created: 2026-11-04
updated: 2026-11-06
sources: ["[[sources/inference-engines-survey-2026-11]]", "[[sources/major-ai-orgs-survey-2026-11]]"]
---

# Microsoft

## 描述

[[entities/openai|OpenAI]] 的最大外部股东与云合作伙伴：2019 年起累计投资超过 130 亿美元，2025-10 OpenAI 改制后持股约 27%（约 1350 亿美元），模型与产品 IP 权利延长到 2032 年；2026-04 双方改约，Microsoft 不再独家销售 OpenAI 模型。通过 [[entities/azure|Azure]]（Microsoft Foundry）提供 OpenAI、[[entities/claude|Claude]] 等多家模型，2025-11 还承诺向 [[entities/anthropic|Anthropic]] 投资最多 50 亿美元。2024-03 成立 Microsoft AI（MAI），由 DeepMind 与 Inflection AI 联合创始人 Mustafa Suleyman 领导，2025-08 起发布 MAI 系列自研模型。旗下 GitHub 推出 [[entities/github-copilot|GitHub Copilot]]，自研芯片有 Maia 加速器和 Cobalt CPU。微软研究院提出了 [[concepts/lora|LoRA]] 等关键微调方法，并开源了分布式训练库 [[entities/deepspeed|DeepSpeed]]（ZeRO），后者 2025 年移交 Linux Foundation、进入 PyTorch Foundation。

## 生态位置

- **层级**：[[maps/X-横切主题|X-横切主题]] · 公司
- **上游依赖**：[[entities/nvidia|NVIDIA]]（GPU）、自研 Maia 加速器（见 [[entities/azure|Azure]]）
- **竞争 / 替代**：[[entities/google-deepmind|Google DeepMind]]（模型）、[[entities/aws|AWS]]、[[entities/google-cloud|Google Cloud]]（云）

## 时间线

- 2019 起投资 OpenAI
- 2020 发布 ZeRO 与 DeepSpeed
- 2021 GitHub Copilot 预览
- 2023-01 宣布对 OpenAI 多年数十亿美元的追加投资
- 2023-11 公布自研 Maia 加速器与 Cobalt CPU；Altman 被解职期间一度宣布他将加入微软
- 2024-03-19 成立 Microsoft AI（MAI），Mustafa Suleyman 任 CEO
- 2025 DeepSpeed 移交 Linux Foundation，5 月成为 PyTorch Foundation 托管项目
- 2025-08-28 MAI 发布首批自研模型 MAI-Voice-1、MAI-1-preview；10 月 MAI-Image-1
- 2025-10-28 与改制后的 OpenAI 签新协议：持股约 27%，IP 权利延长到 2032 年，AGI 改由独立专家组核验，OpenAI 追加购买 2500 亿美元 Azure 服务
- 2025-11-06 MAI 成立超级智能团队
- 2025-11-18 与 NVIDIA、Anthropic 达成合作，承诺投资 Anthropic 最多 50 亿美元
- 2026-01 公布 Maia 200，06 月在爱荷华与亚利桑那数据中心投产
- 2026-03 MAI 拆出 Copilot 部门（Jacob Andreou 领导），Suleyman 专管超级智能部门；03-09 推出基于 Claude Cowork 的 Copilot Cowork
- 2026-04-27 与 OpenAI 再次改约：取消独家销售，IP 许可改为非独占，删除“直到 AGI”条款（媒体报道）
- 2026-06 MAI 发布 7 个自研模型，含 MAI-Image-2.5、MAI-Code-1-Flash

## 相关实体

- [[entities/openai|OpenAI]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/deepspeed|DeepSpeed]]
- [[entities/azure|Azure]]
- [[entities/anthropic|Anthropic]]

## 相关概念

- [[concepts/lora|LoRA]]

## 我的判断

<!-- 你的观点写在这里，和上面的事实分开 -->

## 来源摘录

- "Microsoft's IP rights for both models and products are extended through 2032 and now include models post-AGI" — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Microsoft 博客，2025-10-28）
- "NVIDIA and Microsoft are committing to invest up to $10 billion and up to $5 billion respectively in Anthropic." — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Microsoft 博客，2025-11-18）
- "On August 28, 2025, MAI announced its first in-house models for its products called MAI-Voice-1 and MAI-1-preview" — [[sources/major-ai-orgs-survey-2026-11|主要 AI 实验室与公司调研]]（Wikipedia）
