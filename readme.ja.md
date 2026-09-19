# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**言語：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> [Jev](https://typesafe.ai) を素早く掴む — TypeSafe の、型付き意思決定（choice／score／信頼度付き boolean）向けに研いだ「System One」モデル。コミュニティが熱く語る同類モデルも。

400 個の静かな clone の巨大ディレクトリ、飽きましたよね。私たちも。ここは短く保ち、各項目に**ノート**（なぜ重要か・誰向けか・注意点）を付け、**コミュニティ調査**（測定ループ、X の launch、みんなが引用するパターン）に寄せます。次の実装に盗めるものが見つかると嬉しいです。

## このリストの差別化

大規模ディレクトリは**網羅**（[awesomejev.com](https://awesomejev.com/) など）。ここは**センス**。

| よくあるやり方 | ここ |
| --- | --- |
| 数百リポジトリのスクレイプ | コーヒー一杯で読める短さ |
| 宣伝文句の一行 | **編集ノート**（なぜ重要か・注意点） |
| Star 順 | **コミュニティ調査**（測定ループ、X など） |
| TypeSafe API 呼び出しのみ | 熱がある **Jev-like** も（非公式と明記） |
| すべての fork を平等に | パターンごとのベスト；薄い Ultrafast ラッパは見送り |

好きなリストの肩の上で：

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome)／[awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — 収集ではなくキュレーション。
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — スコープが明確で「ここには載せない」が正直。

## 目次

- [このリストの差別化](#このリストの差別化)
- [選定](#選定基準)
  - [選定基準](#選定基準)
  - [観察](#観察)
- [公式とプラットフォーム](#公式)
  - [公式](#公式)
  - [プラットフォーム](#プラットフォーム)
- [連携・応用](#ブラウザコンピュータ操作)
  - [ブラウザ＆コンピュータ操作](#ブラウザコンピュータ操作)
  - [コーディングエージェント](#コーディングエージェント)
  - [ルータ](#ルータ)
  - [データ＆ライブラリ](#データライブラリ)
  - [研究価値のあるデモ](#研究価値のあるデモ)
- [ユースケースと概念（ウォッチ）](#ユースケースと概念ウォッチ)
- [Jev-like と関連モデル](#jev-like-と関連モデル)
- [関連リスト](#関連リスト)
- [Grok Bot がメンテ](#grok-bot-がメンテ)
- [貢献](#貢献)

## 選定基準

二本立て。どちらも厳しめに。

### 直接 Jev／TypeSafe

次のうち **2 つ以上**：実 API／公式、再利用できるパターン、公開議論（特に X）。

### Jev-like／関連モデル（Jev 未使用可）

**X**（時に HN）で実用関心・熱が見えれば収録。独立／inspired-by と明記。Star だけでは不足。

## 観察

- **有限で観測可能な action space のとき Jev が強い。** X: [Browser Use](https://x.com/gregpr07/status/2100411066966749359)、[computer-use](https://x.com/awlevin/status/2100262612428894676)。
- **小さな LLM はテキスト生成のみ。**
- **コーディング用途はゲート（compaction／review／routing）、執筆ではない。**
- **遅延の物語 > Star。** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) は広く引用された launch 投稿がなくても収録する価値がある。
- **入口:** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)）。
- **高熱でも届け物の薄い概念にも価値がある。** [ユースケースと概念（ウォッチ）](#ユースケースと概念ウォッチ) へ——pattern を理解させるスレ／長文であり、fork 先ではない。検証の弱いバイラル flex は入れないか、一言の注意だけ。
- **Jev-like の熱はシグナルであり所属ではない。**

## 公式

- [TypeSafe](https://typesafe.ai) - 本拠地：製品ホームと early-access console。Jev が何を売っているかをいちばん綺麗に体感できる場所です。System One が自社スタックに合うか測るならここから——ドキュメントの山より「触れるか」。注意：early access は、コミュニティのデモより扉が遅いこともまだあります。
- [System One docs](https://docs.typesafe.ai) - 「Jev は何が得意か」へのいちばん鋭い文章。原子的な型付き質問は○、長い System-2 散文は×。良い統合はみな、静かにこの心的モデルを映しています。API クレジットを燃やす前に prompt／schema を設計する人向け。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 公式 TypeScript／JavaScript クライアント（`@typesafe-ai/sdk`）。Node やブラウザに既にいるなら最短の入口。『面白い論文』から本番の typed Choice／Score／Boolean へ運ぶための道として選びました。auth の角を再発見したいとき以外、自前 fetch はおすすめしません。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 同じ System One 面の公式 Python クライアント。ノートブックやエージェントの隣に Jev を置きたいデータ／ML 勢に最適で、TypeScript 必須とは言いません。薄いけれど信頼できる——研究スケッチではなく、公式クライアントとして扱ってください。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - 通常の chat LLM を背後にした drop-in `TypeSafeClient`。本番モデル待ちなしで A／B やオフライン比較ができます。支出を決める前に公平な baseline が欲しいチーム向け。注意：これは代役であり無料の Jev ではない——評価メモに大きく書いて。
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - System One API 向け公式 agent skills。「正しい道具を出してから火を入れる」パック。[@typesafeai](https://x.com/typesafeai/status/2100376436272173088) が本気のビルダーの始め方として枠づけたので収録。空のリポより慣習が欲しいエージェント作者向け。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare の AI プラットフォーム上のホスト済みモデル掲載。ランタイムがすでに Workers 形ならブックマーク価値あり。クライアントスタック所有よりエッジ同居を気にするときに。教程というより「本当にここにある」という領収書。

## プラットフォーム

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - AI SDK 7 の `evaluate` で `typesafe-ai/jev` を呼べる。プライベート waitlist 待ちなし——誰が試せるかを一晩で変えた入口。[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175) がアクセスを脚注ではなく製品の物語にしたので上位に置いています。Next.js／AI SDK 屋さん向け；Gateway の枠は枠のままです。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - ネイティブな Choice／Score／Boolean。System One の答えがアプリコードに住んでいるように見える道。Gateway 項目の人間工学の双子として選定——同じ心的モデル、グルーファイルは少なめ。experimental の名は正直：API はまだ足元で動きます。

## ブラウザ＆コンピュータ操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - Browser Use の旗艦ループで、いまもネット上いちばん明快な「なぜ Jev か」デモ。DOM → 索引化された操作／ターゲット → Jev 一往復、小さな LLM は入力だけ。Zürich→London Flights（約 7s／約 $0.0039）と [@gregpr07](https://x.com/gregpr07/status/2100411066966749359) が遅延の物語を Star 表より遠くへ運びました。有限で観測可能な action space ならこの設計を盗んで；まだ「何でもやれ」エージェントなら見送り。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS の computer-use：OCR + Jev。著者表のコスト（約 $0.0002／step）で人が背筋を伸ばした一本。[@awlevin](https://x.com/awlevin/status/2100262612428894676) がデスクトップ自動化を雰囲気動画ではなく測定可能な System One の話にしたので収録。Mac ネイティブ向け；完璧なアクセシビリティツリーを飛ばす税が OCR ノイズです。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - ライブラリ型 pilot（surface／perception／policy／verify／safety／traces）。Ultrafast をフォークせず自分のループを設計する人向け。Star は静か、構造は静かではない——だからここにある。差し替え可能な継ぎ目が欲しいとき向き；今夜フライト demo が動けばいいなら先に Ultrafast。

**駐車場:** 新測定も X も無い Ultrafast 薄ラッパ（mobile 含む）。

## コーディングエージェント

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code プラグイン。Jev が tool call／結果を採点し、残す文脈は原文のまま——compaction はゲートであり、創作する要約器ではない。広く引用された launch がなくても高 Star／強トレンドなので「観察」でも名指し。tool ノイズに溺れる Claude Code ヘビーユーザー向け；退屈でも必要な長い尻尾を落とさないよう注意。
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - ソフトウェア工場の監督。Jev が各段階を裁く——「PR を書いて」より「このステージは本当に通ったか」。[@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717) の Codex 監督アングルが好きで収録。マルチエージェント工場向け；単発の review ボットだけなら重い。
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 段階的 review とローカル dashboard。コミュニティが好む「ゲートを見せて」形。[@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556) などの roundup 引用で十分な熱。人の目に見える段階が欲しいとき向き；一発 MCP より重い。
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - ローカル優先の MCP `jev_review`。スタックがすでに MCP 形ならこちら。Claude／Cursor ツールが正面玄関ならこの兄弟を；X は段階 review より弱いがそれでよい。注意：MCP の快感が先、dashboard の磨きは後。
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) - Pi 向け意思決定層。tool-call ゲートと `jev_ask` で、動く前に聞く。特定ランタイム内のきれいな「System One＝許可」パターンとして選定。型付き拒否権が欲しい Pi ユーザー向け；単体の汎用コーディングエージェントではない。
- [pi-warden](https://github.com/DevMortimer/pi-warden) ![GitHub stars](https://img.shields.io/github/stars/DevMortimer/pi-warden?style=flat) - 不可逆ツール・ループ・偽の「完了」を防ぐ Pi ガードレール。Jev が舵取り。安全の見世物を本物のチェックにしたいとき pi-jev と相性良し。「早すぎる完了」に焼かれた運用者向け。

## ルータ

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - Claude Code／Codex のターンごと cheap／strong ルーティング。いまも最頻引用のルータパターン。X はブラウザ demo より静かでも、実用で残す。簡単なつもりだったターンが安いモデルに崩されたらコスト回帰に注意。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono の意味的 HTTP ルーティング。Jev がルートを選び、ハンドラは退屈なまま。System One がコーディングエージェント専用玩具ではないことの小さな証明。Hono／エッジ API 向け；静的 path 表で足りるなら過剰。

## データ＆ライブラリ

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - PostgreSQL 拡張。自然言語で表に聞き、答えは Jev——珍しい「意思決定モデルがデータの隣に住む」角度。X は静か、ニッチ実用は大声で、それで十分。SQL ネイティブ向け；分析ウェアハウス物語の代替にはしないで。

## 研究価値のあるデモ

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - Monad ブロックごとに Kuru MON-USDC の売買を一回——熱いループと校正された choice。「強気っぽい」チャットボットではない。[@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346) が型を運んだ。リズムを盗んで；投資助言や本番デスクにはしないで。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 構造化されたエミュレータ状態から Mario。おもちゃの表面に本気の教訓：できるなら画素ではなく観測状態を食え。action-space の衛生教育用に残しています。楽しさ第一；本番は第二（または永遠に来ない）。

## ユースケースと概念（ウォッチ）

**正式エントリではない。** 議論の熱い **ユースケース／概念** のショーケース——System One の pattern を「見て分かる」スレと記事。アイデアを盗めばよい；注記がなければ磨かれた repo を期待しない。しっかりした公開成果が出たら上の分類へ昇格することもある。

### フレーミング

- [LLM は答えを生成し、Jev は決断する](https://x.com/paarangatrai/status/2100113737097367896) - X で刺さった一行のメンタルモデル。チームに System One を説明する枠。製品ではない。
- [WTF Is Jev? すでに作られている 9 のこと](https://x.com/mvanhorn/status/2100784142850097482) - 証拠つきパターン地図：候補を渡す（発明しない）、速い反応／遅い計画、測定ループ。複製チェックリストにしない。
- [Jev で Harness を組む（LangChain）](https://x.com/sydneyrunkle/status/2100754364545761643) - アーキ文：エージェントループ内のゲート（ルーティング、危険な tool）。形を学べ；主成果は blog／middleware、玩具 demo ではない。

### プロダクト感デモ（repo は任意）

- [意図ランチャー——「さっき落とした PDF」](https://x.com/dabit3/status/2100756930054504776) - 有限候補上の keystroke 意図（約 100 ms）。コードは [dabit3/jev-experiments](https://github.com/dabit3/jev-experiments)（`jev-launcher`）。まず use-case 物語として——人々が引用するのはこのスレ。
- [予測スプレッドシート——列見出しが schema](https://x.com/dabit3/status/2100780008193020049) - 「表は数字を再計算するが、意味は再計算しない。」同実験 repo（`judge-sheets`）。inbox／振り分け表のメタファーが強い。
- [音声 → Jev → ブラウザクリック](https://x.com/moritzkremb/status/2100577979021832365) - 両手が塞がっているときの制御ループ（著者数字 約 300 ms／~$0.0002）。動画 demo；公開 repo 未確認——pattern のみ。
- [端末 OCR ラベル → Jev が選んでクリック](https://x.com/milindlabs/status/2100631847155994852) - ローカル知覚、Jev へは文字のみ（約 90 ms）。掲載の [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) を補完；別作者、同じ「観測可能な action space」の教訓。repo 未確認。

### リアルタイム／マルチエージェント概念

- [Minecraft：Jev が反応、Astra が計画](https://x.com/wuyang_zhou/status/2100727660875808913) - ライブ負荷下の速い System One＋遅い System Two。公開 repo 未確認；役割境界を盗め、クリップを青写真にするな。
- [感情セルオートマトン](https://x.com/riku720720/status/2100738087584481657) - 多数 agent が並行に Jev で状態更新——珍しい多体概念（単機ゲーム bot の繰り返しではない）。いいねは低め、新規性は高め。

### 流通中（注釈つき）

熱いがきれいな届け物がない——レーダーでありレシピではない：

- [「1 時間で Tesla FSD を作り直した」](https://x.com/jpschroeder/status/2100347770867458384) - 極端なループ話；再現できるまでマーケ扱い。
- [Subway Surfers＋50 並列](https://x.com/_MaxBlade/status/2100634359099232678) - 並列意思決定コストの物語；demo のみ。
- [Slay the Spire 2 約 0.7s 選択](https://x.com/coolish/status/2100570517954838897) - 有限ゲーム action space；demo のみ。
- [バイラル投稿スコア（61 問／SuperX）](https://x.com/robj3d3/status/2100722975645598191) - 並列マルチ質問スコアの試用リンク；スレ内に公開 GitHub なし。


## Jev-like と関連モデル

TypeSafe 未使用可。**議論の熱と学習価値**で判断。いずれも**非公式・非提携**。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - 自宅 3090 上のオープンモデルによる「semantic if」。明示的に独立、TypeSafe とは**無関係**。X は疎（例: [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)）でも、ローカル条件分岐を弄りたい人への inspired-by には足りる。DIY GPU 向け；研究の角は残る、磨かれた SaaS 双子ではない。
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 小モデルを一パス選択肢確率向けに学習（Doom／chess／Wikispeedia）。独立／inspired-by の教材。X 疎＋HN 約 161 pts。System One 形の出力がどう学ばれるかを感じたい人に；**Jev の代替ではなく、提携でもない**。
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - オープンな「Jev レシピ」（LoRA＋constrained serving）。TypeSafe **非提携**；レシピ自体が製品。[@madiator](https://x.com/madiator/status/2100990591215783946) と HN が熱をくれた。自前で System One 味を煮たいチーム向け；ML ops の忍耐を持参。
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - SGLang 上の prefill-only、Jev 互換形 API。独立・**非提携**。HN 議論が入場券：serving 形は重みと同じくらい大事。「互換」は「形が似ている」であり「公式」ではない。SGLang 住民の infra 向け。
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - ローカル Gemma／MLX の option scoring。TypeSafe **非提携**；HN の好奇心とノート PC 実験向きで掲載。Apple／ローカル探索者向け；スコアは教材、本番校正ではない。
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - Qwen3 letter-logits の小さな実験。独立・**非提携**；HN が席の理由。logits を突く研究者向け——愛らしいが製品ではない。
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - Apple Silicon 上 MLX による並列決定。**非提携**；[@beni_il_](https://x.com/beni_il_/status/2100617387116568956) と HN の熱。並列 Choice 形を追う Mac MLX ネイティブ向け；評価ハーネスは自前で。
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 並列 constrained／多フィールド決定の HF モデル。独立・TypeSafe **非提携**。[@harshagundal](https://x.com/harshagundal/status/2100044305536889015) の強い X が席を取った。API キーよりダウンロード脳が欲しい人向け；多フィールド出力は制約を検証してから信じて。
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 任意 LLM を Jev-like の `/v1/systemone` 面に包む。**非提携**；[@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337) がアダプタパターンを地図に載せた。プロトコル実験に便利；ラッパは魔法で System One 品質にはならない。

## 関連リスト

- [awesomejev.com](https://awesomejev.com/) - 自動更新の大きなディレクトリ（repos／sites／threads）。こちらがわざと拒む網羅が欲しいときに。発見はそこで、判断はここに戻って。良い相棒だが、センスの代用品ではない。
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) ![GitHub stars](https://img.shields.io/github/stars/yibie/awesome-jev?style=flat) - コミュニティの Jev awesome list。網は広く、編集の声はこちらより軽い。同輩レーダーとして好き。静かな項目はノートを交差確認してから。
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) ![GitHub stars](https://img.shields.io/github/stars/AbdelStark/awesome-typesafe?style=flat) - TypeSafe＋System One＋Jev をもっと広く。API を呼ぶアプリ以外も含む風景図向け。辛口短評よりリンク密度が高い想定。
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - SDK・Gateway・`evaluate` の長文解説。タブを十五枚開きたくない同僚に渡す一枚。温かく実務的で、良い意味で少し意見がある。オンボーディング向き；生きたカタログではない。

## Grok Bot がメンテ

このリストは **[Grok Bot](https://grok.com)** が世話しています（大事な判断は人間も一瞥）。コミュニティが作り、議論しているものを見て、ノートを正直に保ちます。

役に立ったら — あるいは異論があったら — issue や PR をどうぞ。**気に入ってもらえると嬉しいです。** 良いスレッドと「なぜ」がはっきりした PR 大歓迎。

## 貢献

[contributing.md](contributing.md) を参照。repo・有用な理由・選定基準・（あれば）公開スレッドを。

## ライセンス

[CC0](license) — 共有・fork・改変どうぞ。他の awesome list と同じ精神です。
