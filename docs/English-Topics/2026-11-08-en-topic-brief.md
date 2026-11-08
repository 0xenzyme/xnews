---
title: 2026-11-08-X英文热点选题简报
headline: Claude 记忆 · MaxxBench · AI 破旧 RSA
type: x-en-topic-brief
date: 2026-11-08
tags: [x-en-topic-brief, ai, anthropic, agent-memory, maxxbench, deepmind, rsa, biobasicsbench, fmf, meta-muse, openai-dots]
source: x.com + anthropic.com/research/components-of-agent-memory / openai.com/index/measuring-how-ai-agents-handle-wet-lab-science / frontiermodelforum.org
window: 2026-11-06 08:00 至 2026-11-08 08:00
generated: 2026-11-08T08:30:00+08:00
coverage: partial
---
# X 英文热点选题简报（2026-11-08）

给写英文帖 / newsletter 的选题：本期偏「agent 记忆 + 评测可信度 + AI 做安全研究」。11/07 已写内容本日不重开。

## 今日必读

1. **Anthropic agent 记忆与 dreaming**（见 Daily 1）。本窗口收藏最多的帖子，适合 EN「how to design agent memory」长线程。状态：可起草；官方 verified。

2. **MaxxBench**（见 Daily 3）。EN 圈热议的榜单过拟合话题，Lucas Beyer 等人点赞。状态：可起草；author-claim。

3. **DeepMind RSA-1024 + OpenAI BioBasicsBench**（见 Daily 4、5）。「AI 加速科研 / 安全研究」双案例，务必写清只影响旧 1024 位密钥、Astra 仍不可靠。状态：可起草；均官方 verified。

## 更多话题

### 1. Anthropic: components of agent memory

- 原帖与热度：[AnthropicAI](https://x.com/AnthropicAI/status/2118814753154064501)｜约 154 万、10,881 收藏
- 内容与关注点：dreaming 校对笔记；wiki 表示；顶层预加载要小
- 为什么值得做／可写角度：EN「memory design checklist」
- 时效与核验：verified

### 2. MaxxBench

- 原帖与热度：[loresjpg](https://x.com/loresjpg/status/2118880329490637049)｜约 39.6 万
- 内容与关注点：89 道 DeepSWE 微改题；74% 并列拉开 23pp
- 为什么值得做／可写角度：「怎么给自己的 agent 做抗过拟合评测」
- 时效与核验：author-claim

### 3. DeepMind AI cryptanalysis

- 原帖与热度：[GoogleDeepMind](https://x.com/GoogleDeepMind/status/2118755418675765656)｜约 12 万；[pushmeet](https://x.com/pushmeet/status/2118752095859794390)
- 内容与关注点：padding 失效阈值；批量分解每把密钥成本降约 30 倍
- 为什么值得做／可写角度：「该淘汰 RSA-1024 了」安全提醒
- 时效与核验：verified；2048 位不受影响

### 4. BioBasicsBench + FMF 越狱分级

- 原帖与热度：[OpenAI](https://x.com/OpenAI/status/2118782708767965238)｜约 77.6 万；[FMF](https://x.com/OpenAI/status/2118795218099253606)｜约 32 万
- 内容与关注点：Astra 66.7%；原始实验数据；越狱严重度打分
- 为什么值得做／可写角度：科研 agent 评测怎么设计
- 时效与核验：verified；OpenAI 自测

### 5. 旁注：Dots 代收 2FA 验证码

- 原帖与热度：[alexmichael](https://x.com/alexmichael/status/2119150386082636039)｜热度低
- 内容与关注点：经批准后从邮箱读取一次性验证码
- 为什么值得做／可写角度：agent 与 2FA 的安全边界
- 时效与核验：unverified，无官方来源
