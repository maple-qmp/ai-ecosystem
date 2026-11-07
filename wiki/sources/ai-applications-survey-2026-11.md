---
title: AI 应用产品调研（2026-11）
type: source
tags: [notes]
source_note: "[[AI应用产品调研-2026-11]]"
url: https://www.anthropic.com/news/product
created: 2026-11-05
updated: 2026-11-07
sources:
  - "[[entities/chatgpt]]"
  - "[[entities/claude-app]]"
  - "[[entities/gemini-app]]"
  - "[[entities/doubao-app]]"
  - "[[entities/kimi-app]]"
  - "[[entities/perplexity]]"
  - "[[entities/devin]]"
  - "[[entities/windsurf]]"
  - "[[entities/midjourney]]"
  - "[[entities/suno]]"
  - "[[entities/claude-code]]"
  - "[[entities/cursor]]"
  - "[[entities/github-copilot]]"
  - "[[entities/openclaw]]"
---

# AI 应用产品调研（2026-11）

## Summary

补全 L5 应用层，按四组整理面向终端用户的 AI 产品。对话助手：[[entities/chatgpt|ChatGPT]]、[[entities/claude-app|Claude 应用]]、[[entities/gemini-app|Gemini App]]、[[entities/doubao-app|豆包 App]]、[[entities/kimi-app|Kimi App]]；AI 搜索：[[entities/perplexity|Perplexity]]；编程 Agent：[[entities/devin|Devin]]、[[entities/windsurf|Windsurf（Devin Desktop）]]，并核实已有的 [[entities/claude-code|Claude Code]]、[[entities/cursor|Cursor]]、[[entities/github-copilot|GitHub Copilot]]；创意工具：[[entities/midjourney|Midjourney]]、[[entities/suno|Suno]]。

2026 年的三条主线：一是对话助手进入十亿用户量级，ChatGPT 每周 9 亿活跃用户（2026-02），Gemini App 月活 10 亿（2026-08），国内豆包 App 月活约 3.82 亿（2026-05）；二是助手从聊天转向 Agent，Claude Cowork（2026-09 与聊天合并为一个 Claude）、Gemini Spark、Kimi 的 OK Computer 与 Agent Swarm、Perplexity Computer、ChatGPT Work 都让模型替用户执行多步任务；三是编程 Agent 市场整合，Cognition 收购 Windsurf 并改造成 Devin Desktop，SpaceX 收购 Cursor，GitHub Copilot 用 Agent HQ 接入第三方 Agent。另一个值得注意的现象：美国的编程产品大量以中国开放权重模型 [[entities/kimi|Kimi]] 为基座，Cursor 的 Composer 2 基于 Kimi K2.5，Cognition 的 SWE-1.7 基于 Kimi K2.7。

## Key Points

- **资料可靠性**：一手资料覆盖 Anthropic / Claude、Google 博客与 Alphabet 财报讲话、GitHub 博客与文档、Cognition、Cursor、Midjourney、Suno 的官方博客与更新页、Kimi 帮助中心；另读取了 12 个 Wikipedia 词条。openai.com、perplexity.ai 返回 403，Windsurf、Suno 的 Wikipedia 词条因限流未读到，相关事实仍有一部分标为「二手报道」。素材末尾附「更正记录」，列出第一版的错误
- **对话助手规模**：ChatGPT 9 亿周活（2026-02）；Gemini App 月活 9.5 亿（2026-07-22）→ 10 亿（2026-08-11）；豆包 App 月活约 3.82 亿（QuestMobile，2026-05）；Kimi App 未查到 2026 年单独用户数据
- **Claude 应用**：claude.ai 2023-07 随 Claude 2 上线；Cowork 2026-01-12 研究预览、04-09 正式可用、07-07 上网页和移动端、09-16 与聊天合并为一个 Claude；另有 Claude Design、Claude Tag、Claude Science；套餐 Free / Pro / Max / Ultra
- **ChatGPT 商业化**：2026-01 宣布测试广告，03 月起展示，08 月广告收入达 10 亿美元；Atlas 浏览器 2025-10 上线、2026-03 宣布与桌面应用和 Codex 合并、08-09 关停
- **Perplexity**：2022-12 上线；自研 Sonar 基于 Llama 3.3，另经 Microsoft Azure 调用 OpenAI、Anthropic、xAI 模型；Comet 浏览器、Perplexity Computer；2026-02 放弃广告；2026 年初估值约 212 亿美元
- **编程 Agent 整合**：Windsurf 2025-07 先被 Google 聘走核心团队、再被 Cognition 收购，2026-06 升级为 Devin Desktop；Cognition 2026-09 E 轮估值 480 亿美元，年化收入 09-25 超过 10 亿美元；Cursor 2026 年初年化收入超过 30 亿美元，2026-08-14 被 SpaceX 收购完成
- **GitHub Copilot**：coding agent 2025-09 正式可用，Agent HQ 2025-10 发布，Copilot CLI 2026-02 正式可用，Copilot app 2026-06 发布；模型表含 OpenAI、Anthropic、Google、Microsoft、Moonshot AI、xAI 六家；按 AI 积分计费
- **创意工具**：Midjourney 自研 V 系列到 V8.2（2026-07），有 Video V1，三起好莱坞版权诉讼 2025-11 合并审理，2026-07 首次收购；Suno 与 Warner、BMG、Believe 从诉讼转为合作，2026-09 推出与它们合作开发的 v6，2026-06 估值 54 亿美元
- **未收录**：Sora、Veo、可灵、FLUX 等生成模型由 L2 多模态调研负责

## Mentioned Pages

- [[entities/chatgpt|ChatGPT]]
- [[entities/claude-app|Claude 应用]]
- [[entities/gemini-app|Gemini App]]
- [[entities/doubao-app|豆包 App]]
- [[entities/kimi-app|Kimi App]]
- [[entities/perplexity|Perplexity]]
- [[entities/devin|Devin]]
- [[entities/windsurf|Windsurf（Devin Desktop）]]
- [[entities/midjourney|Midjourney]]
- [[entities/suno|Suno]]
- [[entities/claude-code|Claude Code]]
- [[entities/cursor|Cursor]]
- [[entities/github-copilot|GitHub Copilot]]
- [[entities/openai|OpenAI]]
- [[entities/anthropic|Anthropic]]
- [[entities/google-deepmind|Google DeepMind]]
- [[entities/bytedance|字节跳动]]
- [[entities/moonshot-ai|月之暗面]]
- [[entities/microsoft|Microsoft]]
- [[entities/xai|xAI（SpaceX Super Intelligence）]]
- [[entities/gpt|GPT]]
- [[entities/claude|Claude]]
- [[entities/gemini|Gemini]]
- [[entities/doubao|豆包大模型]]
- [[entities/kimi|Kimi]]
- [[entities/grok|Grok]]
- [[entities/llama|Llama]]
- [[entities/deepseek-r1|DeepSeek-R1]]
- [[concepts/agent-skills|Agent Skills]]
- [[concepts/ai-agent|AI Agent]]
