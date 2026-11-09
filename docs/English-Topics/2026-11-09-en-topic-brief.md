---
title: 2026-11-09-X英文热点选题简报
headline: Harness 评测 · METR 加速报告 · AI 证明量子猜想
type: x-en-topic-brief
date: 2026-11-09
tags: [x-en-topic-brief, ai, harness, garry-tan, harness-leaderboard, metr, anthropic, psi, aaronson-ambainis, deepmind, arete-27b, openai]
source: x.com + metr.org / psi.inc / nousresearch.com/arete / huggingface.co/spaces/joelniklaus/harness-leaderboard
window: 2026-11-07 08:00 至 2026-11-09 08:00
generated: 2026-11-09T08:30:00+08:00
coverage: partial
---
# X 英文热点选题简报（2026-11-09）

给写英文帖 / newsletter 的选题：本期偏「agent 外壳怎么选 + AI 加速研发与科研」。11/08 已写内容本日不重开；METR、PSI、Arete 为 11/05–11/06 发布、本周末仍在发酵的补录。

## 今日必读

1. **Harness 之争**（见 Daily 1）。Garry Tan 的前沿模型对比（71–79% 挤在一起）对照 Niklaus 的开源模型排行榜（24 个点差距），EN 圈正在吵「harness 还重不重要」。状态：可起草；均 author-claim。

2. **METR × Anthropic「约 2 倍加速」**（见 Daily 6）。EN 圈本周末讨论焦点是「被涂黑的证据」。适合写「What METR can and can't tell us」。状态：可起草；报告 verified，证据受限。

3. **PSI 用 AI 证明 Aaronson–Ambainis**（见 Daily 4）。Lean 验证 + 全部开源，适合配合 DeepMind Pushmeet 的「科学相变」预告写「AI for science 周报」。状态：可起草；verified，等价性待复核。

## 更多话题

### 1. Garry Tan harness evals

- 原帖与热度：[garrytan](https://x.com/garrytan/status/2119492448200405110)｜约 5.5 万、91 回复；跟帖 [0xDevShah](https://x.com/0xDevShah/status/2119511261478277380) 认为「harness 工程已到天花板」
- 内容与关注点：14/20 题全组合同分；成本 $0.19–$0.44/题；Codex on Sol 最快
- 为什么值得做／可写角度：「cost per solved task」比通过率更值得看
- 时效与核验：author-claim；Terminal-Bench 重跑待出

### 2. Harness Leaderboard（Joël Niklaus）

- 原帖与热度：[joelniklaus](https://x.com/joelniklaus/status/2118373808692437403)｜约 31.5 万、2,754 收藏
- 内容与关注点：28,849 次试验；mini-swe-agent 51.4%；Pi $0.29/题；OpenCode $3.35/题
- 为什么值得做／可写角度：与 Garry 的结果放一起写「model strength masks harness gaps」
- 时效与核验：author-claim；数据公开在 HF Space

### 3. DeepMind「phase transition」预告

- 原帖与热度：[pushmeet](https://x.com/pushmeet/status/2119373171321196892)｜约 65 万、7,224 赞
- 内容与关注点：未来几周有科学类发布
- 为什么值得做／可写角度：预告型短帖，等发布再展开
- 时效与核验：verified；产品名传闻 unverified

### 4. Arete-27B

- 原帖与热度：[NousResearch](https://x.com/NousResearch/status/2118822925445050435)｜约 223 万、7,669 收藏
- 内容与关注点：约 5,280 万 token SFT；宣传口径 22% → 约 1%；能力基本不变
- 为什么值得做／可写角度：「open weights mean values are editable」
- 时效与核验：verified（权重与数据公开）；评测为 Nous 自建

### 5. OpenAI「Tomorrow.」

- 原帖与热度：[OpenAIDevs](https://x.com/OpenAIDevs/status/2119521359185478140)｜约 47 万
- 内容与关注点：多半是 ModRetro Chromatic 掌机开售；GPT-6.2 Sol 只是传闻
- 为什么值得做／可写角度：今天发布后再写，避免猜测
- 时效与核验：解读 unverified
