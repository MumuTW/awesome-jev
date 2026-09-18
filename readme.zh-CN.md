# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**语言：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> 精选、高信号的 [Jev](https://typesafe.ai) 相关项目 — TypeSafe AI 的 System One 模型（带置信度的 typed 决策）— 以及在公开讨论有热度时的 **Jev-like** 模型与复制品。

## 这份清单的差异化

市面上已有以**广度**为主的目录（[awesomejev.com](https://awesomejev.com/)、[yibie/awesome-jev](https://github.com/yibie/awesome-jev)、[AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)）。我们做的是**判断**。

| 常见做法 | 我们的做法 |
| --- | --- |
| 扫街／镜像几百个 repo | 短清单，一次能读完 |
| 营销式一行介绍 | **评语**：为什么值得看、限制、适合谁 |
| 用星数当排序 | **社区基础研究** — 可测量循环、launch 讨论（尤其 X） |
| 只收「打了 TypeSafe API」 | 也收 **Jev-like／相关模型**（X／HN 显示实用兴趣时），并标非 TypeSafe |
| 每个 fork 一视同仁 | 每类 pattern 优先 best-in-class |

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
- [Jev-like 与相关模型](#jev-like-与相关模型)
- [相关清单](#相关清单)
- [贡献](#贡献)

## 怎么筛

### 直接使用 Jev／TypeSafe

至少满足 **两项**：真 API／官方、可偷师的 pattern、公开讨论（尤其 X）。

### Jev-like／相关模型（可不调用 Jev）

只要公开讨论（尤其 **X**，有时 HN）显示**实用兴趣或热度**即可收，并清楚标独立／inspired-by。星数不够；有人转述的讨论串或测量 demo 通常够。

## 观察

- **Action space 有限且可观测时 Jev 才赢。** X 上打出声量的：[Browser Use 机票](https://x.com/gregpr07/status/2100411066966749359)、[Mac computer-use 成本](https://x.com/awlevin/status/2100262612428894676)。
- **小 LLM 只负责产文字。**
- **Coding 用法在闸门，不在写作。**
- **延迟叙事 > 星数。** **Star ≠ X：** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) 没找到 launch 帖仍 keep。
- **入场路径：** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)）。
- **Jev-like 热度是信号，不是归属。**

## 官方

- [TypeSafe](https://typesafe.ai) - 产品首页与 early-access console。
- [System One 文档](https://docs.typesafe.ai) - 适合／不适合什么。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) - 官方 TS／JS client。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) - 官方 Python client。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) - LLM 后端的 drop-in client，方便 A/B。
- [skills](https://github.com/typesafe-ai/skills) - 官方 agent skills（[@typesafeai](https://x.com/typesafeai/status/2100376436272173088)）。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare 模型条目。

## 平台

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - 经 AI SDK 7 `evaluate` 调用；见 [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 原生 Choice／Score／Boolean。

## 浏览器与电脑操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) - 旗舰循环；Flights ~7s／~$0.0039。X：[@gregpr07](https://x.com/gregpr07/status/2100411066966749359)。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) - macOS OCR + Jev。X：[@awlevin](https://x.com/awlevin/status/2100262612428894676)。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) - 库型 pilot；星数低、结构强。

**暂不收录：** 无新测量／无 X 声量的 Ultrafast 薄包装（含 mobile，等有讨论再看）。

## 代码代理

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) - Claude Code compaction；高星／趋势强，无 launch 帖仍 keep。
- [foreman](https://github.com/thruwire/foreman) - 软件工厂监督。X：[@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717)。
- [jev-review（devagrawal09）](https://github.com/devagrawal09/jev-review) - 分阶段 review；见 roundup [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556)。
- [jev-review（NiazMorshed2007）](https://github.com/NiazMorshed2007/jev-review) - MCP-first 时再优先。
- [pi-jev](https://github.com/y0usaf/pi-jev) - Pi 决策层。
- [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi 护栏。

## 路由器

- [jev-router](https://github.com/gargpratyush/jev-router) - 最常被引用的 router；X 弱于浏览器 demo，仍因实用 keep。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) - Hono 语义路由。

## 数据与库

- [pg-jev](https://github.com/realZachi/pg-jev) - Postgres 扩展；X 弱、niche 实用强故 keep。

## 值得研究的 Demo

- [jev-trader](https://github.com/jarrodwatts/jev-trader) - Monad block 交易决策。X：[@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346)。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) - 结构化状态玩 Mario。

## Jev-like 与相关模型

可不调用 TypeSafe；收录看**讨论热度与研究价值**。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) - 开源「语义 if」。X 稀疏（如 [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)）；标 inspired-by。
- [jevlike](https://github.com/vinnylarouge/jevlike) - 小模型一次通过选项概率；X 稀疏 + HN ~161 pts。

有更多 X／HN 持续讨论时欢迎 PR。

## 相关清单

- [awesomejev.com](https://awesomejev.com/)
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev)
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/)

## 贡献

见 [contributing.md](contributing.md)。合并以英文 `readme.md` 为准。

## 授权

[CC0](license)
