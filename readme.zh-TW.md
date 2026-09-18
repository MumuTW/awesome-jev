# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**語言：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> 精選、高訊號的 [Jev](https://typesafe.ai) 相關專案 — TypeSafe AI 的 System One 模型（帶置信度的 typed 決策）— 以及在公開討論有熱度時的 **Jev-like** 模型與複製品。

## 這份清單的差異化

市面上已有以**廣度**為主的目錄（[awesomejev.com](https://awesomejev.com/)、[yibie/awesome-jev](https://github.com/yibie/awesome-jev)、[AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)）。我們做的是**判斷**。

| 常見做法 | 我們的做法 |
| --- | --- |
| 掃街／鏡像幾百個 repo | 短清單，一次能讀完 |
| 行銷式一行介紹 | **評語**：為什麼值得看、限制、適合誰 |
| 用星數當排序 | **社群基礎研究** — 可量測迴圈、launch 討論（尤其 X） |
| 只收「有打 TypeSafe API」 | 也收 **Jev-like／相關模型**（X／HN 顯示實用興趣時），並標非 TypeSafe |
| 每個 fork 一視同仁 | 每類 pattern 優先 best-in-class |

## 目錄

- [這份清單的差異化](#這份清單的差異化)
- [策展](#怎麼篩)
  - [怎麼篩](#怎麼篩)
  - [觀察](#觀察)
- [官方與平台](#官方)
  - [官方](#官方)
  - [平台](#平台)
- [整合應用](#瀏覽器與電腦操作)
  - [瀏覽器與電腦操作](#瀏覽器與電腦操作)
  - [程式碼代理](#程式碼代理)
  - [路由器](#路由器)
  - [資料與函式庫](#資料與函式庫)
  - [值得研究的 Demo](#值得研究的-demo)
- [Jev-like 與相關模型](#jev-like-與相關模型)
- [相關清單](#相關清單)
- [貢獻](#貢獻)

## 怎麼篩

### 直接使用 Jev／TypeSafe

至少滿足 **兩項**：真 API／官方、可偷師的 pattern、公開討論（尤其 X）。

### Jev-like／相關模型（可不呼叫 Jev）

只要公開討論（尤其 **X**，有時 HN）顯示**實用興趣或熱度**即可收，並清楚標獨立／inspired-by。星數不夠；有人轉述的討論串或量測 demo 通常夠。

## 觀察

- **Action space 有限且可觀測時 Jev 才贏。** X 上打出聲量的：[Browser Use 機票](https://x.com/gregpr07/status/2100411066966749359)、[Mac computer-use 成本](https://x.com/awlevin/status/2100262612428894676)。
- **小 LLM 只負責產文字。**
- **Coding 用法在閘門，不在寫作。**
- **延遲敘事 > 星數。** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) 即使沒有廣為引用的 launch 帖也值得看。
- **入場路徑：** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)）。
- **Jev-like 熱度是訊號，不是歸屬。**

## 官方

- [TypeSafe](https://typesafe.ai) - 產品首頁與 early-access console。
- [System One 文件](https://docs.typesafe.ai) - 適合／不適合什麼。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 官方 TS／JS client。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 官方 Python client。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - LLM 後端的 drop-in client，方便 A/B。
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - 官方 agent skills（[@typesafeai](https://x.com/typesafeai/status/2100376436272173088)）。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare 模型條目。

## 平台

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - 經 AI SDK 7 `evaluate` 呼叫；見 [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 原生 Choice／Score／Boolean。

## 瀏覽器與電腦操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - 旗艦迴圈；Flights ~7s／~$0.0039。X：[@gregpr07](https://x.com/gregpr07/status/2100411066966749359)。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS OCR + Jev。X：[@awlevin](https://x.com/awlevin/status/2100262612428894676)。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - 函式庫型 pilot；星數低、結構強。

**暫不收錄：** 無新量測／無 X 聲量的 Ultrafast 薄包裝（含 mobile，等有討論再看）。

## 程式碼代理

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code compaction；高星／趨勢強，即使沒有廣為引用的 launch 帖。
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - 軟體工廠監督。X：[@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717)。
- [jev-review（devagrawal09）](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 分階段 review；見 roundup [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556)。
- [jev-review（NiazMorshed2007）](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - MCP-first 時再優先。
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) - Pi 決策層。
- [pi-warden](https://github.com/DevMortimer/pi-warden) ![GitHub stars](https://img.shields.io/github/stars/DevMortimer/pi-warden?style=flat) - Pi 護欄。

## 路由器

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - 最常被引用的 router；X 弱於瀏覽器 demo，仍因實用而收錄。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono 語意路由。

## 資料與函式庫

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - Postgres 擴充；X 弱、niche 實用強故仍收錄。

## 值得研究的 Demo

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - Monad block 交易決策。X：[@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346)。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 結構化狀態玩 Mario。

## Jev-like 與相關模型

可不呼叫 TypeSafe；收錄看**討論熱度與研究價值**。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - 開源「語意 if」。X 稀疏（如 [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)）；標 inspired-by。
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 小模型一次通過選項機率；X 稀疏 + HN ~161 pts。
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - 開源「Jev 配方」（LoRA＋constrained serving）。非官方。X：[@madiator](https://x.com/madiator/status/2100990591215783946)；亦上 HN。
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - Prefill-only、相容 Jev 形狀的 API（SGLang）。非官方。HN 有討論。
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - 本機 Gemma／MLX option scoring。非官方。HN。
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - Qwen3 letter-logits 小實驗。非官方。HN。
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - Apple Silicon MLX 平行決策。非官方。X：[@beni_il_](https://x.com/beni_il_/status/2100617387116568956)；HN。
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 平行 constrained／多字段（HF 模型）。非官方。強 X：[@harshagundal](https://x.com/harshagundal/status/2100044305536889015)。
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 任意 LLM 包成類 Jev `/v1/systemone`。非官方。X：[@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337)。

有更多 X／HN 持續討論時歡迎 PR。

## 相關清單

- [awesomejev.com](https://awesomejev.com/)
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) ![GitHub stars](https://img.shields.io/github/stars/yibie/awesome-jev?style=flat)
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) ![GitHub stars](https://img.shields.io/github/stars/AbdelStark/awesome-typesafe?style=flat)
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/)

## 貢獻

## 授權

[CC0](license)
