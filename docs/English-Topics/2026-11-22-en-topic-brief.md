---
title: 2026-11-22-X 英文热点简报
headline: 黎曼猜想获认证 · NS 爆破待验 · OpenRouter 隐私警告
type: x-en-topic-brief
date: 2026-11-22
tags: [x-en-topic-brief, ai, riemann-hypothesis, navier-stokes, claude, lean, gowers, openrouter, minimax, privacy, inkling, thinking-machines, anthropic, pentagon, oracle, openai, nvidia, gemini, antigravity, chatgpt]
source: x.com + alpo.ge / Lean 社区博客 / Scientific American / GitHub / Groundy / The Next Web / thinkingmachines.ai / Novita / Privacy Affairs / CNBC / oracle.com / Bloomberg
window: 2026-11-21 08:00 至 2026-11-22 08:00（Asia/Shanghai），含 11 月 20 日补录
generated: 2026-11-22T08:40:00+08:00
coverage: partial
---
# X 英文热点简报（2026-11-22）

英文圈周六几乎被数学刷屏：黎曼猜想的证明拿到 Lean 社区认证，Navier–Stokes 的爆破论文紧随其后但尚待验证。开发者侧是 OpenRouter 的 MiniMax 隐私邮件。Thinking Machines 的 Inkling 2 Mini 是上期漏掉的模型新闻。

## 今日必读

1. **黎曼猜想证明获 Lean / Mathlib 联合声明认证**（见 Daily 第 1 节）。英文稿的重点是认证流程本身：命题比对、复现编译、多个独立检查器，而不是「AI 解决了数学」。Gowers 一边祝贺，一边当天去参加 PauseAI 游行，可以作为人物侧写。状态：可起草；形式化结论 verified，Claude 的贡献 author-claim。

2. **Navier–Stokes 有限时间爆破：论文与 Lean 形式化已公开，数值证书未公开**（见 Daily 第 1 节）。标题要写「声称」，并说明只能验证形式化那一层。Tao 的评价目前只有媒体转述。状态：可起草，但需标明 unverified。

3. **OpenRouter：发往 MiniMax 的请求可能被第三方读取**（见 Daily 第 3 节）。英文开发者的关注点是 ZDR 标签和「美国托管」承诺在聚合层下是否可信。写清时间段、涉及的三家托管商，以及「轮换密钥」的建议。状态：可起草；Novita 确认 verified，OpenRouter 邮件 author-claim。

4. **Inkling 2 Mini：26.4B 循环 Transformer，可在笔记本上运行**（见 Daily 第 2 节）。角度是循环架构与思维链可监控性的权衡，Murati 的原话可以直接引用。状态：可起草；规格 verified，基准 author-claim。

## 更多话题

### 1. 五角大楼再称 Anthropic「肯定是供应链风险」

- 原帖与热度：[@Polymarket](https://x.com/Polymarket/status/2123825006345945592)｜约 24.6 万曝光、4,908 赞；原文：[CNBC 采访视频](https://www.cnbc.com/video/2026/11/20/watch-cnbcs-full-interview-with-the-pentagons-emil-michael.html)
- 内容与关注点：五角大楼技术主管 Emil Michael 11 月 20 日在 CNBC 表示，Claude 的使用条款禁止战场管理和武器开发等用途，因此 Anthropic 仍是供应链风险。发生在 ANT 首个完整交易日下跌 8.5% 的同一天（上期已报行情）。
- 为什么值得做／可写角度：上市公司 Anthropic 的使用政策与国防市场的冲突。不要把股价下跌全部归因于这次采访。
- 时效与核验：采访 verified（CNBC 视频）；「导致股价下跌」是部分报道的推断，unverified。

### 2. Oracle 抢在媒体报道前声明：OpenAI 合同所需资金已全部到位

- 原帖与热度：[@Oracle](https://x.com/Oracle/status/2123884437045760420)｜约 248 万曝光、5,186 赞、1,331 收藏；原文：[Oracle 声明](https://www.oracle.com/news/announcement/oracle-statement-2026-11-20/)
- 内容与关注点：Oracle 称完成本月初最后一轮融资后，履行 OpenAI 合同所需资金已全部筹齐，是本轮投资周期第一家资金完全到位的云厂商，且交付能力不依赖进一步的供应商融资谈判。
- 为什么值得做／可写角度：AI 基础设施融资压力的信号。一家公司主动「预先辟谣」，本身就说明市场在担心什么。
- 时效与核验：声明 verified；资金是否真正充足是公司说法，author-claim。

### 3. Google 重置 Antigravity 上所有人的 Gemini 配额，缓存改进让同等配额多做 22% 的工作

- 原帖与热度：[@_mohansolo（Varun Mohan）](https://x.com/_mohansolo/status/2124070033534161407)｜约 82 万曝光、11,844 赞
- 内容与关注点：周末鼓励开发者用 Gemini 4 Neon 构建；Simon Willison 另发帖提醒，Gemini 4 Hydrogen 的 high 与 xhigh 推理档效果差别很大。
- 为什么值得做／可写角度：可作为编码工具价格战的短讯。
- 时效与核验：配额重置是官方人员发帖，verified；「多 22%」是公司说法，author-claim。

### 4. ChatGPT 的 Space 功能向 Plus 用户开放

- 原帖与热度：[@ChatGPT 官方帖](https://x.com/chatgpt/status/2123850912867471807)；[@testingcatalog](https://x.com/testingcatalog/status/2123938809113137280)｜约 4.3 万曝光、797 赞
- 内容与关注点：可与他人和 ChatGPT 协作制作交互页面、幻灯片和网站，支持移动端编辑。
- 为什么值得做／可写角度：短讯即可。
- 时效与核验：官方帖 verified；本期未取得官方帖互动数据。

### 5. 作家群体：Anthropic 员工已在 IPO 中套现，15 亿美元版权和解款却还没付

- 原帖与热度：[@KBAndersen](https://x.com/KBAndersen/status/2124154059288613171)｜约 7.1 万曝光、2,962 赞
- 内容与关注点：2025 年 8 月的和解约定每本书约 3,000 美元，帖子称至今未付款，并主张按 Anthropic 现在的市值提高赔偿。
- 为什么值得做／可写角度：上市后的声誉议题；需要找法院或和解管理方的付款时间表。
- 时效与核验：和解金额 verified 为公开信息；「一分钱都没付」是作者说法，本期未核实付款进度，author-claim。
