---
title: 2026-11-12-X中文热点选题简报
headline: Qwen4-Max 与文心 5.5 同日亮相 · 百度世界今天开 · 「蒸馏断供」争论
type: x-cn-topic-brief
date: 2026-11-12
tags: [x-cn-topic-brief, ai, qwen4-max, alibaba, ernie-5-5-flash, baidu, baidu-world, distillation, kimi, deepseek, gemini-decision-1, praxis-1, anthropic, amd]
source: x.com + qwencloud.com / blog.google / runway.com/news / alignment.openai.com
window: 2026-11-11 00:00 至 2026-11-12 08:00
generated: 2026-11-12T08:50:00+08:00
coverage: partial
---
# X 中文热点选题简报（2026-11-12）

给中文作者的选题单：中文圈今天的主线是两家国产旗舰同日亮相（Qwen4-Max 预览、文心 5.5 Flash Preview），以及英文圈抛来的「Anthropic 封堵蒸馏后，国产模型是不是停滞了」。今天百度世界大会召开，适合准备跟进稿。中文原生帖整体热度不高，多数讨论是转述官方英文帖。

## 今日必读

1. **Qwen4-Max 预览**（见 Daily 第 1 节）。官方帖约 112 万曝光、1.2 万赞，Token Plan、Qoder、Qwen App 可抢先用。适合写「拿三个真实任务实测 Qwen4-Max」，比结论更有价值的是过程和失败案例。状态：可起草；上线 verified，跑分尚无，「令人失望」的说法是传言。

2. **文心 5.5 Flash Preview + 今天的百度世界**（见 Daily 第 1 节）。280B 总参 / 14B 激活、100 万上下文、11/25 前开源权重。中文帖里的调侃是「百度起了大早赶了晚集」「没人在意文心也发了」。适合写「百度这次靠开源能不能把声量拿回来」，并在大会后补跟进。状态：可起草；参数 verified，大会内容待今天确认。

3. **「蒸馏断供」争论**。@Da7_Tech 称「Anthropic 关上蒸馏的门后，中国模型一寸都没动」（约 46 万曝光、5,972 赞），另一帖自称有中国大厂找他帮忙蒸馏 Fable 被拒（约 21 万曝光），并以 Kimi K3.1 Pro 百天进步不大为例。适合写一篇有数据的反驳或复核：拿公开榜单看国产模型最近三个月到底有没有进步。状态：观点帖，unverified；自称经历无法核实，引用需标注。

## 更多话题

### 1. Qwen4-Max 实测

- 原帖与热度：[Alibaba_Qwen](https://x.com/Alibaba_Qwen/status/2120335993643684315)｜约 112 万曝光、11,779 赞、1,490 收藏；[UnslothAI](https://x.com/UnslothAI/status/2120342367932981581)｜约 6.3 万曝光
- 内容与关注点：主打复杂编码、知识工作、前端和专业软件流程；Unsloth 表态要做量化
- 为什么值得做／可写角度：前端/全栈 demo 对比 Gemini 4 Carbon、Fable 5.2
- 时效与核验：今天就能写；官方帖 verified，上下文长度等细节 unverified

### 2. 文心 5.5 Flash 与百度世界

- 原帖与热度：[Baidu_Inc](https://x.com/Baidu_Inc/status/2120391732248637734)｜约 18 万曝光、1,356 赞；中文吐槽帖 [JangXiin](https://x.com/JangXiin/status/2120402556643844343)｜约 2,300 曝光
- 内容与关注点：14B 激活的部署成本、11/25 开源时间、千帆 API 是否打折
- 为什么值得做／可写角度：大会直播跟进；「国产开源 MoE 选型表」
- 时效与核验：参数 verified；benchmark 分数、OpenRouter 免费为转述，unverified

### 3. 蒸馏与国产模型节奏

- 原帖与热度：[Da7_Tech](https://x.com/Da7_Tech/status/2120502872051720453)｜约 46 万曝光；[Da7_Tech 长帖](https://x.com/Da7_Tech/status/2120540672696451162)｜约 21 万曝光、1,643 赞；[kimmonismus](https://x.com/kimmonismus/status/2120461099745096146)｜约 5.5 万曝光
- 内容与关注点：英文圈把 Qwen4 传言、Kimi K3.1 Pro、DeepSeek 节奏串成「停滞」叙事
- 为什么值得做／可写角度：用 Artificial Analysis、LMArena 等公开数据做时间线复核
- 时效与核验：观点为主，unverified；写作时避免把指控当事实

### 4. Gemini Decision 1 的中文转述

- 原帖与热度：[OfficialLoganK](https://x.com/OfficialLoganK/status/2120581433639198885)｜约 41 万曝光、7,599 赞；中文转述 [xiaoanlab](https://x.com/xiaoanlab/status/2120655309253304605)｜热度低
- 内容与关注点：「只做选择题的模型」，每百万输入 0.1 美元、输出免费、150–250 毫秒
- 为什么值得做／可写角度：给国内 agent 开发者讲「路由和审核为什么不该用生成模型」
- 时效与核验：verified（官方博客）

### 5. Runway Praxis-1 与 Claude 三天上 AMD

- 原帖与热度：[runwayml](https://x.com/runwayml/status/2120533081182577116)｜约 4.8 万曝光；[AndrewCurran_](https://x.com/AndrewCurran_/status/2120323074860179674)｜约 21 万曝光
- 内容与关注点：Praxis-1 文本编码器用 Qwen3.5-2B，Apache 2.0 可商用；Anthropic 称 Mythos 三天把 Claude 移植到 AMD
- 为什么值得做／可写角度：「美国开源机器人模型里的中国开源部件」；「模型自己写 kernel，对国产芯片意味着什么」
- 时效与核验：Praxis-1 verified；AMD 三天为 Anthropic 自述，author-claim
