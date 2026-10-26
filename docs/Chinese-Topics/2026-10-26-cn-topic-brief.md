---
title: 2026-10-26-X中文热点选题简报
headline: Nanbeige 开源 · Apollo 零回报 · CF 审计 skill
type: x-cn-topic-brief
date: 2026-10-26
tags: [x-cn-topic-brief, ai, nanbeige, anthropic, openrouter, agents, codex, security, apollo, cloudflare, papers]
source: x.com + techcrunch / huggingface / github
window: 2026-10-24 00:00 至 2026-10-26 09:10
generated: 2026-10-26T09:10:00+08:00
coverage: partial
---
# X 中文热点选题简报（2026-10-26）

给中文作者的选题单：优先可写、可核验、对 builder 有动作空间。早间 X 主线保留；午间并入非 X 媒体/开源/论文。昨日 Kimi / 离线训练 / Mythos / 价战 / Claude Code 离职线本日不重开。

## 今日必读

1. **Nanbeige4.3-33B 开源**（见第 1 条）。智联招聘侧实验室补上 ~30B agent 编程教师档。形式：与 Qwen3.8-27B / 本地 24GB 跑通对照表。状态：可起草；官方 verified，榜分为实验室自测。

2. **Anthropic「拆 subagent」× OpenRouter Claude 3.6× × Apollo 零回报**（见第 2–4 条）。架构简化 + 平台烧 token + 非科技报表未兑现——中文缺这一组「用量≠ ROI」对照。形式：迁移清单 + 双轴图（OpenRouter vs S&P 493）。状态：可起草；指南 / OpenRouter / TC 报道 verified。

3. **AGENTS.md 劫持 × Cloudflare security-audit-skill**（见第 5–6 条）。威胁与官方审计样板同窗。形式：一页 checklist + skill 安装短教程。状态：可起草；Forever Security 为 author-claim，CF 仓库 verified。

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

### 4. Apollo：S&P 493「零财务回报」

- 原帖与热度：https://techcrunch.com/2026/10/25/ai-delivers-zero-financial-payoff-to-most-companies-according-to-apollo-economist/｜无 X metrics
- 内容与关注点：去掉七家科技巨头后利润率/人均收入走平；Slok「AI 是计算器、生意是判断」
- 为什么值得做／可写角度：中文采购/投研帖——「平台用量暴涨」vs「客户报表未动」双图
- 时效与核验：verified — TC 报道；方法论为经济学家口径

### 5. Downloads 里的恶意 AGENTS.md

- 原帖与热度：[choblin29](https://x.com/choblin29/status/2114455243664810172) 等转述｜单帖热度中等但多源一致
- 内容与关注点：网页可写 Downloads；Codex 复现 >90%、Claude Code ~50%；改全局 MCP / OAuth
- 为什么值得做／可写角度：中文安全短帖——「永远别在下载目录启 agent」+ 配置审计命令
- 时效与核验：author-claim — Forever Security；待原报告与厂商回应

### 6. Cloudflare security-audit-skill

- 原帖与热度：https://github.com/cloudflare/security-audit-skill ｜ https://blog.cloudflare.com/build-your-own-vulnerability-harness/｜无 X metrics
- 内容与关注点：六阶段审计、`confirmed`/`needs_validation`、发现者≠验证者、需 OS 沙箱
- 为什么值得做／可写角度：中文「如何用 skill 做可验证安全审计」安装+纪律帖；对标 AGENTS.md 威胁
- 时效与核验：verified — Cloudflare 官方

### 7. Naive RAG 论文 + IQuest-Q1（可选）

- 原帖与热度：https://arxiv.org/abs/2610.30755 ｜ https://arxiv.org/abs/2610.30949｜无 X metrics
- 内容与关注点：Raw-RAG 六胜七场；320B/15B MoE CLI agent 基础模型开源声明
- 为什么值得做／可写角度：与「拆 subagent」同写「删 memory 复杂性」；IQuest 等权重落地再深挖
- 时效与核验：论文页 verified；分数与开源落地为 author-claim

### 8. Codex Day 20 / Thorsten Ball（低优先保留）

- 原帖与热度：[Day 20](https://x.com/thsottiaux/status/2114200152701575656)；[thorstenball](https://x.com/thorstenball/status/2114386050638336082)
- 内容与关注点：额度重置；Amp 作者实践长文
- 为什么值得做／可写角度：额度日历 / 工程心法摘录
- 时效与核验：verified — 当事人
