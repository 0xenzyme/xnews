---
title: 2026-11-23-X 中文热点简报
headline: 蚂蚁开源医疗大模型 · 国家数据局管词元计费 · 芯片流入中国获证实
type: x-cn-topic-brief
date: 2026-11-23
tags: [x-cn-topic-brief, ai, ant-group, lingsante, medical-ai, token-factory, national-data-administration, nvidia, export-controls, kimi, semianalysis, rubin, muxi, hy4, zhipu, minimax, doubao]
source: x.com + huggingface.co / 第一财经 / The Next Web / Semafor / OpenAI 官网
window: 2026-11-22 08:00 至 2026-11-23 08:00（Asia/Shanghai）
generated: 2026-11-23T08:30:00+08:00
coverage: partial
---
# X 中文热点简报（2026-11-23）

周日中文圈没有新的大模型发布，讨论集中在三处：蚂蚁开源的医疗大模型、国家数据局要给「词元」定计费标准，以及美国情报总监证实管制芯片流入中国。另有两条适合做技术稿的线索：SemiAnalysis 用 Kimi K3.1 Pro 测英伟达 Rubin，以及国产 GPU 的「Day 0 适配」。

## 今日必读

1. **蚂蚁 inclusionAI 开源 LingSante-3.1-flash：560B / 25B 激活、MIT 许可的医疗模型**（见 Daily 第 2 节）。中文角度：国内大厂在垂直领域开源旗舰规模模型，许可比多数通用模型更宽松；可对照国内医疗 AI 的监管要求写「能下载 ≠ 能上临床」。状态：可起草；权重与许可 verified，领先成绩 author-claim。

2. **国家数据局：健全词元计量计费、质量测评标准，避免「低质量重复建设」**（见 Daily 第 3 节）。中文角度：词元工厂在各地铺开，计费口径统一后，推理 token、缓存 token 怎么算会直接影响价格战。X 上的英文讨论多在调侃「token 账单」，中文稿可以讲清楚已立项的计数规则国家标准。状态：可起草；讲话 verified，token 用量数字 author-claim。

3. **美国情报总监 Clayton：中国「接触到了」受管制的英伟达芯片；Bessent 为对华销售辩护**（见 Daily 第 3 节）。中文角度：接上周的 87.9 万颗审批数据与黄仁勋事件，美方内部对出口管制的说法并不一致。适合写「华盛顿两种声音」，不要写成「美国承认中国突破封锁」。状态：可起草；原话 verified，「7,000–22,000 张 Blackwell」unverified。

4. **OpenAI 公开内部预训练困惑度，提议行业「共同上限」**（见 Daily 第 1 节）。中文角度：国产模型厂商会不会跟进公开同口径数字？这关系到中国实验室能否进入任何将来的「共同上限」框架。状态：可起草；verified。

## 更多话题

### 1. SemiAnalysis：Kimi K3.1 Pro 在 Vera Rubin NVL72 上每美元 token 产出为 GB300 的 1.82–6.67 倍

- 原帖与热度：[@AIQuanting 的拆解](https://x.com/AIQuanting/status/2124641617093284150)｜96 曝光；[@ChuckBass8808 中文转述](https://x.com/ChuckBass8808/status/2124648515796381783)｜250 曝光、7 赞
- 内容与关注点：测试回放真实 Claude Code 会话，按持有成本计每美元服务 token 数。拆解帖指出：GB300 用 vLLM 时表现好得多，6.67 倍里大部分来自 GB300 的 SGLang 配置，同速下 Rubin 领先约 2 倍。
- 为什么值得做／可写角度：中国 2.8T 开源模型被拿来当英伟达新架构的基准负载，本身就是信号。
- 时效与核验：只有二手转述，未读到 SemiAnalysis 原图，unverified；热度很低。

### 2. 沐曦称已为 52 个主流模型做过「Day 0 适配」，Hy4 是最新一个

- 原帖与热度：[@ofrbkj](https://x.com/ofrbkj/status/2124419567304982964)｜407 曝光、9 赞
- 内容与关注点：腾讯 Hy4 发布当天，沐曦宣布曦云 C 系列完成适配；帖子指出这不是第一次，沐曦自称自 2025 年 12 月起已适配 52 个模型。
- 为什么值得做／可写角度：配合 Clayton 的表态，写「国产算力适配速度」比写「芯片走私」更有建设性。
- 时效与核验：数字来自沐曦自述（经转述），author-claim。

### 3. 国产 AI 应用月活与上市公司亏损：豆包 4.19 亿、智谱与 MiniMax 上半年各亏约 19.6 亿

- 原帖与热度：[@YxzRainy 月活榜](https://x.com/YxzRainy/status/2124307625362034935)｜约 5,300 曝光、72 赞；[@ileoyeye 财务对比](https://x.com/ileoyeye/status/2124334765486821604)｜约 1.7 万曝光、34 赞
- 内容与关注点：Anthropic 上市与黎曼猜想之后，中文圈在对比国产模型公司的财务压力。
- 为什么值得做／可写角度：可做「烧钱与开源」专题，但需要先找财报原文。
- 时效与核验：月活与财务数字均未注明来源，unverified，不宜直接引用。

### 4. 豆包工作、千问办公接入多家模型，WorkBuddy 的多模型优势被追平

- 原帖与热度：[@WangNextDoor2](https://x.com/WangNextDoor2/status/2124458872454647819)｜约 1,400 曝光、5 赞
- 内容与关注点：11 月 12 日豆包工作开放 Kimi、GLM、DeepSeek，几天后千问办公接入十款模型；有用户反馈同一模型在豆包工作里更慢。
- 为什么值得做／可写角度：国产办公 agent 平台从「拼自家模型」转向「拼模型超市」。
- 时效与核验：产品接入情况需到官方页面确认，本期 unverified；用户体验为个人反馈。
