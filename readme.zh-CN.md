# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**语言：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> 快速看懂风格鲜明的 [Jev](https://typesafe.ai)：TypeSafe 专为类型化决策（单选、评分、附带信心度的布林值）设计的「系统一」模型，以及社群热烈讨论时值得关注的同类模型。

看腻 400 个安静 clone 的大杂烩了吗？我们也是。这份清单故意短，每条有**评语**（为什么值得看、适合谁、要注意什么），并靠**社群研究** — 可量测循环、X 上的 launch 串、大家一直在转述的 pattern。希望你能带走下一周就能用上的东西。

## 这份清单的差异化

市面上已有以**广度**为主的目录（[awesomejev.com](https://awesomejev.com/)、[yibie/awesome-jev](https://github.com/yibie/awesome-jev)、[AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)）。我们做的是**品味**。

| 常见做法 | 我们的做法 |
| --- | --- |
| 扫街／镜像几百个 repo | 短清单，配杯咖啡就能读完 |
| 行销式一行介绍 | **评语** — 为什么值得看、限制、适合谁 |
| 用星数当排序 | **社群基础研究** — 可量测循环、launch 讨论（尤其 X） |
| 只收「有打 TypeSafe API」 | 也收 **Jev-like／相关模型**（X／HN 真有热度时），并标非 TypeSafe |
| 每个 fork 一视同仁 | 每类 pattern 挑最好的；薄包装 Ultrafast 礼貌略过 |

站在我们喜欢的清单肩膀上：

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome)／[awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — 策展不是搜集；门槛高；要说清楚 *为什么* awesome。
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — 范围清楚，诚实标「不收／另类」。

## 目录

- [这份清单的差异化](#这份清单的差异化)
- [策展](#怎么筛)
  - [怎么筛](#怎么筛)
  - [观察](#观察)
- [官方与平台](#官方)
  - [官方](#官方)
  - [平台](#平台)
- [整合应用](#浏览器与电脑操作)
  - [浏览器与电脑操作](#浏览器与电脑操作)
  - [代码代理](#代码代理)
  - [路由器](#路由器)
  - [数据与库](#数据与库)
  - [值得研究的 Demo](#值得研究的-demo)
- [用例与概念](#用例与概念)
- [Jev-like 与相关模型](#jev-like-与相关模型)
- [相关清单](#相关清单)
- [由 Grok Bot 维护](#由-grok-bot-维护)
- [贡献](#贡献)

## 怎么筛

### 直接使用 Jev／TypeSafe

至少满足 **两项**：真 API／官方、可借鉴的 pattern、公开讨论（尤其 X）。

### Jev-like／相关模型（可不调用 Jev）

只要公开讨论（尤其 **X**，有时 HN）显示**实用兴趣或热度**即可收，并清楚标独立／inspired-by。星数不够；有人转述的讨论串或量测 demo 通常够。

## 观察

- **Action space 有限且可观测时 Jev 才赢。** X 上打出声量的：[Browser Use 机票](https://x.com/gregpr07/status/2100411066966749359)、[Mac computer-use 成本](https://x.com/awlevin/status/2100262612428894676)。
- **小 LLM 只负责产文字。**
- **Coding 用法在闸门，不在写作。**
- **延迟叙事 > 星数。** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) 即使没有广为引用的 launch 帖也值得看。
- **入场路径：** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)）。
- **高讨论但缺可交付 repo 的概念仍然有价值。** 收进 [用例与概念](#用例与概念)——用讨论串与长文说明 System One pattern 长什么样。验证薄弱的病毒 flex 不进，或只留一句警告。
- **Jev-like 热度是讯号，不是归属。**

## 官方

- [TypeSafe](https://typesafe.ai) - 母舰：产品首页、early-access console，也是最干净感受「Jev 在卖什么」的地方。若你还在评估 System One 能不能进自家 stack，先来这里——比较像「能不能动手试」，不是文件大杂烩。提醒：early access 仍代表有些门开得比社群 demo 慢。
- [System One 文件](https://docs.typesafe.ai) - 对「Jev 擅长什么」写得最利的答案：原子类型问题可以，长篇 System-2 散文不行。我们收它，是因为每个好的整合都在默默对齐这套心智模型。适合架构师在烧 API 额度前先把 prompt 与 schema 想清楚。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 官方 TypeScript／JavaScript client（`@typesafe-ai/sdk`）——若你的应用已在 Node 或浏览器，这是阻力最小的入场口。收录理由很务实：从「有趣论文」走到正式环境里的 typed Choice／Score／Boolean。别急着手写 fetch，除非你热爱重新踩 auth 边角。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 同一套 System One 界面的官方 Python client。最适合资料／ML 人把 Jev 放进 notebook 与 agent 旁，不必假装一定要写 TypeScript。薄但可信——当它是受祝福的正式 client，不是研究草稿。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - 用一般 chat LLM 当后端的 drop-in `TypeSafeClient`，好做 A／B 与离线对照，不用干等真模型。挑给「先要公平 baseline 再决定要不要砸钱」的团队。Caveat：这是替身，不是免费 Jev——评估笔记里请大声标清楚。
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - 官方 agent skills，对准 System One API——「先把对的厨具拿出来再开火」那一包。收录是因为 [@typesafeai](https://x.com/typesafeai/status/2100376436272173088) 把它框成认真建造者该怎么起步。给想要惯例、不要又一个空白 repo 的 agent 作者。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare AI 平台上的托管模型条目；若你的 runtime 本来就是 Workers 形状，值得收藏。在意边缘同地部署胜过自己养 client stack 时很实用。比较像「真的有上架」的收据，不是教学文。

## 平台

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - 透过 AI SDK 7 `evaluate` 呼叫 `typesafe-ai/jev`，不用干等私人 waitlist——隔夜就改写「谁能动手试」的入场路径。放在较高位置，是因为 [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175) 把存取权变成产品故事，不是脚注。Next.js／AI SDK 商店首选；只是 Gateway 配额终究还是配额。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 原生 Choice／Score／Boolean 路径，看起来就像 System One 的答案已经住进你的应用程序代码。选作 Gateway 条目的人体工学双胞胎——同一套心智模型、更少胶水档。实验性名称很诚实：API 仍可能在你脚下移动。

## 浏览器与电脑操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - Browser Use 旗舰循环，也仍是网络上最清楚的「为什么需要 Jev」示范：DOM → 索引化操作／目标 → 一轮 Jev，小 LLM 只负责打字。Zürich→London Flights（约 7 秒、约 $0.0039）加上 [@gregpr07](https://x.com/gregpr07/status/2100411066966749359)，让延迟叙事比任何星数图走得更远。Action space 有限且可观测就借鉴这套架构；若你的 agent 还在「随便做」，先别装。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS 电脑操作：OCR + Jev，作者表上的成本数字（约 $0.0002／步）让人坐直。值得一看，是因为 [@awlevin](https://x.com/awlevin/status/2100262612428894676) 把桌面自动化讲成可量测的 System One 故事，不是气氛片。Mac 原生建造者首选；OCR 噪声是你跳过完美无障碍树时要付的税。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - 库型 pilot（surface、perception、policy、verify、safety、traces），给要自己设计循环、不想硬 fork Ultrafast 的人。星数安静，结构不安静——这正是收它的理由。想要可抽换接缝就选它；今晚只想看到能飞的机票 demo，先看 Ultrafast。

**暂未收录：** 无新量测／无 X 声量的 Ultrafast 薄包装（含 mobile，等有讨论再看）。

## 代码代理

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code plugin：Jev 替 tool call／结果打分，保留的上下文维持原文——compaction 是闸门，不是会发明内容的摘要器。高星、趋势强，即使没有广为引用的 launch 帖；我们在「观察」也点名它。给被 tool 噪音淹死的 Claude Code 重度使用者；若任务需要一长串无聊但必要的尾巴，小心删太狠。
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - 软件工厂监督，让 Jev 审判每个步骤——比较像「这阶段真的过了吗？」，不是「帮我写 PR」。[@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717) 丢进时间轴的 Codex 监督视角很有力。给多 agent 工厂建造者；若你只要单一 review bot，这偏重。
- [jev-review（devagrawal09）](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 分阶段 review 加本地 dashboard——社群最爱的「把闸门摊开给我看」形状。出现在 [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556) 这类 roundup，热度对 review 工具来说够了。想要人眼可见的阶段就选它；比一次 MCP 呼叫重。
- [jev-review（NiazMorshed2007）](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - 本地优先的 MCP `jev_review`，给 stack 已经是 MCP 形状的人。若 Claude／Cursor 工具是你的正门，优先这位兄弟；X 讯号弱于分阶段那位，没关系。Caveat：MCP 爽感优先，dashboard 抛光其次。
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) - Pi 的决策层：tool-call 闸门加上 `jev_ask`，让 agent 先问再动手。收作干净的「System One 当权限」pattern，绑在特定 agent runtime。给想要类型化否决权的 Pi 使用者；它本身不是通用 coding agent。
- [pi-warden](https://github.com/DevMortimer/pi-warden) ![GitHub stars](https://img.shields.io/github/stars/DevMortimer/pi-warden?style=flat) - Pi 护栏，挡不可逆工具、循环与假「完成」，由 Jev 导航。跟 pi-jev 很合拍，当你在意安全表演要变成真检查时。最适合曾被「太早说做完」的 agent 烫过的人。

## 路由器

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - 给 Claude Code 与 Codex 的每回合 cheap／strong 路由——仍是这生态系最常被引用的 router pattern。X 热度淡于浏览器 demo，但实用性本身就值得收录。当你以为简单的回合开始被「便宜」模型搞砸时，盯紧成本回弹。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono 的语意 HTTP 路由：Jev 选路，handler 保持无聊。小而干净，证明 System One 不只是 coding agent 玩具。给 Hono／边缘 API 人；静态 path 表已够用就别硬加。

## 数据与库

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - PostgreSQL 扩充，用白话问表，答案走 Jev——少见的「决策模型住在资料旁边」角度。X 安静，niche 实用很大声，对我们够了。给 SQL 原生团队；别拿它当完整分析仓储故事的替代品。

## 值得研究的 Demo

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - 每个 Monad block 对 Kuru MON-USDC 做一次买／卖决策——热循环加校准过的 choice，不是「感觉看多」的聊天机器人。[@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346) 让这模板传开。学它的节奏；别当投资建议，也别当正式交易台。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 用结构化模拟器状态玩 Mario——玩具表面，认真教训：能喂观测状态就别硬喂像素。收录是为了教 action-space 卫生。好玩第一；上线第二（或永远不上）。

## 用例与概念

这里放高讨论的讨论串与文章，用来说明 System One pattern 长什么样。许多是 demo 或长文，未必有打磨好的公开 repo（除非另注）。有扎实的开源产物后，可能移到上方主分类。

### 框架

- [LLMs 产答案，Jev 做决定](https://x.com/paarangatrai/status/2100113737097367896) - 在 X 上站稳的一句心智模型。用来跟队友解释 System One；这是框架，不是产品。
- [WTF Is Jev? 九件社区已在做的事](https://x.com/mvanhorn/status/2100784142850097482) - 有收据的模式总览：给候选（别发明）、快反应／慢规划、可测量循环。当「该看什么」地图，不要当复刻清单。
- [用 Jev 组 Harness（LangChain）](https://x.com/sydneyrunkle/status/2100754364545761643) - 架构文：Jev 当 agent 循环里的闸门（路由、高风险 tool）。学 harness 形状；主产物是 blog／LangChain middleware，不是玩具 demo repo。

### 产品感 Demo（repo 可有可无）

- [意图 launcher——「我刚下载的 PDF」](https://x.com/dabit3/status/2100756930054504776) - 在有限候选上读 keystroke 意图（约 100 ms）。工作码在 [dabit3/jev-experiments](https://github.com/dabit3/jev-experiments)（`jev-launcher`）；先当 use-case 故事，因为大家引用的是这则帖。
- [预测试算表——栏位标题当 schema](https://x.com/dabit3/status/2100780008193020049) - 「试算表重算数字，不重算意义。」同实验库（`judge-sheets`）。很适合 inbox／分流表的隐喻。
- [语音 → Jev → 浏览器点击](https://x.com/moritzkremb/status/2100577979021832365) - 双手被占住时的控制循环（作者数字约 300 ms／~$0.0002）。影片 demo；未核到公开 repo——只收 pattern。
- [本机 OCR 标签 → Jev 选点](https://x.com/milindlabs/status/2100631847155994852) - 本地感知、只送文字给 Jev（约 90 ms）。补足上方的 [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use)；不同作者、同一课：可观测的 action space。未核到 repo。

### 即时／多智能体概念

- [Minecraft：Jev 反应、Astra 规划](https://x.com/wuyang_zhou/status/2100727660875808913) - 活负载下的快 System One＋慢 System Two 分工。未核到公开 repo；学角色边界，别把片段当蓝图。
- [情绪细胞自动机](https://x.com/riku720720/status/2100738087584481657) - 多个 agent 并行用 Jev 更新状态——少见的多体概念（不是又一个单人游戏 bot）。赞数较低；新意较高。

### 流传中（附保留）

声量大、但还没有干净可交付物的 demo——适合对齐方向，不当可直接照抄的起点：

- [「一小时重做 Tesla FSD」](https://x.com/jpschroeder/status/2100347770867458384) - 极端循环叙事；可重现前先当营销。
- [Subway Surfers＋50 平行局](https://x.com/_MaxBlade/status/2100634359099232678) - 并行决策成本叙事；仅 demo。
- [Slay the Spire 2 约 0.7s 选招](https://x.com/coolish/status/2100570517954838897) - 有限游戏 action space；仅 demo。
- [贴文病毒分（61 问／SuperX）](https://x.com/robj3d3/status/2100722975645598191) - 并行多问打分的产品试用链接；帖内无公开 GitHub。


## Jev-like 与相关模型

可不调用 TypeSafe；收录看**讨论热度与研究价值**。它们**非官方、非附属**。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - 家里 3090 上用开源模型做的「语意 if」——明确独立，与 TypeSafe **无附属关系**。X 稀疏（如 [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)），但对想在本机玩条件式的人够当 inspired-by 参考。给 DIY GPU 玩家；预期研究毛边，不是抛光 SaaS 双胞胎。
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 训练小模型一次通过输出选项几率（Doom／chess／Wikispeedia）。独立／inspired-by 教材，X 稀疏但 HN 约 161 分有感。想亲自感受 System One 形状输出怎么被学出来就看它；**非** Jev 替身，也**非**附属。
- [laya](https://github.com/NandhaKishorM/laya) ![GitHub stars](https://img.shields.io/github/stars/NandhaKishorM/laya?style=flat) - 可本机跑的开源 System One 味决策模型（[HF](https://huggingface.co/convaiinnovations/laya)、PyPI `laya`）——**与 TypeSafe 无附属关系**。亮点是可交付堆栈，以及 **selective gating**（没把握就弃权／上送）。作者自报 vs Jev 的延迟／正确率图值得当雷达，**不是**同一套基准：Jev 数字常靠 frontier 一致度，Laya 多用自家 in-task——**别读成「赢过 Jev」定论**。想试开源替代的人收；请务必留意方法论差异。
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - 开源「Jev 配方」（LoRA＋constrained serving）——**非** TypeSafe 附属；配方本身就是产品，所以收在这里。[@madiator](https://x.com/madiator/status/2100990591215783946) 与 HN 都给了热度。给想自己煮 System One 味模型的团队；请自备 ML ops 耐心。
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - SGLang 上的 prefill-only、Jev 形状相容 API——独立，**非**附属。HN 讨论是门票：serving 形状跟权重一样重要。给已住在 SGLang 的 infra 人；把「相容」读成「形状像」，不是「官方」。
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - 本机 Gemma／MLX option scoring。与 TypeSafe **无附属关系**；因 HN 好奇与笔电友善实验而上榜。给 Apple／本机探索者；分数当教材，别当正式校准。
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - 用 Qwen3 letter-logits 朝 System One 风格选择的小实验。独立、**非**附属；HN 是它坐在这里的理由。给拿 stick 戳 logits 的研究者——可爱，不是产品。
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - 透过 MLX 在 Apple Silicon 上做平行决策。**非**附属；热度来自 [@beni_il_](https://x.com/beni_il_/status/2100617387116568956) 与 HN。Mac MLX 原生、想追平行 Choice 形呼叫的人首选；评估架请自备。
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 平行 constrained／多字段决策的 HF 模型——独立，**非** TypeSafe。[@harshagundal](https://x.com/harshagundal/status/2100044305536889015) 的强 X 换到席位。给想下载一颗脑、不要 API key 的人；信任多字段输出前先验证约束。
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 把任意 LLM 包成类 Jev 的 `/v1/systemone` 表面。**非**附属；[@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337) 把 adapter pattern 放到地图上。协议实验很方便；记住包装纸不会魔法变成 System One 品质。

有更多 X／HN 持续讨论时欢迎 PR。

## 相关清单

- [awesomejev.com](https://awesomejev.com/) - 大型自动刷新目录（repos、sites、threads），专门补我们刻意拒绝的广度。用它扫街发现，回这里做品味判断。好搭档，但别拿它当品味的替代品。
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) ![GitHub stars](https://img.shields.io/github/stars/yibie/awesome-jev?style=flat) - 社群版 Jev awesome list——网更宽、编辑声比较轻。适合作同侪雷达，一起对照社区在长什么。安静条目请交叉核对评语再采用。
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) ![GitHub stars](https://img.shields.io/github/stars/AbdelStark/awesome-typesafe?style=flat) - 更广的 TypeSafe＋System One＋Jev 资源，不只「有打 API 的 app」。给要画整片地景、而不是只挑旗舰 demo 的人。预期链接密度高于辛辣短评。
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - 长文解释 SDK、Gateway 与 `evaluate`——你丢给不想开十五个分页的同事的那一篇。温暖、务实、带一点好的主见。最适合 onboarding，不是活目录。

## 由 Grok Bot 维护

这份清单由 **[Grok Bot](https://grok.com)** 打理（重要取舍会有人类盯一眼）。我们看社群在做什么、在吵什么，再把评语写诚实。

如果这里帮你上线了什么 — 或你觉得哪条收错了 — 开 issue 或 PR 都行。**希望你喜欢。** 附上好讨论串、讲清楚「为什么」的 PR，我们会很开心。

## 贡献

见 [contributing.md](contributing.md)。PR 请附 repo、为什么有用、命中哪条筛选，以及（若有）公开讨论链接。低讯号的「也提到 Jev」会温柔关闭。

## 授权

[CC0](license) — 随便分享、fork、改作。跟多数 awesome list 一样。
