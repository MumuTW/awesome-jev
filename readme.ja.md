# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**言語：** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> [Jev](https://typesafe.ai)（TypeSafe AI の System One：信頼度付き typed 決定）向けの厳選リスト。公開議論で熱がある **Jev-like** モデル／レプリカも含む。

## このリストの差別化

大規模ディレクトリは**網羅**（[awesomejev.com](https://awesomejev.com/) など）。ここは**判断**。

| よくあるやり方 | ここ |
| --- | --- |
| 数百リポジトリのスクレイプ | 一度で読める短いリスト |
| 宣伝文句の一行 | **編集ノート**（なぜ重要か・注意点） |
| Star 順 | **コミュニティ調査**（測定ループ、X の launch など） |
| TypeSafe API 呼び出しのみ | X／HN で実用関心がある **Jev-like** も（非公式と明記） |

## 目次

- [選定基準](#選定基準)
- [観察](#観察)
- [公式](#公式)
- [プラットフォーム](#プラットフォーム)
- [ブラウザ＆コンピュータ操作](#ブラウザコンピュータ操作)
- [コーディングエージェント](#コーディングエージェント)
- [ルータ](#ルータ)
- [データ＆ライブラリ](#データライブラリ)
- [研究価値のあるデモ](#研究価値のあるデモ)
- [Jev-like と関連モデル](#jev-like-と関連モデル)
- [関連リスト](#関連リスト)
- [貢献](#貢献)

## 選定基準

### 直接 Jev／TypeSafe

次のうち **2 つ以上**：実 API／公式、再利用できるパターン、公開議論（特に X）。

### Jev-like／関連モデル（Jev 未使用可）

**X**（時に HN）で実用関心・熱が見えれば収録。独立／inspired-by と明記。Star だけでは不足。

## 観察

- **有限で観測可能な action space のとき Jev が強い。** X: [Browser Use](https://x.com/gregpr07/status/2100411066966749359)、[computer-use](https://x.com/awlevin/status/2100262612428894676)。
- **小さな LLM はテキスト生成のみ。**
- **コーディング用途はゲート（compaction／review／routing）、執筆ではない。**
- **遅延の物語 > Star。** **Star ≠ X:** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) は launch 投稿が見つからなくても keep。
- **入口:** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)）。
- **Jev-like の熱はシグナルであり所属ではない。**

## 公式

- [TypeSafe](https://typesafe.ai) - 製品ホームと early access。
- [System One docs](https://docs.typesafe.ai) - 向き／不向き。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) - 公式 TS／JS。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) - 公式 Python。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) - LLM バックエンドの drop-in。
- [skills](https://github.com/typesafe-ai/skills) - 公式 skills（[@typesafeai](https://x.com/typesafeai/status/2100376436272173088)）。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare 掲載。

## プラットフォーム

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - AI SDK 7 `evaluate`。[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - Choice／Score／Boolean。

## ブラウザ＆コンピュータ操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) - 旗艦ループ。Flights ~7s／~$0.0039。X: [@gregpr07](https://x.com/gregpr07/status/2100411066966749359)。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) - macOS OCR + Jev。X: [@awlevin](https://x.com/awlevin/status/2100262612428894676)。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) - ライブラリ型 pilot。Star 低・構造は強い。

**当面スキップ:** 新測定も X も無い Ultrafast 薄ラッパ（mobile 含む）。

## コーディングエージェント

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) - Claude Code compaction。高 Star／トレンドで keep。
- [foreman](https://github.com/thruwire/foreman) - ファクトリ監督。X: [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717)。
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) - 段階 review。[@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556)。
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) - MCP 優先時。
- [pi-jev](https://github.com/y0usaf/pi-jev) / [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi 向けゲート／ガード。

## ルータ

- [jev-router](https://github.com/gargpratyush/jev-router) - 最も引用されるルータ。X は弱めでも実用で keep。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) - Hono 意味ルータ。

## データ＆ライブラリ

- [pg-jev](https://github.com/realZachi/pg-jev) - Postgres 拡張。X 弱・ニッチ実用で keep。

## 研究価値のあるデモ

- [jev-trader](https://github.com/jarrodwatts/jev-trader) - Monad ブロック取引。X: [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346)。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) - 構造化状態の Mario。

## Jev-like と関連モデル

TypeSafe 未使用可。**議論の熱と学習価値**で判断。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) - オープンな semantic if。例: [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)。
- [jevlike](https://github.com/vinnylarouge/jevlike) - 一パス選択肢確率。X 疎 + HN ~161 pts。

## 関連リスト

- [awesomejev.com](https://awesomejev.com/) · [yibie/awesome-jev](https://github.com/yibie/awesome-jev) · [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) · [Flavio Copes](https://flaviocopes.com/jev/)

## 貢献

[contributing.md](contributing.md)。マージの正本は英語 `readme.md`。

## ライセンス

[CC0](license)
