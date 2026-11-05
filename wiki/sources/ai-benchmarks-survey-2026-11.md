---
title: AI 评测基准调研（2026-11）
type: source
tags: [notes]
source_note: "[[AI评测基准调研-2026-11]]"
created: 2026-11-05
updated: 2026-11-05
sources:
  - "[[concepts/swe-bench]]"
  - "[[concepts/chatbot-arena]]"
  - "[[concepts/humanitys-last-exam]]"
  - "[[concepts/gpqa]]"
  - "[[concepts/mmlu]]"
  - "[[concepts/arc-agi]]"
  - "[[concepts/terminal-bench]]"
  - "[[concepts/tau-bench]]"
  - "[[concepts/benchmark-contamination]]"
  - "[[concepts/scaling-laws]]"
---

# AI 评测基准调研（2026-11）

## Summary

梳理前沿模型发布时最常引用的八组评测基准及“基准污染 / 饱和”问题，检索日期 2026-11-05。一手资料是各基准官方 GitHub 仓库的 README，以及规模定律两篇原始论文的摘要；排行榜分数、融资和部分日期来自搜索摘要与第三方聚合站，标为二手，分数互相矛盾，只作量级参考。2026 年的主线：静态知识问答基准（MMLU、GPQA）饱和，OpenAI 2026-02 停止报告 SWE-bench Verified，评测重心转向 Agent 类（Terminal-Bench 2.0、τ-bench、SWE-bench Pro）和交互式基准（ARC-AGI-3）。附录核实了规模定律。

## Key Points

- **SWE-bench**：真实 GitHub issue 修复；Verified 为 500 道人工确认子集（2024-08）；OpenAI 认为 Verified 已污染，改推 SWE-bench Pro（2026-09 发布 V2，642 题）
- **Chatbot Arena**：众包盲测投票排行榜；2026-01-28 改名 Arena；《The Leaderboard Illusion》批评私测选择性公开
- **Humanity's Last Exam**：CAIS 与 Scale AI 的 2,500 道专家级题目，2026-01 发表于 Nature；2026 年中最好成绩约 55%（无工具）
- **GPQA Diamond**：198 道研究生级科学题，2026 年榜首 94%–96%，已饱和
- **MMLU / MMLU-Pro**：MMLU 已饱和；MMLU-Pro 改 10 选项、12,000 多题
- **ARC-AGI**：抽象推理网格题；ARC-AGI-3（2026-03）改为交互式游戏环境，发布时模型不到 1%
- **Terminal-Bench 2.0**：89 道终端任务，Harbor harness，按“Agent + 模型”排名
- **τ-bench**：工具 + 模拟用户的客服 Agent 基准，pass^k 指标；2.0 增加六种语言与语音
- **污染与饱和**：canary 字符串、加密分发、私有测试集、重写同分布新题（GSM1k）
- **规模定律**：Kaplan 2020 幂律；Chinchilla 2022 参数与 token 同比扩展

## Mentioned Pages

- [[concepts/swe-bench|SWE-bench]]
- [[concepts/chatbot-arena|Chatbot Arena（LMArena）]]
- [[concepts/humanitys-last-exam|Humanity's Last Exam]]
- [[concepts/gpqa|GPQA]]
- [[concepts/mmlu|MMLU / MMLU-Pro]]
- [[concepts/arc-agi|ARC-AGI]]
- [[concepts/terminal-bench|Terminal-Bench]]
- [[concepts/tau-bench|τ-bench]]
- [[concepts/benchmark-contamination|基准污染与饱和]]
- [[concepts/scaling-laws|规模定律]]
- [[entities/promptfoo|Promptfoo]]
- [[entities/langsmith|LangSmith]]
- [[entities/openai|OpenAI]]
- [[entities/anthropic|Anthropic]]
