---
title: 2026-11-27-X 中文热点简报
headline: GLM-5.5 与 K4 或延期 · 腾讯开源 DFly2 · 方言语音上新
type: x-cn-topic-brief
date: 2026-11-27
tags: [x-cn-topic-brief, ai, glm-5.5, kimi-k4, moonshot, zhipu, distillation, export-controls, nvidia, tencent, dfly2, hy4-flash, ant-group, ming-image, qwen-audio, gigachat-4, sensetime, robotics, lingbot-navi]
source: x.com（中文讨论帖；官方帖 @TencentHunyuan、@TencentAI_News、@AntLingAGI、@Alibaba_Qwen、@robbyant_brain；路透、FT 经 X 转述）
window: 2026-11-26 08:00 至 2026-11-27 08:00（Asia/Shanghai；美国感恩节，美方官方发布偏少）
generated: 2026-11-27T08:40:00+08:00
coverage: partial
---
# X 中文热点简报（2026-11-27）

今天中文 X 的主线是「卡」：路透称算力新规加反蒸馏可能让 GLM-5.5、Kimi K4 推迟到 2027 年，配合一张流传很广的「各家 H100 数量」对比图，讨论几乎一边倒地看空月之暗面。另一边，国内大厂当天开源的都是「省卡」和「垂直能力」：腾讯 DFly2 推测解码、蚂蚁设计向文生图、千问方言语音。中文原创帖整体互动仍偏低。

## 今日必读

1. **GLM-5.5、Kimi K4 或推迟：算力新规与反蒸馏两面夹击**（见 Daily 第 3 节）。中文角度：[@bboczeng](https://x.com/bboczeng/status/2125888806939463769)（约 7.5 万曝光、442 赞）和 [@NFT_Chen](https://x.com/NFT_Chen/status/2125907314574344382) 转述路透：GLM-5.5 约 3 万亿参数，或推迟到 2027 年一季度以后；Kimi K4 或拖到 2027 年年中，月之暗面转向蒸馏 Google、Meta 模型并去欧洲找算力。[@oldfrog123](https://x.com/oldfrog123/status/2125872600786379171)（约 17.9 万曝光、758 赞）流传的卡数对比称 Kimi 仅约 4.5 万张 H100、为国内最少，并称 11 月取消了一项 1.5 亿美元海外算力租赁。热度：本窗口中文 AI 帖最高。状态：可起草；路透为匿名信源（unverified），卡数和租约为个人帖，未见出处（unverified）。

2. **腾讯开源 DFly2，Hy4 flash 在 opencode 上日跑 10T token**（见 Daily 第 2 节）。中文角度：推测解码直接读目标模型的 KV 缓存，对 DeepSeek-V4.1-Flash 吞吐最高提升 81%；混元同日称 Hy4 flash 在 opencode 上每天消耗 10T token（[@TencentHunyuan](https://x.com/TencentHunyuan/status/2125979836170842187)）。热度：官方英文帖 约 9 万曝光、1,426 赞、847 收藏。状态：可起草；开源 verified，加速数据和 10T 为 author-claim。

3. **模态侧开源：蚂蚁 Ming-Image-0.2-Design 与 Qwen-Audio-3.1 方言**（见 Daily 第 2 节）。中文角度：Ming 主打海报和带可读文字的产品图，分层版下周开源；Qwen-Audio 支持 8 种汉语方言识别、6 种方言合成。热度：约 12.1 万曝光、1,155 赞、523 收藏（Qwen）。状态：可起草；权重 verified，排名和语种数为 author-claim。

## 更多话题

- **俄罗斯 GigaChat 4：「三足鼎立」？** 中文帖把 Sber 708B 开源称为中美之外的第三极（[@heRiverYY](https://x.com/heRiverYY/status/2125998020668080422)）。角度：Sber 的对比对象主要是中国开源模型。热度：低。核验：HF 上架 verified，跑分 author-claim。
- **东南亚停货谁最受伤**：有帖子称字节、月之暗面受影响最大（[@ileoyeye](https://x.com/ileoyeye/status/2125970098691400169)）。热度：低。核验：个人分析，unverified。
- **国模口碑**：有中文帖调侃一轮发布后「口碑最高的仍是 DeepSeek V4.1 Flash」（[@xingzengji](https://x.com/xingzengji/status/2125892569217503390)）。热度：低。核验：主观评价，不作事实引用。
- **具身智能开源**：商汤 SenseNova-RoboRSI-27B（Apache 2.0）称只用仿真后训练就部署到真机，RoboDojo 34.7 分；蚂蚁灵波 LingBot-Navi 开源，导航时复用跨任务的 3D 空间记忆（[@robbyant_brain](https://x.com/robbyant_brain/status/2126020732610302086)，约 11.2 万曝光、61 赞）。热度：低到中。核验：均为 author-claim。
