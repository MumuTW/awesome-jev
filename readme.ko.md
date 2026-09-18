# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**언어:** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> [Jev](https://typesafe.ai)(TypeSafe AI System One: 신뢰도 있는 typed 결정) 엄선 목록. 공개 논의 열기가 있으면 **Jev-like** 모델/복제본도 포함.

## 이 목록의 차별점

대형 디렉터리는 **범위**([awesomejev.com](https://awesomejev.com/) 등). 여기는 **판단**.

| 흔한 방식 | 여기 |
| --- | --- |
| 수백 개 스크랩 | 한 번에 읽을 짧은 목록 |
| 마케팅 한 줄 | **편집 노트**(왜 중요한지·주의점) |
| 스타 순위 | **커뮤니티 조사**(측정 루프, X 런치 등) |
| TypeSafe API만 | X/HN 실용 관심이 있는 **Jev-like**도(비공식 표기) |

## 목차

- [이 목록의 차별점](#이-목록의-차별점)
- [선정](#선정-기준)
  - [선정 기준](#선정-기준)
  - [관찰](#관찰)
- [공식 & 플랫폼](#공식)
  - [공식](#공식)
  - [플랫폼](#플랫폼)
- [통합·응용](#브라우저--컴퓨터-사용)
  - [브라우저 & 컴퓨터 사용](#브라우저--컴퓨터-사용)
  - [코딩 에이전트](#코딩-에이전트)
  - [라우터](#라우터)
  - [데이터 & 라이브러리](#데이터--라이브러리)
  - [연구할 만한 데모](#연구할-만한-데모)
- [Jev-like & 관련 모델](#jev-like--관련-모델)
- [관련 목록](#관련-목록)
- [기여](#기여)


## 선정 기준


### 직접 Jev/TypeSafe

다음 중 **2개 이상**: 실제 API/공식, 재사용 패턴, 공개 논의(특히 X).

### Jev-like/관련 모델(Jev 미사용 가능)

**X**(가끔 HN)에서 실용 관심·열기가 보이면 수록. 독립/inspired-by 명시. 스타만으로는 부족.

## 관찰

- **유한·관측 가능한 action space에서 Jev가 강함.** X: [Browser Use](https://x.com/gregpr07/status/2100411066966749359), [computer-use](https://x.com/awlevin/status/2100262612428894676).
- **작은 LLM은 텍스트 생성만.**
- **코딩 용도는 게이트(compaction/review/routing), 작성 아님.**
- **지연 서사 > 스타.** **Star ≠ X:** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction)은 런치 글이 없어도 keep.
- **진입점:** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)([@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)).
- **Jev-like 열기는 신호이지 소속이 아님.**

## 공식

- [TypeSafe](https://typesafe.ai) - 제품 홈 / early access.
- [System One docs](https://docs.typesafe.ai) - 적합한/부적합한 것.
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 공식 TS/JS.
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 공식 Python.
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - LLM 백엔드 drop-in.
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - 공식 skills([@typesafeai](https://x.com/typesafeai/status/2100376436272173088)).
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare 목록.

## 플랫폼

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - AI SDK 7 `evaluate`. [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175).
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - Choice/Score/Boolean.

## 브라우저 & 컴퓨터 사용

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - 플래그십. Flights ~7s/~$0.0039. X: [@gregpr07](https://x.com/gregpr07/status/2100411066966749359).
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS OCR + Jev. X: [@awlevin](https://x.com/awlevin/status/2100262612428894676).
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - 라이브러리형 pilot. 스타 낮고 구조는 탄탄.

**일단 제외:** 새 측정/X 없는 Ultrafast 얇은 래퍼(모바일 포함).

## 코딩 에이전트

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code compaction. 고스타/트렌드로 수록.
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - 팩토리 감독. X: [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717).
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 단계 review. [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556).
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - MCP 우선 시.
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) / [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi 게이트/가드레일.

## 라우터

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - 가장 많이 인용. X는 약해도 실용적이라 수록.
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono 의미 라우터.

## 데이터 & 라이브러리

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - Postgres 확장. X는 약하지만 니치 실용성이 큼.

## 연구할 만한 데모

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - Monad 블록 거래. X: [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346).
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 구조화 상태 Mario.

## Jev-like & 관련 모델

TypeSafe 미사용 가능. **논의 열기·학습 가치**로 판단.

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - 오픈 semantic if. 예: [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010).
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 원패스 선택 확률. X 희소 + HN ~161 pts.
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - 오픈 Jev 레시피(LoRA＋constrained serving). 비공식. X: [@madiator](https://x.com/madiator/status/2100990591215783946); HN.
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - Prefill-only Jev 호환 API(SGLang). 비공식. HN.
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - 로컬 Gemma/MLX option scoring. 비공식. HN.
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - Qwen3 letter-logits 소실험. 비공식. HN.
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - Apple Silicon MLX 병렬 결정. 비공식. X: [@beni_il_](https://x.com/beni_il_/status/2100617387116568956); HN.
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 병렬 constrained/다중 필드(HF). 비공식. 강한 X: [@harshagundal](https://x.com/harshagundal/status/2100044305536889015).
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 임의 LLM을 Jev-like `/v1/systemone`으로. 비공식. X: [@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337).

## 관련 목록

- [awesomejev.com](https://awesomejev.com/) · [yibie/awesome-jev](https://github.com/yibie/awesome-jev) · [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) · [Flavio Copes](https://flaviocopes.com/jev/)

## 기여


## 라이선스

[CC0](license)
