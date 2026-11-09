---
title: 2026-11-09-X中文热点选题简报
headline: DeepSeek Harness 154 万日活 · 开源支出 89% 归中国模型 · Arete 去审查
type: x-cn-topic-brief
date: 2026-11-09
tags: [x-cn-topic-brief, ai, deepseek-harness, menlo-ventures, kimi, arete-27b, qwen, harness-leaderboard, bla]
source: x.com + menlovc.com/perspective/2026-the-state-of-enterprise-ai / nousresearch.com/arete / huggingface.co/spaces/joelniklaus/harness-leaderboard
window: 2026-11-07 08:00 至 2026-11-09 08:00
generated: 2026-11-09T08:30:00+08:00
coverage: partial
---
# X 中文热点选题简报（2026-11-09）

给中文作者的选题单：周末中文圈的讨论集中在「国产 agent 平台的体量」和「海外怎么用、怎么改中国开源模型」。11/08 已写的 Qwen 4 预热、Qoduck、MaxxBench、Claude 记忆本日不重开。

## 今日必读

1. **DeepSeek Harness 日活 154 万**（见 Daily 第 2 条）。官方长文给出 DAU、日耗 token、插件数和插件作者扶持计划，适合写「一切皆插件的 agent 操作系统」。状态：可起草；官方 verified，DAU 限官方 API 口径。

2. **美国企业开源模型支出 89% 流向中国模型**。Menlo Ventures 11/3 报告周末在中文圈刷屏：Kimi 61%、DeepSeek 15%、GLM 11%、Qwen 3%，Llama 7%；但开源整体只占模型支出约 4%、token 用量约 19%。适合写「用量赢了、钱还没赢」。状态：可起草；报告原文 verified，份额为调查估算。

3. **Arete-27B：Qwen 被「去官方口径」微调**（见 Daily 第 3 条）。与第 2 条放在一起写「中国模型成了海外开源底座，也成了被改造的对象」。状态：可起草；Nous 自建评测，注明出处，避免情绪化表述。

## 更多话题

### 1. DeepSeek Harness 插件生态

- 原帖与热度：[DeepSeekHarness](https://x.com/DeepSeekHarness/status/2119431663642153128)｜约 31 万曝光、3,892 赞、1,709 收藏；中文早期转述 [leo114119](https://x.com/leo114119/status/2118353985317032366)｜约 5,600
- 内容与关注点：8/13 上线 v0.1，9/29 桌面版；154 万 DAU、约 92 万亿 token/日；3.5 万插件，约 60% 活跃用户用过插件；官方插件市场在建
- 为什么值得做／可写角度：盘点文中点名的中文作者插件（创作工作台、设计、上下文可视化、论文阅读）
- 时效与核验：verified；扶持计划细则未公布

### 2. Menlo 报告：开源模型支出

- 原帖与热度：[Frontier_Now_26](https://x.com/Frontier_Now_26/status/2119336437888008365)、[meishengsimon](https://x.com/meishengsimon/status/2119429761764081728) 等转述，单帖热度不高但多账号重复；原文见 [menlovc.com](https://menlovc.com/perspective/2026-the-state-of-enterprise-ai/)
- 内容与关注点：约 400 名美国企业决策者调查（9/8–9/26）；Anthropic 占企业 LLM API 支出 55%
- 为什么值得做／可写角度：「开源用量占 19%、支出只占 4%」的价格逻辑
- 时效与核验：verified（报告原文）；按模型的份额是估算，不是审计数据；Menlo 披露投资了 Anthropic

### 3. Harness 选型：Niklaus 排行榜 + Garry Tan 对比

- 原帖与热度：[joelniklaus](https://x.com/joelniklaus/status/2118373808692437403)｜约 31.5 万；中文转述 [heitieya](https://x.com/heitieya/status/2119295228830248976)｜约 735；[garrytan](https://x.com/garrytan/status/2119492448200405110)｜约 5.5 万
- 内容与关注点：开源模型上外壳差距 24 个点（mini-swe-agent 51.4% vs OpenClaw 27.3%）；Hermes Agent 在 DeepSeek-V4.1-Flash 上最好，Kimi Code 在 Flint 上最好；前沿闭源模型上 7 种组合都在 71–79%
- 为什么值得做／可写角度：「用国产开源模型时该配哪个外壳」实用帖
- 时效与核验：author-claim

### 4. BLA：中国开发者做的反 AI 逆向工具

- 原帖与热度：[xteam3301](https://x.com/xteam3301/status/2119409257628246441)；[xqliu](https://x.com/xqliu/status/2119394753355895093)｜约 450
- 内容与关注点：诱饵密钥、资源陷阱，让逆向 agent 白烧 token；CLI / MCP 双形态
- 为什么值得做／可写角度：独立开发者 + AI 攻防，适合工具介绍
- 时效与核验：author-claim；效果数字为作者自报

### 5. 「IP, PLEASE」：用 Claude 做的抓「偷用 Claude」的游戏

- 原帖与热度：[feishutoday](https://x.com/feishutoday/status/2119545717572391286)｜约 380
- 内容与关注点：借《请出示文件》玩法，讽刺 Anthropic 对中国用户的限制
- 为什么值得做／可写角度：轻松向周末话题
- 时效与核验：unverified（游戏作者与链接未独立核对），热度低，仅作备选
