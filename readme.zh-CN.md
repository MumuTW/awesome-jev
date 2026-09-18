# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**语言：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md)

> 精选、高信号的 [Jev](https://typesafe.ai) 相关项目 — TypeSafe AI 的 System One 模型，返回带置信度的 typed 决策（choice / score / boolean）。

## 这份清单的差异化

市面上已有以**广度**为主的目录（[awesomejev.com](https://awesomejev.com/)、[yibie/awesome-jev](https://github.com/yibie/awesome-jev)、[AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)）。我们做的是**判断**。

| 常见做法 | 我们的做法 |
| --- | --- |
| 扫街／镜像几百个 repo | 短清单，一次能读完 |
| 营销式一行介绍 | **评语**：为什么值得看、限制、适合谁 |
| 用星数当排序 | **社区基础研究**：可测量循环、launch 讨论（尤其 X）、大家真正在转述的 pattern |
| 每个 fork 一视同仁 | 每类 pattern 优先 best-in-class；薄包装 Ultrafast 先跳过 |

向这些清单借鉴（再改成我们的口味）：

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome)／[awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — 策展不是收集；门槛高；要说清楚 *为什么* awesome。
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — 范围清楚，诚实标「不收／另页」（我们的 [开源复制品](#开源复制品非-jev)、「暂不收录」）。
- 多语 README 惯例 — 英文为 OSS 发现用正本；繁体／简体是一等公民镜像。

## 目录

- [怎么筛](#怎么筛)
- [观察](#观察)
- [官方](#官方)
- [平台](#平台)
- [浏览器与电脑操作](#浏览器与电脑操作)
- [代码代理](#代码代理)
- [路由器](#路由器)
- [数据与库](#数据与库)
- [值得研究的 Demo](#值得研究的-demo)
- [开源复制品（非 Jev）](#开源复制品非-jev)
- [相关清单](#相关清单)
- [贡献](#贡献)

## 怎么筛

至少满足以下 **两项** 才收：

1. 真正调用 TypeSafe／Jev API（或官方文档／SDK），不是同名撞车。
2. 这周就能偷师或上线的 pattern（成本、延迟、action space、routing、review）。
3. 有公开讨论，不只安静 README（launch 串、成本／延迟数字、被别人引用）。

不收：大杂烩目录、没有决策循环的改名 clone、从不调用 Jev 的「inspired by」（若有教学价值，只放 [开源复制品](#开源复制品非-jev)）。

若与已收录项目类似，PR 里要说明 **为什么更好** — 成熟 awesome list 的同一条规矩。

## 观察

- **Action space 有限且可观测时，Jev 才赢。** 在 X 上打出声量的（Browser Use 机票 demo、Mac computer-use 成本表）都是把世界收成索引表，再一次并行问 Jev。开放式「随便做」代理不适合。
- **小 LLM 只负责产文字。** Ultrafast 与 computer-use 都把 `TYPE_TEXT`／打字留给文字模型。常见架构是分工，不是「整颗代理换成 Jev」。
- **写代码代理的用法在闸门，不在写作。** Compaction、review、工具放行／拒绝、模型路由，才是 System One 的主场。预期会看到更多 MCP／skill，而不是整颗 coding agent 重写。
- **延迟叙事比星数更会传。** ~7 秒／~$0.004 机票、~$0.0002／步桌面，才是大家转述的数字。优先收有测量循环的 repo。
- **入场路径很重要。** TypeSafe 候位 vs [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（`typesafe-ai/jev`）一夜改变谁能玩 — Gateway 要和官方 SDK 并列。
- **复制品有价值，归属要标清楚。** SemIf／jevlike 教开源替代；必须标独立，避免被当成 TypeSafe。

## 官方

- [TypeSafe](https://typesafe.ai) - Jev 产品首页与 early-access console。
- [System One 文档](https://docs.typesafe.ai) - 适合什么（原子 typed 问题）、不适合什么（长篇 System-2 散文）。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) - 官方 TypeScript／JavaScript client（`@typesafe-ai/sdk`）。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) - 官方 Python client。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) - 用聊天 LLM 当后端的 drop-in `TypeSafeClient`，方便 A/B 与离线比较。
- [skills](https://github.com/typesafe-ai/skills) - 官方 agent skills（偏 Claude Code／Codex）。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare AI 平台上的模型条目。

## 平台

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - 经 AI SDK 7 `evaluate` 调用 `typesafe-ai/jev`，可不排 TypeSafe 候位。对多数人是实用入场口。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 原生 Choice／Score／Boolean，对齐 System One 在应用里的答案形状。

## 浏览器与电脑操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) - Browser Use 旗舰循环：DOM → 索引操作／目标 → 一次 Jev round trip；小 LLM 只负责打字。苏黎世→伦敦 Flights demo（~7s、~$0.0039）与 [@gregpr07](https://x.com/gregpr07) launch 串，是最多人转述的参考叙事。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) - macOS：OCR + Jev 选下一步（作者表约 ~$0.0002／步）。同一套「决策模型 + 小文字助手」，搬离浏览器。
- [mobile-jev](https://github.com/droidrun/mobile-jev) - 手机自动化、Jev 坐决策位；关心 phone surface 时看这个。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) - 库型 pilot（surface／perception／policy／verify／safety／traces）。星数尚低；若要设计自己的循环，结构比再抄一个 demo 有用。

**暂不收录：** 大多只是重述 Ultrafast、没有新测量或新 surface 的浏览器薄包装。等有独立 benchmark 或有讨论度的语音／UX 角度再看。

## 代码代理

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) - Claude Code plugin：用 Jev 给 tool call／结果打分，留下的内容保持原文。目前「把 System One 塞进 coding loop」信号最强的例子之一，公开讨论也大。
- [foreman](https://github.com/thruwire/foreman) - 「软件工厂」监督，Jev 判断工厂步骤 — 更接近编排而非聊天。
- [jev-review（devagrawal09）](https://github.com/devagrawal09/jev-review) - 分阶段 review + 本地 dashboard。除非你特别要 MCP 包装，优先看这个。
- [jev-review（NiazMorshed2007）](https://github.com/NiazMorshed2007/jev-review) - Local-first MCP `jev_review`，coding agent 仍负责改码。栈是 MCP-first 再收。
- [pi-jev](https://github.com/y0usaf/pi-jev) - Pi agent 的决策层：tool-call 闸门 + `jev_ask`。
- [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi 护栏（不可逆工具、循环、假 done），用 Jev 导航而非硬中断。
- [building-with-jev-skill](https://github.com/dbreunig/building-with-jev-skill) - 社区 skill，教怎么把 Jev 调用写好；可搭官方 `skills`。

## 路由器

- [jev-router](https://github.com/gargpratyush/jev-router) - Claude Code／Codex 每回合 cheap／strong 路由，保留各 CLI 原生体验。最常被引用的 router pattern；实务上留意成本是否变差。
- [jev-codex-router](https://github.com/0xNatoshi/jev-codex-router) - 专注 Codex：每回合选模型、thinking 深度、速度模式。比 jev-router 窄，适合只比 Codex。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) - Hono 语义 HTTP 路由。小但干净的「Jev 选 route」例子，离开 coding agent。

## 数据与库

- [pg-jev](https://github.com/realZachi/pg-jev) - PostgreSQL 扩展：用白话问表，背后是 Jev。少见的「Jev 进数据库」角度。
- [advocaat](https://github.com/pithings/advocaat) - 小型 typed client，对数据提问。不想上完整 agent 栈时的轻量选项。

## 值得研究的 Demo

- [jev-trader](https://github.com/jarrodwatts/jev-trader) - 每个 Monad block 一次买卖决策（Kuru MON-USDC），RPC 预算很紧。就算不交易，也是「热循环 + 校准 choice」模板。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) - 从结构化模拟器状态玩 Mario。玩具表面，认真课：能喂观测状态就别喂像素。
- [jev-search](https://github.com/superagents-lab/jev-search) - 来源选择／query 理解／排序 + Search1API。尚早；收是因为检索型决策集合有意思。

## 开源复制品（非 Jev）

探索 System One 风格决策、**不**宣称 TypeSafe 归属的独立项目。可学概念，勿当 drop-in Jev。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) - 家用 3090 上开源模型做「语义 if」。明确标独立。
- [jevlike](https://github.com/vinnylarouge/jevlike) - 训练小模型做一次通过的选项概率（Doom／棋／Wikispeedia demo）。

## 相关清单

要广度时看这些：

- [awesomejev.com](https://awesomejev.com/) - 大型自动刷新目录（repos、站点、讨论串）。
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) - 社区 awesome list。
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) - 更广的 TypeSafe／System One／Jev 资源。
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - 长文说明（SDK、Gateway、evaluate）。

## 贡献

见 [contributing.md](contributing.md)。PR 请附：repo URL、一句为什么有用、命中哪条筛选、（若有）公开讨论链接。「也提到 Jev」的低信号 PR 会关。

翻译：改结构或条目时请同步 [readme.zh-TW.md](readme.zh-TW.md)／[readme.zh-CN.md](readme.zh-CN.md)；合并以英文 `readme.md` 为准。

## 授权

[CC0](license) — 与多数 awesome list 相同精神。
