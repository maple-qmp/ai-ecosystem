---
title: 智谱与 GLM 时间线调研（2026-11）
type: source
tags: [notes]
source_note: "[[智谱-GLM调研-2026-11]]"
url: https://huggingface.co/zai-org
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[entities/zhipu-ai]]"
  - "[[entities/glm]]"
  - "[[entities/alibaba]]"
  - "[[concepts/anthropic-messages-api]]"
---

# 智谱与 GLM 时间线调研（2026-11）

## Summary

整理 [[entities/zhipu-ai|智谱（Z.ai）]]从 2019 年清华孵化到 2026-11 的公司、上市与 [[entities/glm|GLM]] 模型时间线。智谱 2026-01-08 在港交所上市，是中国第一家上市的大模型公司。2025-07 的 GLM-4.5 起，旗舰模型以 MIT 协议开放权重；GLM-5（744B）、GLM-5.2（1M 上下文）延续 MIT。2026-08 的 GLM-5.3 改为自定义许可证：12 个月收入超 100 亿美元的模型服务商须先通过 Z.ai 安全审查。模型日期和许可证以 Hugging Face 模型卡为准（2026-11-05 读取）。

## Key Points

- **起源**：2019 年清华 KEG 孵化，唐杰；2022 年 ACL 发表 GLM 论文；2023 年开源 ChatGLM-6B 系列
- **股东**：2023 年融资的投资方有[[entities/alibaba|阿里巴巴]]、腾讯、美团、蚂蚁、小米、红杉中国；2025-01 被列入美国实体清单
- **GLM-4.5（2025-07-28）**：355B / 32B [[concepts/mixture-of-experts|MoE]]，统一推理、编码与 Agent，MIT
- **国产芯片**：GLM-4.6 首次在寒武纪芯片上做 FP8 / Int4 [[concepts/quantization|量化]]部署，并适配华为昇腾、摩尔线程
- **上市（2026-01-08）**：港交所 2513
- **GLM-5（2026-02）**：744B / 40B，面向 “Agentic Engineering”；之后 5.1（04）、5.2（06，1M 上下文，IndexShare）、5.3（08，只改后训练）
- **许可证收紧**：GLM-5.3 的 MaaS 安全审查门槛是 100 亿美元年收入，只针对超大云厂商；GLM-5.3-Flash 仍为 MIT
- **开发者生态**：[[concepts/anthropic-messages-api|Anthropic Messages API]] 兼容端点让 [[entities/claude-code|Claude Code]] 直接用 GLM；官方的多项基准成绩就在 Claude Code 里测；2026-07 推出自有编码应用 ZCode
- **与阿里生态**：阿里是早期投资方；2026-05-20 起阿里云百炼上架 GLM-5.1

## Mentioned Pages

- [[entities/zhipu-ai|智谱（Z.ai）]]
- [[entities/glm|GLM]]
- [[entities/alibaba|阿里巴巴（通义）]]
- [[entities/claude-code|Claude Code]]
- [[entities/kimi|Kimi]]
- [[entities/minimax-m|MiniMax-M]]
- [[entities/qwen|Qwen]]
- [[concepts/anthropic-messages-api|Anthropic Messages API]]
- [[concepts/mixture-of-experts|混合专家（MoE）]]
- [[concepts/quantization|量化]]
- [[concepts/reasoning-model|推理模型]]
