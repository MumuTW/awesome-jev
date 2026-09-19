# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**語言：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> 快速看懂風格鮮明的 [Jev](https://typesafe.ai)：TypeSafe 專為型別化決策（單選、評分、附帶信心度的布林值）設計的「系統一」模型，以及社群熱烈討論時值得關注的同類模型。

看膩 400 個安靜 clone 的大雜燴了嗎？我們也是。這份清單刻意短，每條有**評語**（為什麼值得看、適合誰、要注意什麼），並靠**社群研究** — 可量測迴圈、X 上的 launch 串、大家一直在轉述的 pattern。希望你能偷到下一週就能用的東西。

## 這份清單的差異化

市面上已有以**廣度**為主的目錄（[awesomejev.com](https://awesomejev.com/)、[yibie/awesome-jev](https://github.com/yibie/awesome-jev)、[AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)）。我們做的是**品味**。

| 常見做法 | 我們的做法 |
| --- | --- |
| 掃街／鏡像幾百個 repo | 短清單，配杯咖啡就能讀完 |
| 行銷式一行介紹 | **評語** — 為什麼值得看、限制、適合誰 |
| 用星數當排序 | **社群基礎研究** — 可量測迴圈、launch 討論（尤其 X） |
| 只收「有打 TypeSafe API」 | 也收 **Jev-like／相關模型**（X／HN 真有熱度時），並標非 TypeSafe |
| 每個 fork 一視同仁 | 每類 pattern 挑最好的；薄包裝 Ultrafast 禮貌略過 |

站在我們喜歡的清單肩膀上：

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome)／[awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — 策展不是蒐集；門檻高；要說清楚 *為什麼* awesome。
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — 範圍清楚，誠實標「不收／另類」。

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
- [Use case 與概念展示（觀察中）](#use-case-與概念展示觀察中)
- [Jev-like 與相關模型](#jev-like-與相關模型)
- [相關清單](#相關清單)
- [由 Grok Bot 維護](#由-grok-bot-維護)
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
- **高討論但缺可交付 repo 的概念仍然有價值。** 收進 [Use case 與概念展示（觀察中）](#use-case-與概念展示觀察中)——讓人「看懂 pattern」的帖／長文，不是 fork 目標。驗證薄弱的病毒 flex 不進，或只留一句警告。
- **Jev-like 熱度是訊號，不是歸屬。**

## 官方

- [TypeSafe](https://typesafe.ai) - 母艦：產品首頁、early-access console，也是最乾淨感受「Jev 在賣什麼」的地方。若你還在評估 System One 能不能進自家 stack，先來這裡——比較像「能不能動手試」，不是文件大雜燴。提醒：early access 仍代表有些門開得比社群 demo 慢。
- [System One 文件](https://docs.typesafe.ai) - 對「Jev 擅長什麼」寫得最利的答案：原子型別問題可以，長篇 System-2 散文不行。我們收它，是因為每個好的整合都在默默對齊這套心智模型。適合架構師在燒 API 額度前先把 prompt 與 schema 想清楚。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 官方 TypeScript／JavaScript client（`@typesafe-ai/sdk`）——若你的應用已在 Node 或瀏覽器，這是阻力最小的入場口。收錄理由很務實：從「有趣論文」走到正式環境裡的 typed Choice／Score／Boolean。別急著手寫 fetch，除非你熱愛重新踩 auth 邊角。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 同一套 System One 介面的官方 Python client。最適合資料／ML 人把 Jev 放進 notebook 與 agent 旁，不必假裝一定要寫 TypeScript。薄但可信——當它是受祝福的正式 client，不是研究草稿。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - 用一般 chat LLM 當後端的 drop-in `TypeSafeClient`，好做 A／B 與離線對照，不用乾等真模型。挑給「先要公平 baseline 再決定要不要砸錢」的團隊。Caveat：這是替身，不是免費 Jev——評估筆記裡請大聲標清楚。
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - 官方 agent skills，對準 System One API——「先把對的廚具拿出來再開火」那一包。收錄是因為 [@typesafeai](https://x.com/typesafeai/status/2100376436272173088) 把它框成認真建造者該怎麼起步。給想要慣例、不要又一個空白 repo 的 agent 作者。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare AI 平台上的託管模型條目；若你的 runtime 本來就是 Workers 形狀，值得收藏。在意邊緣同地部署勝過自己養 client stack 時很實用。比較像「真的有上架」的收據，不是教學文。

## 平台

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - 透過 AI SDK 7 `evaluate` 呼叫 `typesafe-ai/jev`，不用乾等私人 waitlist——隔夜就改寫「誰能動手試」的入場路徑。我們把它放高，是因為 [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175) 把存取權變成產品故事，不是腳註。Next.js／AI SDK 商店首選；只是 Gateway 配額終究還是配額。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 原生 Choice／Score／Boolean 路徑，看起來就像 System One 的答案已經住進你的應用程式碼。選作 Gateway 條目的人體工學雙胞胎——同一套心智模型、更少膠水檔。實驗性名稱很誠實：API 仍可能在你腳下移動。

## 瀏覽器與電腦操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - Browser Use 旗艦迴圈，也仍是網路上最清楚的「為什麼需要 Jev」示範：DOM → 索引化操作／目標 → 一輪 Jev，小 LLM 只負責打字。Zürich→London Flights（約 7 秒、約 $0.0039）加上 [@gregpr07](https://x.com/gregpr07/status/2100411066966749359)，讓延遲敘事比任何星數圖走得更遠。Action space 有限且可觀測就偷這套架構；若你的 agent 還在「隨便做」，先別裝。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS 電腦操作：OCR + Jev，作者表上的成本數字（約 $0.0002／步）讓人坐直。收錄是因為 [@awlevin](https://x.com/awlevin/status/2100262612428894676) 把桌面自動化講成可量測的 System One 故事，不是氣氛片。Mac 原生建造者首選；OCR 雜訊是你跳過完美無障礙樹時要付的稅。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - 函式庫型 pilot（surface、perception、policy、verify、safety、traces），給要自己設計迴圈、不想硬 fork Ultrafast 的人。星數安靜，結構不安靜——這正是收它的理由。想要可抽換接縫就選它；今晚只想看到能飛的機票 demo，先看 Ultrafast。

**暫放停車場：** 無新量測／無 X 聲量的 Ultrafast 薄包裝（含 mobile，等有討論再看）。

## 程式碼代理

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code plugin：Jev 替 tool call／結果打分，保留的上下文維持原文——compaction 是閘門，不是會發明內容的摘要器。高星、趨勢強，即使沒有廣為引用的 launch 帖；我們在「觀察」也點名它。給被 tool 噪音淹死的 Claude Code 重度使用者；若任務需要一長串無聊但必要的尾巴，小心刪太狠。
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - 軟體工廠監督，讓 Jev 審判每個步驟——比較像「這階段真的過了嗎？」，不是「幫我寫 PR」。我們喜歡 [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717) 丟進時間軸的 Codex 監督視角。給多 agent 工廠建造者；若你只要單一 review bot，這偏重。
- [jev-review（devagrawal09）](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 分階段 review 加本地 dashboard——社群最愛的「把閘門攤開給我看」形狀。出現在 [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556) 這類 roundup，熱度對 review 工具來說夠了。想要人眼可見的階段就選它；比一次 MCP 呼叫重。
- [jev-review（NiazMorshed2007）](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - 本地優先的 MCP `jev_review`，給 stack 已經是 MCP 形狀的人。若 Claude／Cursor 工具是你的正門，優先這位兄弟；X 訊號弱於分階段那位，沒關係。Caveat：MCP 爽感優先，dashboard 拋光其次。
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) - Pi 的決策層：tool-call 閘門加上 `jev_ask`，讓 agent 先問再動手。收作乾淨的「System One 當權限」pattern，綁在特定 agent runtime。給想要型別化否決權的 Pi 使用者；它本身不是通用 coding agent。
- [pi-warden](https://github.com/DevMortimer/pi-warden) ![GitHub stars](https://img.shields.io/github/stars/DevMortimer/pi-warden?style=flat) - Pi 護欄，擋不可逆工具、迴圈與假「完成」，由 Jev 導航。跟 pi-jev 很合拍，當你在意安全表演要變成真檢查時。最適合曾被「太早說做完」的 agent 燙過的人。

## 路由器

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - 給 Claude Code 與 Codex 的每回合 cheap／strong 路由——仍是這生態系最常被引用的 router pattern。X 熱度淡於瀏覽器 demo，但實用性夠我們留它。當你以為簡單的回合開始被「便宜」模型搞砸時，盯緊成本回彈。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono 的語意 HTTP 路由：Jev 選路，handler 保持無聊。小而乾淨，證明 System One 不只是 coding agent 玩具。給 Hono／邊緣 API 人；靜態 path 表已夠用就別硬加。

## 資料與函式庫

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - PostgreSQL 擴充，用白話問表，答案走 Jev——少見的「決策模型住在資料旁邊」角度。X 安靜，niche 實用很大聲，對我們夠了。給 SQL 原生團隊；別拿它當完整分析倉儲故事的替代品。

## 值得研究的 Demo

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - 每個 Monad block 對 Kuru MON-USDC 做一次買／賣決策——熱迴圈加校準過的 choice，不是「感覺看多」的聊天機器人。[@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346) 讓這模板傳開。偷它的節奏；別當投資建議，也別當正式交易台。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 用結構化模擬器狀態玩 Mario——玩具表面，認真教訓：能餵觀測狀態就別硬餵像素。我們留它是為了教 action-space 衛生。好玩第一；上線第二（或永遠不上）。


## Use case 與概念展示（觀察中）

**不是正式條目。** 這裡放高討論的 **use case／概念** 展示——讓 System One pattern 可點進去看的帖與文章。偷想法即可；除非另註，不要期待打磨好的 repo。有扎實公開產物後，再考慮升格到上方分類。

### 框架

- [LLMs 產答案，Jev 做決定](https://x.com/paarangatrai/status/2100113737097367896) - 在 X 上站穩的一句心智模型。用來跟隊友解釋 System One；這是框架，不是產品。
- [WTF Is Jev? 九件社群已在做的事](https://x.com/mvanhorn/status/2100784142850097482) - 有收據的模式總覽：給候選（別發明）、快反應／慢規劃、可量測迴圈。當「該看什麼」地圖，不要當複刻清單。
- [用 Jev 組 Harness（LangChain）](https://x.com/sydneyrunkle/status/2100754364545761643) - 架構文：Jev 當 agent 迴圈裡的閘門（路由、高風險 tool）。學 harness 形狀；主產物是 blog／LangChain middleware，不是玩具 demo repo。

### 產品感 Demo（repo 可有可無）

- [意圖 launcher——「我剛下載的 PDF」](https://x.com/dabit3/status/2100756930054504776) - 在有限候選上讀 keystroke 意圖（約 100 ms）。工作碼在 [dabit3/jev-experiments](https://github.com/dabit3/jev-experiments)（`jev-launcher`）；先當 use-case 故事，因為大家引用的是這則帖。
- [預測試算表——欄位標題當 schema](https://x.com/dabit3/status/2100780008193020049) - 「試算表重算數字，不重算意義。」同實驗庫（`judge-sheets`）。很適合 inbox／分流表的隱喻。
- [語音 → Jev → 瀏覽器點擊](https://x.com/moritzkremb/status/2100577979021832365) - 雙手被佔住時的控制迴圈（作者數字約 300 ms／~$0.0002）。影片 demo；未核到公開 repo——只收 pattern。
- [本機 OCR 標籤 → Jev 選點](https://x.com/milindlabs/status/2100631847155994852) - 本地感知、只送文字給 Jev（約 90 ms）。補足上方的 [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use)；不同作者、同一課：可觀測的 action space。未核到 repo。

### 即時／多智能體概念

- [Minecraft：Jev 反應、Astra 規劃](https://x.com/wuyang_zhou/status/2100727660875808913) - 活負載下的快 System One＋慢 System Two 分工。未核到公開 repo；偷角色邊界，別偷片段當藍圖。
- [情緒細胞自動機](https://x.com/riku720720/status/2100738087584481657) - 多個 agent 並行用 Jev 更新狀態——少見的多體概念（不是又一個單人遊戲 bot）。讚數較低；新意較高。

### 流傳中（附保留）

熱、但沒有乾淨可交付物——當雷達，不當食譜：

- [「一小時重做 Tesla FSD」](https://x.com/jpschroeder/status/2100347770867458384) - 極端迴圈敘事；可重現前先當行銷。
- [Subway Surfers＋50 平行局](https://x.com/_MaxBlade/status/2100634359099232678) - 並行決策成本敘事；僅 demo。
- [Slay the Spire 2 約 0.7s 選招](https://x.com/coolish/status/2100570517954838897) - 有限遊戲 action space；僅 demo。
- [貼文病毒分（61 問／SuperX）](https://x.com/robj3d3/status/2100722975645598191) - 並行多問打分的產品試用連結；帖內無公開 GitHub。

## Jev-like 與相關模型

可不呼叫 TypeSafe；收錄看**討論熱度與研究價值**。它們**非官方、非附屬**。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - 家裡 3090 上用開源模型做的「語意 if」——明確獨立，與 TypeSafe **無附屬關係**。X 稀疏（如 [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)），但對想在本機玩條件式的人夠當 inspired-by 參考。給 DIY GPU 玩家；預期研究毛邊，不是拋光 SaaS 雙胞胎。
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 訓練小模型一次通過輸出選項機率（Doom／chess／Wikispeedia）。獨立／inspired-by 教材，X 稀疏但 HN 約 161 分有感。想親自感受 System One 形狀輸出怎麼被學出來就看它；**非** Jev 替身，也**非**附屬。
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - 開源「Jev 配方」（LoRA＋constrained serving）——**非** TypeSafe 附屬；配方本身就是產品。[@madiator](https://x.com/madiator/status/2100990591215783946) 與 HN 都給了熱度。給想自己煮 System One 味模型的團隊；請自備 ML ops 耐心。
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - SGLang 上的 prefill-only、Jev 形狀相容 API——獨立，**非**附屬。HN 討論是門票：serving 形狀跟權重一樣重要。給已住在 SGLang 的 infra 人；把「相容」讀成「形狀像」，不是「官方」。
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - 本機 Gemma／MLX option scoring。與 TypeSafe **無附屬關係**；因 HN 好奇與筆電友善實驗而上榜。給 Apple／本機探索者；分數當教材，別當正式校準。
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - 用 Qwen3 letter-logits 朝 System One 風格選擇的小實驗。獨立、**非**附屬；HN 是它坐在這裡的理由。給拿 stick 戳 logits 的研究者——可愛，不是產品。
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - 透過 MLX 在 Apple Silicon 上做平行決策。**非**附屬；熱度來自 [@beni_il_](https://x.com/beni_il_/status/2100617387116568956) 與 HN。Mac MLX 原生、想追平行 Choice 形呼叫的人首選；評估架請自備。
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 平行 constrained／多字段決策的 HF 模型——獨立，**非** TypeSafe。[@harshagundal](https://x.com/harshagundal/status/2100044305536889015) 的強 X 換到席位。給想下載一顆腦、不要 API key 的人；信任多字段輸出前先驗證約束。
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 把任意 LLM 包成類 Jev 的 `/v1/systemone` 表面。**非**附屬；[@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337) 把 adapter pattern 放到地圖上。協議實驗很方便；記住包裝紙不會魔法變成 System One 品質。

有更多 X／HN 持續討論時歡迎 PR。

## 相關清單

- [awesomejev.com](https://awesomejev.com/) - 大型自動刷新目錄（repos、sites、threads），專門補我們刻意拒絕的廣度。用它掃街發現，回這裡做品味判斷。好搭檔，但別拿它當品味的替代品。
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) ![GitHub stars](https://img.shields.io/github/stars/yibie/awesome-jev?style=flat) - 社群版 Jev awesome list——網更寬、編輯聲比較輕。我們當它是同儕雷達，一起盯社群在長什麼。安靜條目請交叉核對評語再採用。
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) ![GitHub stars](https://img.shields.io/github/stars/AbdelStark/awesome-typesafe?style=flat) - 更廣的 TypeSafe＋System One＋Jev 資源，不只「有打 API 的 app」。給要畫整片地景、而不是只挑旗艦 demo 的人。預期連結密度高於辛辣短評。
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - 長文解釋 SDK、Gateway 與 `evaluate`——你丟給不想開十五個分頁的同事的那一篇。溫暖、務實、帶一點好的主見。最適合 onboarding，不是活目錄。

## 由 Grok Bot 維護

這份清單由 **[Grok Bot](https://grok.com)** 打理（重要取捨會有人類盯一眼）。我們看社群在做什麼、在吵什麼，再把評語寫誠實。

如果這裡幫你上線了什麼 — 或你覺得哪條收錯了 — 開 issue 或 PR 都行。**希望你喜歡。** 附上好討論串、講清楚「為什麼」的 PR，我們會很開心。

## 貢獻

見 [contributing.md](contributing.md)。PR 請附 repo、為什麼有用、命中哪條篩選，以及（若有）公開討論連結。低訊號的「也提到 Jev」會溫柔關閉。

## 授權

[CC0](license) — 隨便分享、fork、改作。跟多數 awesome list 一樣。
