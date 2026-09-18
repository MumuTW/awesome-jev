# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**語言：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md)

> 精選、高訊號的 [Jev](https://typesafe.ai) 相關專案 — TypeSafe AI 的 System One 模型，回傳帶置信度的 typed 決策（choice / score / boolean）。

## 這份清單的差異化

市面上已有以**廣度**為主的目錄（[awesomejev.com](https://awesomejev.com/)、[yibie/awesome-jev](https://github.com/yibie/awesome-jev)、[AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)）。我們做的是**判斷**。

| 常見做法 | 我們的做法 |
| --- | --- |
| 掃街／鏡像幾百個 repo | 短清單，一次能讀完 |
| 行銷式一行介紹 | **評語**：為什麼值得看、限制、適合誰 |
| 用星數當排序 | **社群基礎研究**：可量測迴圈、launch 討論（尤其 X）、大家真的在轉述的 pattern |
| 每個 fork 一視同仁 | 每類 pattern 優先 best-in-class；薄包裝 Ultrafast 先跳過 |

向這些清單借鏡（再改成我們的口味）：

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome)／[awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — 策展不是蒐集；門檻高；要說清楚 *為什麼* awesome。
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — 範圍清楚，誠實標「不收／另頁」（我們的 [開源複製品](#開源複製品非-jev)、「暫不收錄」）。
- 多語 README 慣例 — 英文為 OSS 發現用正本；正體／簡體是一等公民鏡像。

## 目錄

- [怎麼篩](#怎麼篩)
- [觀察](#觀察)
- [官方](#官方)
- [平台](#平台)
- [瀏覽器與電腦操作](#瀏覽器與電腦操作)
- [程式碼代理](#程式碼代理)
- [路由器](#路由器)
- [資料與函式庫](#資料與函式庫)
- [值得研究的 Demo](#值得研究的-demo)
- [開源複製品（非 Jev）](#開源複製品非-jev)
- [相關清單](#相關清單)
- [貢獻](#貢獻)

## 怎麼篩

至少滿足以下 **兩項** 才收：

1. 真的呼叫 TypeSafe／Jev API（或官方文件／SDK），不是同名撞車。
2. 這週就能偷師或上線的 pattern（成本、延遲、action space、routing、review）。
3. 有公開討論，不只安靜 README（launch 串、成本／延遲數字、被別人引用）。

不收：大雜燴目錄、沒決策迴圈的改名 clone、從不呼叫 Jev 的「inspired by」（若有教學價值，只放 [開源複製品](#開源複製品非-jev)）。

若與已收錄專案類似，PR 裡要說明 **為什麼更好** — 成熟 awesome list 的同一條規矩。

## 觀察

- **Action space 有限且可觀測時，Jev 才贏。** 在 X 上打出聲量的（Browser Use 機票 demo、Mac computer-use 成本表）都是把世界收成索引表，再一次平行問 Jev。開放式「隨便做」代理不適合。
- **小 LLM 只負責產文字。** Ultrafast 與 computer-use 都把 `TYPE_TEXT`／打字留給文字模型。常見架構是分工，不是「整顆代理換成 Jev」。
- **寫 code 代理的用法在閘門，不在寫作。** Compaction、review、工具放行／拒絕、模型路由，才是 System One 的主場。預期會看到更多 MCP／skill，而不是整顆 coding agent 重寫。
- **延遲敘事比星數更會傳。** ~7 秒／~$0.004 機票、~$0.0002／步桌面，才是大家轉述的數字。優先收有量測迴圈的 repo。
- **入場路徑很重要。** TypeSafe 候位 vs [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（`typesafe-ai/jev`）一夜改變誰能玩 — Gateway 要跟官方 SDK 並列。
- **複製品有價值，歸屬要標清楚。** SemIf／jevlike 教開源替代；必須標獨立，避免被當成 TypeSafe。

## 官方

- [TypeSafe](https://typesafe.ai) - Jev 產品首頁與 early-access console。
- [System One 文件](https://docs.typesafe.ai) - 適合什麼（原子 typed 問題）、不適合什麼（長篇 System-2 散文）。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) - 官方 TypeScript／JavaScript client（`@typesafe-ai/sdk`）。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) - 官方 Python client。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) - 用聊天 LLM 當後端的 drop-in `TypeSafeClient`，方便 A/B 與離線比較。
- [skills](https://github.com/typesafe-ai/skills) - 官方 agent skills（偏 Claude Code／Codex）。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare AI 平台上的模型條目。

## 平台

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - 經 AI SDK 7 `evaluate` 呼叫 `typesafe-ai/jev`，可不排 TypeSafe 候位。對多數人是實用入場口。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 原生 Choice／Score／Boolean，對齊 System One 在應用裡的答案形狀。

## 瀏覽器與電腦操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) - Browser Use 旗艦迴圈：DOM → 索引操作／目標 → 一次 Jev round trip；小 LLM 只負責打字。蘇黎世→倫敦 Flights demo（~7s、~$0.0039）與 [@gregpr07](https://x.com/gregpr07) launch 串，是最多人轉述的參考敘事。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) - macOS：OCR + Jev 選下一步（作者表約 ~$0.0002／步）。同一套「決策模型 + 小文字助手」，搬離瀏覽器。
- [mobile-jev](https://github.com/droidrun/mobile-jev) - 手機自動化、Jev 坐決策位；關心 phone surface 時看這個。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) - 函式庫型 pilot（surface／perception／policy／verify／safety／traces）。星數尚低；若要設計自己的迴圈，結構比再抄一個 demo 有用。

**暫不收錄：** 大多只是重述 Ultrafast、沒有新量測或新 surface 的瀏覽器薄包裝。等有獨立 benchmark 或有討論度的語音／UX 角度再看。

## 程式碼代理

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) - Claude Code plugin：用 Jev 幫 tool call／結果打分，留下的內容保持原文。目前「把 System One 塞進 coding loop」訊號最強的例子之一，公開討論也大。
- [foreman](https://github.com/thruwire/foreman) - 「軟體工廠」監督，Jev 判斷工廠步驟 — 較接近編排而非聊天。
- [jev-review（devagrawal09）](https://github.com/devagrawal09/jev-review) - 分階段 review + 本機 dashboard。除非你特別要 MCP 包裝，優先看這個。
- [jev-review（NiazMorshed2007）](https://github.com/NiazMorshed2007/jev-review) - Local-first MCP `jev_review`，coding agent 仍負責改碼。堆疊是 MCP-first 再收。
- [pi-jev](https://github.com/y0usaf/pi-jev) - Pi agent 的決策層：tool-call 閘門 + `jev_ask`。
- [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi 護欄（不可逆工具、迴圈、假 done），用 Jev 導航而非硬中斷。
- [building-with-jev-skill](https://github.com/dbreunig/building-with-jev-skill) - 社群 skill，教怎麼把 Jev 呼叫寫好；可搭官方 `skills`。

## 路由器

- [jev-router](https://github.com/gargpratyush/jev-router) - Claude Code／Codex 每回合 cheap／strong 路由，保留各 CLI 原生體驗。最常被引用的 router pattern；實務上留意成本是否變差。
- [jev-codex-router](https://github.com/0xNatoshi/jev-codex-router) - 專注 Codex：每回合選模型、thinking 深度、速度模式。比 jev-router 窄，適合只比 Codex。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) - Hono 語意 HTTP 路由。小但乾淨的「Jev 選 route」例子，離開 coding agent。

## 資料與函式庫

- [pg-jev](https://github.com/realZachi/pg-jev) - PostgreSQL 擴充：用白話問表，背後是 Jev。少見的「Jev 進資料庫」角度。
- [advocaat](https://github.com/pithings/advocaat) - 小型 typed client，對資料提問。不想上完整 agent 堆疊時的輕量選項。

## 值得研究的 Demo

- [jev-trader](https://github.com/jarrodwatts/jev-trader) - 每個 Monad block 一次買賣決策（Kuru MON-USDC），RPC 預算很緊。就算不交易，也是「熱迴圈 + 校準 choice」模板。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) - 從結構化模擬器狀態玩 Mario。玩具表面，認真課：能餵觀測狀態就別餵像素。
- [jev-search](https://github.com/superagents-lab/jev-search) - 來源選擇／query 理解／排序 + Search1API。尚早；收是因為檢索型決策集合有意思。

## 開源複製品（非 Jev）

探索 System One 風格決策、**不**宣稱 TypeSafe 歸屬的獨立專案。可學概念，勿當 drop-in Jev。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) - 家用 3090 上開源模型做「語意 if」。明確標獨立。
- [jevlike](https://github.com/vinnylarouge/jevlike) - 訓練小模型做一次通過的選項機率（Doom／棋／Wikispeedia demo）。

## 相關清單

要廣度時看這些：

- [awesomejev.com](https://awesomejev.com/) - 大型自動刷新目錄（repos、站點、討論串）。
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) - 社群 awesome list。
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) - 更廣的 TypeSafe／System One／Jev 資源。
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - 長文說明（SDK、Gateway、evaluate）。

## 貢獻

見 [contributing.md](contributing.md)。PR 請附：repo URL、一句為什麼有用、命中哪條篩選、（若有）公開討論連結。「也提到 Jev」的低訊號 PR 會關。

翻譯：改結構或條目時請同步 [readme.zh-TW.md](readme.zh-TW.md)／[readme.zh-CN.md](readme.zh-CN.md)；合併以英文 `readme.md` 為準。

## 授權

[CC0](license) — 與多數 awesome list 相同精神。
