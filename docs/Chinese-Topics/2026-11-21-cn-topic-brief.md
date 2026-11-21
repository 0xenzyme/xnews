---
title: 2026-11-21-X 中文热点简报
headline: 微信 WeMM 开源 · ANT 次日回落 · 权重取证传开
type: x-cn-topic-brief
date: 2026-11-21
tags: [x-cn-topic-brief, ai, wechat, wemm-video, anthropic, ant, nasdaq, nvidia, checkpoint-forensics, moonshot, deepseek, apple, stepfun]
source: x.com + CNBC / Reuters / openai.com / arxiv.org/abs/2611.26409 / unemploymentlabs.com / TechCrunch
window: 2026-11-20 08:00 至 2026-11-21 08:00（Asia/Shanghai）
generated: 2026-11-21T08:45:00+08:00
coverage: partial
---
# X 中文热点简报（2026-11-21）

给写中文圈的选题单：今天能动手核的头条是微信视觉开源 WeMM-Video，权重、仓库和论文都在。市场侧是 ANT 首个完整交易日回落，并连带英伟达约跌 14% 与尚未被官方确认的会计调查。另外，Unemployment Labs 11 月 12 日的 Checkpoint Forensics 报告这几天在中文圈传开，写的时候必须把方法边界写清楚。

## 今日必读

1. **微信 WeMM-Video 开源：2B 到 35B-A3B，自称接近 Gemini 3.0 Flash**（见 Daily 第 3 节）。官方账号、[论文](https://arxiv.org/abs/2611.26409)、[GitHub](https://github.com/Tencent/WeMM-Video) 和 [HF 合集](https://huggingface.co/collections/tencent/wemm-video) 对得上。适合写成「产品里已经在用的模型，这次把权重和评测链放出来了」，不要只复述开源 SOTA 对比图。状态：可起草；发布 verified，榜单数字 author-claim。

2. **ANT 次日收于 88.91 美元，跌 8.5%；AI 股跟着回调**（见 Daily 第 1 节）。和上期「首日收涨 17.1%」接上写。纳指、标普、道指的收盘点位以 CNBC 为准；英伟达约跌 14% 和 Reuters 的 SEC 会计调查要分开：前者是行情，后者是消息人士转述。状态：可起草；收盘 verified，调查 unverified。

3. **苹果据报要做能操作设备的 agent**（见 Daily 第 4 节）。Gurman 原帖在北京时间 11 月 20 日凌晨，上期未写入。中文稿容易写成「苹果要对标 Claude Code」，更好的角度是招聘启事里的计算机使用权限，以及这对第三方 agent 在 Mac 上的意味。状态：可起草；招聘和报道 verified，发布时间表 unverified。

## 更多话题

### 1. Checkpoint Forensics：11 月 12 日的报告，本周在中文圈传开

- 原帖与热度：[中文解读帖](https://x.com/mylifcc/status/2123597446244712731)｜约 1.2 万曝光、96 赞、77 收藏；原文：[Unemployment Labs，Will DePue，2026-11-12](https://unemploymentlabs.com/checkpoint-forensics)
- 内容与关注点：方法是从已发布权重里尚未被覆盖的 embedding 行，恢复 GPU 随机初始化的痕迹，从而判断初始化时的芯片代际（如 B200/B300 的 148 SM、GB200/GB300 的 152 SM）。报告称 DeepSeek-V4、Kimi K3 / K3.1-Pro、MiniMax-M3、蚂蚁 Ling-3.1-flash 等六个模型读出 Blackwell 指纹，而同实验室更早的模型仍是 Hopper；阿里、智谱、腾讯、小米、阶跃的可读新模型仍是 Hopper。作者自己写明：这证明的是初始化硬件，支持但并不能证明训练也在同一类芯片上完成，也不能说明芯片在哪里、如何获得，或是否违反出口管制。
- 为什么值得做／可写角度：适合当「开源权重里藏着硬件指纹」的方法稿，并把边界写进导语；不要写成「已实锤走私 Blackwell」。上期月之暗面取消印尼租卡的报道，可以作政策背景，不要和这份 11 月 12 日的技术报告揉成同一条突发。
- 时效与核验：报告页面日期为 11 月 12 日 verified，不是今天首发。方法描述与「不证明位置或违法」的限定 verified 为原文。对具体模型的指纹判定是作者结论，author-claim；本期未复现。中文传播把「取证」写成定论的，需要回原文纠偏。

### 2. 阶跃星辰在旧金山放出 Step 5 Preview，互动有限

- 原帖与热度：[官方帖](https://x.com/StepFun_ai/status/2123902251983110204)｜约 622 曝光、13 赞
- 内容与关注点：在 Agent Night Out 上介绍 Step 5 Preview，讨论 agent 跑得更久、更少失败、更便宜；没有权重、基准或上线时间。
- 为什么值得做／可写角度：最多当「预览露脸」的补丁，等可核对的技术博客或 API 再单开；不要写成 Step 5 已发布。
- 时效与核验：活动与「Preview」表述 verified 为官方帖；产品能力 unverified。

### 3. 英伟达据报在中国招 Open Models 产品经理，点名 Qwen / Kimi / MiniMax / StepFun

- 原帖与热度：[中文转述](https://x.com/changchuan888/status/2123716236651708839)｜约 3,530 曝光、6 赞；职业网站条目：[Product Manager - Open Models](https://nvidia.wd5.myworkdayjobs.com/en-US/NVIDIAExternalCareerSite/job/Product-Manager---Open-Models_JR2023506)
- 内容与关注点：转述称岗位地点包括北京、上海或深圳，职责是支持上述中文社区开源模型，而不是英伟达自研开源模型「首次发布」。搜索结果支持该职位存在，但本期未能把 Workday 页面正文完整抓下来核对每一句职责。
- 为什么值得做／可写角度：可写成「英伟达继续把中国开源模型当生态对象」，以职业网站原文为准；「第一次招聘」是转述，不要升格成战略宣布。
- 时效与核验：职位 URL 存在 verified 为搜索可见的官方招聘页；职责细节本期未逐句核对，author-claim。转述中的「第一次」unverified。
