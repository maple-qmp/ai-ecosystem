---
title: AI 评测基准调研（2026-11）
type: source
tags: [notes]
source_note: "[[AI评测基准调研-2026-11]]"
created: 2026-11-05
updated: 2026-11-06
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

梳理前沿模型发布时最常引用的八组评测基准，以及“基准污染 / 饱和”问题，检索日期 2026-11-05。一手资料包括 arXiv 论文摘要、各基准官网与官方排行榜（swebench.com、Scale AI、arena.ai、lastexam.ai、arcprize.org、tbench.ai）和 GitHub README。2026-11-05 第二轮核实后，首轮来自聚合站、与官方不符的分数已改正或删除。融资、OpenAI 停止报告 Verified 的博客和部分第三方分数仍是二手资料。2026 年的主线：静态知识问答基准（MMLU、GPQA）饱和，OpenAI 2026-02 停止报告 SWE-bench Verified，评测重心转向 Agent 类（Terminal-Bench 2.0、τ-bench、SWE-bench Pro）和交互式基准（ARC-AGI-3）。附录核实了规模定律。

## Key Points

- **SWE-bench**：2,294 道真实 GitHub issue 修复题；Verified 是 500 道人工确认子集（2024-08），官方榜最高 79.2%，2026-02 后没有新提交；OpenAI 改推 SWE-Bench Pro（2026-09 发布 V2，642 题，公开榜榜首 61.5%）
- **Chatbot Arena**：众包盲测投票排行榜；2026-01-28 改名 Arena；《The Leaderboard Illusion》指出私测造成选择性披露（例如 Meta 私测了 27 个变体），且对战数据分配不对称
- **Humanity's Last Exam**：CAIS 与 Scale AI 的 2,500 道专家级题目，2026-01 发表于 Nature；先后推出 HLE-Rolling（2025-10）和 HLE-Diamond（2026-09）
- **GPQA**：448 道研究生级科学题（Diamond 子集 198 题），专家准确率 65%、非专家 34%；2026 年已饱和
- **MMLU / MMLU-Pro**：MMLU 已饱和；MMLU-Pro 改 10 选项、12,000 多题
- **ARC-AGI**：抽象推理网格题；ARC-AGI-3（2026-03-24）改为交互式环境，人类 100%、AI 不到 1%；ARC Prize 2026 结果于 12-04 公布
- **Terminal-Bench**：2.0（2025-11，89 题）→ 2.1 → 3.0（2026-07，最好成绩约 34%）→ 4.0（2026-08，删除饱和题）；2026-04 起对奖励投机记 0 分
- **τ-bench**：工具加模拟用户的客服 Agent 基准，用 pass^k 指标；gpt-4o 成功率不到 50%；τ²-bench 加入双控环境，2.0 增加六种语言与语音
- **污染与饱和**：canary 字符串、加密分发、私有测试集、重写同分布新题（GSM1k：最多掉 8%）、奖励投机检测、持续维护
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
