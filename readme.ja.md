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
- **遅延の物語 > Star。** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) は広く引用された launch 投稿がなくても収録する価値がある。
- **入口:** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)（[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)）。
- **Jev-like の熱はシグナルであり所属ではない。**

## 公式

- [TypeSafe](https://typesafe.ai) - 製品ホームと early access。
- [System One docs](https://docs.typesafe.ai) - 向き／不向き。
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 公式 TS／JS。
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 公式 Python。
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - LLM バックエンドの drop-in。
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - 公式 skills（[@typesafeai](https://x.com/typesafeai/status/2100376436272173088)）。
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare 掲載。

## プラットフォーム

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - AI SDK 7 `evaluate`。[@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)。
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - Choice／Score／Boolean。

## ブラウザ＆コンピュータ操作

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - 旗艦ループ。Flights ~7s／~$0.0039。X: [@gregpr07](https://x.com/gregpr07/status/2100411066966749359)。
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS OCR + Jev。X: [@awlevin](https://x.com/awlevin/status/2100262612428894676)。
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - ライブラリ型 pilot。Star 低・構造は強い。

**当面スキップ:** 新測定も X も無い Ultrafast 薄ラッパ（mobile 含む）。

## コーディングエージェント

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code compaction。高 Star／トレンドで収録。
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - ファクトリ監督。X: [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717)。
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 段階 review。[@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556)。
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - MCP 優先時。
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) / [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi 向けゲート／ガード。

## ルータ

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - 最も引用されるルータ。X は弱めでも実用で収録。
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono 意味ルータ。

## データ＆ライブラリ

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - Postgres 拡張。X 弱・ニッチ実用で収録。

## 研究価値のあるデモ

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - Monad ブロック取引。X: [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346)。
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 構造化状態の Mario。

## Jev-like と関連モデル

TypeSafe 未使用可。**議論の熱と学習価値**で判断。

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - オープンな semantic if。例: [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)。
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 一パス選択肢確率。X 疎 + HN ~161 pts。
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - オープンな Jev レシピ（LoRA＋constrained serving）。非公式。X: [@madiator](https://x.com/madiator/status/2100990591215783946); HN も。
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - Prefill-only の Jev 互換 API（SGLang）。非公式。HN。
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - ローカル Gemma/MLX option scoring。非公式。HN。
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - Qwen3 letter-logits の小実験。非公式。HN。
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - Apple Silicon MLX 並列決定。非公式。X: [@beni_il_](https://x.com/beni_il_/status/2100617387116568956); HN。
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 並列 constrained／多フィールド（HF）。非公式。強い X: [@harshagundal](https://x.com/harshagundal/status/2100044305536889015)。
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 任意 LLM を Jev-like `/v1/systemone` に。非公式。X: [@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337)。

## 関連リスト

- [awesomejev.com](https://awesomejev.com/) · [yibie/awesome-jev](https://github.com/yibie/awesome-jev) · [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) · [Flavio Copes](https://flaviocopes.com/jev/)

## 貢献

## ライセンス

[CC0](license)
