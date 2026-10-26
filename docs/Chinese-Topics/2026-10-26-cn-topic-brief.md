---
title: 2026-10-26-X中文热点选题简报
headline: Nanbeige 开源教师 · 拆 subagent · Claude 用量暴涨
type: x-cn-topic-brief
date: 2026-10-26
tags: [x-cn-topic-brief, ai, nanbeige, anthropic, openrouter, agents, codex, security]
source: x.com
window: 2026-10-24 00:00 至 2026-10-26 08:00
generated: 2026-10-26T08:08:00+08:00
coverage: partial
---
# X 中文热点选题简报（2026-10-26）

给中文作者的选题单：优先可写、可核验、对 builder 有动作空间。热度取自可见原帖 metrics。昨日 Kimi / 离线训练 / Mythos / 价战 / Claude Code 离职线本日不重开；主线改写「国产 30B 开源教师 + 单 agent 架构回摆 + Claude 用量暴涨 + Downloads 指令劫持」。

## 今日必读

1. **Nanbeige4.3-33B 开源**（见第 1 条）。智联招聘侧实验室补上 ~30B agent 编程教师档。形式：与 Qwen3.8-27B / 本地 24GB 跑通对照表。状态：可起草；官方 verified，榜分为实验室自测。

2. **Anthropic「拆 subagent」× OpenRouter Claude 3.6×**（见第 2、3 条）。架构简化遇上真实烧 token——中文缺「org-chart agent 该不该砍」的硬核读。形式：迁移清单 + 路由用量图解。状态：可起草；指南与 OpenRouter 数据 verified。

3. **AGENTS.md Downloads 劫持**（见第 5 条）。给国内 Claude Code / Codex 重度用户的安全硬规则。形式：一页 checklist。状态：可起草；Forever Security 为 author-claim，多源转述一致。

## 更多话题

### 1. Nanbeige4.3-33B：国产 ~30B 开源 agent 教师

- 原帖与热度：[nanbeige](https://x.com/nanbeige/status/2114328933181333798)｜约 31.1 万浏览、2335 赞；HF https://huggingface.co/Nanbeige/Nanbeige4.3-33B
- 内容与关注点：Apache 2.0、先教师后 3B 蒸馏、agentic coding/cowork、可接主流 harness
- 为什么值得做／可写角度：一张「本地可跑的 coding 教师」选型表——参数、显存、许可证、是否独立复核
- 时效与核验：verified — 官方；细分数 author-claim

### 2. Anthropic：多余 subagent 折回主循环

- 原帖与热度：[cherry_mx_reds](https://x.com/cherry_mx_reds/status/2113969070118666670)｜约 83 万浏览、3401 赞；指南 https://claude.com/resources/articles/building-agents-when-to-fold-subagents-into-your-main-agent-loop
- 内容与关注点：skills / tools / subagents 三分法、客户约 2× 加速、progressive disclosure
- 为什么值得做／可写角度：给中文 agent 团队写「删比加难」审计模板——handoff 延迟与 token 账单
- 时效与核验：verified — Anthropic 官方文

### 3. OpenRouter：Claude 5.5 系 token 约 3.6×

- 原帖与热度：[PeterJ_Walker](https://x.com/PeterJ_Walker/status/2114377706603429899)｜约 16.3 万浏览、630 赞
- 内容与关注点：7 日均自 Opus 5.5 起涨 3.6×；Sonnet/Haiku 同步；多为净增
- 为什么值得做／可写角度：对照「中文开源靠低价霸榜 token」叙事——闭源也能用价质表抢量
- 时效与核验：verified — OpenRouter 数据帖

### 4. Codex Day 20：又一天 Rest and reset

- 原帖与热度：[Day 20](https://x.com/thsottiaux/status/2114200152701575656)｜约 123 万浏览、1.12 万赞；[Dots 招人](https://x.com/thsottiaux/status/2114074885622501706)｜约 187 万浏览
- 内容与关注点：午夜 PST 前重置；剩余 8 天猜测；Dots 扩到 10 亿用户招人
- 为什么值得做／可写角度：给重度用户写「额度日历」；别把 reset 写成停更
- 时效与核验：verified — Tibo

### 5. Downloads 里的恶意 AGENTS.md

- 原帖与热度：[choblin29](https://x.com/choblin29/status/2114455243664810172) 等转述｜单帖热度中等但多源一致
- 内容与关注点：网页可写 Downloads；Codex 复现 >90%、Claude Code ~50%；改全局 MCP / OAuth
- 为什么值得做／可写角度：中文安全短帖——「永远别在下载目录启 agent」+ 配置审计命令
- 时效与核验：author-claim — Forever Security；待原报告与厂商回应

### 6. 可选：Thorsten Ball《How I work with Agents》

- 原帖与热度：[thorstenball](https://x.com/thorstenball/status/2114386050638336082)｜约 18.4 万浏览、2366 赞、4933 书签
- 内容与关注点：Amp 作者实践：前沿模型、结果导向 prompt、全可见日志
- 为什么值得做／可写角度：翻译/摘录给中文工程团队的「少步骤、多验证」心法
- 时效与核验：verified — 当事人长文
