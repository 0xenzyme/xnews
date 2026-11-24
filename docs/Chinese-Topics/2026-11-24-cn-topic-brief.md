---
title: 2026-11-24-X 中文热点简报
headline: 黄仁勋复职 · 智谱 GLM-5.4 循环架构 · Claude 证明 VP≠VNP
type: x-cn-topic-brief
date: 2026-11-24
tags: [x-cn-topic-brief, ai, nvidia, jensen-huang, megaspeed, zhipu, glm-5.4, loop-transformer, claude, vp-vnp, deepmind, quantum, qoder, hungerg, memos, claude-ship]
source: x.com + nvidianews.nvidia.com / CNBC / Semafor / z.ai / github.com/anthropics/formal-math / deepmind.google
window: 2026-11-23 08:00 至 2026-11-24 08:00（Asia/Shanghai）
generated: 2026-11-24T08:40:00+08:00
coverage: partial
---
# X 中文热点简报（2026-11-24）

中文圈今天三条主线：黄仁勋复职与美股暴涨（「爽剧剧情」类调侃刷屏）、智谱 GLM-5.4 的循环架构与实测，以及 Claude 在黎曼猜想之后又放出 VP ≠ VNP 证明。另有 Qoder 上线匿名「隐身模型」HungerG，适合做「猜猜是谁」类短稿。

## 今日必读

1. **英伟达让黄仁勋复职，股价收涨 31%；Megaspeed 同日被列入实体清单**（见 Daily 第 1 节）。中文角度：董事会声明写明「听取了美国政府高层意见」，特朗普公开说自己介入；同一天把东南亚转运商拉黑。适合写「人回来了，渠道关上了」，对国内拿卡的影响比股价更值得讲。状态：可起草；复职、涨幅、拉黑 verified。

2. **智谱 GLM-5.4：750B、28 层循环两遍的 Loop Transformer**（见 Daily 第 3 节）。中文角度：国产厂商把循环 Transformer 做到旗舰规模，而且是改造已有基座；技术亮点在 KV 设计（多一轮只多一个滑动窗口）。中文 X 上的实测普遍是「强但慢」，3D 体素、鹈鹕骑车等测试要跑一个多小时。目前只开放给 Coding Plan，API 与权重未放。状态：可起草；架构 verified，跑分 author-claim。

3. **Claude 署名的 VP ≠ VNP 证明进入 Anthropic 官方仓库**（见 Daily 第 2 节）。中文角度：解释清楚「代数版 P vs NP」是什么、为什么不等于解决 P vs NP，以及「Lean 通过但无人审阅」意味着什么。中文转述已经出现「47 年悬案被破」的标题，写稿要克制。状态：可起草；仓库内容 verified，定理成立 author-claim。

4. **DeepMind 智能体团队优化量子算法**（见 Daily 第 2 节）。中文角度：中文帖普遍写对了「近 10 倍」口径，但也有把 arcsin 的 290 倍当总体结论的。可与 Claude 证明合写「AI + Lean 做科研」一稿。状态：可起草；verified。

## 更多话题

### 1. Qoder 上线匿名「隐身模型」HungerG，11 月 23–30 日免费

- 原帖与热度：[@qoder_ai_ide 官方帖](https://x.com/qoder_ai_ide/status/2124899980632822148)｜约 122 万曝光、623 赞；[@aitrackerbot 鹈鹕/黑洞测试](https://x.com/aitrackerbot/status/2124954200119631970)｜31 赞
- 内容与关注点：Qoder（阿里系 AI IDE）上线代号 HungerG 的模型，身份保密，Qoder 与 Qoder IDE 免费用 7 天，邀请用户猜开发者。
- 为什么值得做／可写角度：隐身模型常是新模型正式发布前的公测，猜测方向值得跟踪；但不要在没有证据时点名厂商。
- 时效与核验：发布 verified（官方帖）；开发者身份未知，任何猜测都是 unverified。

### 2. MemOS 发布 554B 记忆原生模型 MemT-1.0-Pro

- 原帖与热度：[@MemOS_dev](https://x.com/MemOS_dev/status/2124623963087126562)｜约 125 万曝光、2,838 赞、3,126 收藏
- 内容与关注点：与英伟达合作、基于 Nemotron 3 Ultra，把记忆写进固定大小的参数块。
- 为什么值得做／可写角度：「记忆放在模型里」和 RAG、长上下文的对比，是 agent 开发者关心的话题。
- 时效与核验：发布 verified；权重与跑分本期未核对模型卡，author-claim。

### 3. 「Qwen 核心成员离职、Qwen4 可能不开源」的担忧

- 原帖与热度：[@MiaoHype](https://x.com/MiaoHype/status/2125017050128994498)｜61 曝光、2 赞
- 内容与关注点：中文用户担心阿里通义千问核心人员离开后 Qwen4 不再开源。
- 为什么值得做／可写角度：如果有官方信源，会是国内开源生态的大事。
- 时效与核验：本期没有找到可靠来源，unverified；热度极低，暂不起草。

### 4. Claude Ship 与 Claude Plugins

- 原帖与热度：[@ClaudeDevs](https://x.com/ClaudeDevs/status/2124959436640858475)｜约 119 万曝光、1.38 万赞；[@claudeai Plugins](https://x.com/claudeai/status/2124970294523945328)｜4,480 赞
- 内容与关注点：自动审 PR、修 PR、按策略批准；connectors 与 skills 合并为插件。
- 为什么值得做／可写角度：国内用 Claude Code 接国产模型（如 GLM-5.4）的开发者会关心 /ship 能否在第三方模型下工作，可做实测。
- 时效与核验：verified（官方文章）。
