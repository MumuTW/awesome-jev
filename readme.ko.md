# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**언어:** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> [Jev](https://typesafe.ai)를 빠르게 파악 — TypeSafe가 타입드 결정(choice·score·신뢰도 있는 boolean)용으로 벼린 「System One」 모델, 그리고 커뮤니티가 뜨거울 때 볼 만한 동류 모델.

조용한 clone 400개짜리 거대 디렉터리, 지겹죠? 우리도요. 목록은 짧게 두고, 항목마다 **노트**(왜 중요한지·누구용인지·주의점)를 달며, **커뮤니티 조사**(측정 루프, X 런치, 사람들이 인용하는 패턴)에 기대요. 다음 주에 바로 훔쳐 쓸 무언가를 찾으면 좋겠어요.

## 이 목록의 차별점

대형 디렉터리는 **범위**([awesomejev.com](https://awesomejev.com/) 등). 여기는 **취향**.

| 흔한 방식 | 여기 |
| --- | --- |
| 수백 개 스크랩 | 커피 한 잔에 끝나는 짧은 목록 |
| 마케팅 한 줄 | **편집 노트** — 왜 중요한지·주의점·누구용 |
| 스타 순위 | **커뮤니티 조사** — 측정 루프, X 런치 등 |
| TypeSafe API만 | 열기 있는 **Jev-like**도(비공식 표기) |
| 모든 fork 평등 | 패턴별 베스트; 얇은 Ultrafast 래퍼는 패스 |

좋아하는 목록의 어깨 위에서:

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome)／[awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — 수집이 아니라 큐레이션.
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — 범위가 뚜렷하고 ‘여기엔 안 넣음’이 솔직함.

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
- [Grok Bot이 유지보수](#grok-bot이-유지보수)
- [기여](#기여)

## 선정 기준

두 트랙. 둘 다 까다롭게.

### 직접 Jev/TypeSafe

다음 중 **2개 이상**: 실제 API/공식, 재사용 패턴, 공개 논의(특히 X).

### Jev-like/관련 모델(Jev 미사용 가능)

**X**(가끔 HN)에서 실용 관심·열기가 보이면 수록. 독립/inspired-by 명시. 스타만으로는 부족.

## 관찰

- **유한·관측 가능한 action space에서 Jev가 강함.** X: [Browser Use](https://x.com/gregpr07/status/2100411066966749359), [computer-use](https://x.com/awlevin/status/2100262612428894676).
- **작은 LLM은 텍스트 생성만.**
- **코딩 용도는 게이트(compaction/review/routing), 작성 아님.**
- **지연 서사 > 스타.** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction)은 널리 인용된 런치 글이 없어도 수록할 만하다.
- **진입점:** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway)([@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)).
- **Jev-like 열기는 신호이지 소속이 아님.**

## 공식

- [TypeSafe](https://typesafe.ai) - 모함: 제품 홈과 early-access console. Jev가 무엇을 파는지 가장 깔끔하게 느껴 보는 곳. System One이 우리 스택에 맞는지 재볼 때 여기서 시작하세요 — 문서 산더미보다 「만져볼 수 있나」. 주의: early access는 커뮤니티 데모보다 문이 느릴 수 있어요.
- [System One docs](https://docs.typesafe.ai) - 「Jev는 어디에 센가」에 대한 가장 날카로운 글. 원자적 타입 질문은 ○, 긴 System-2 산문은 ×. 좋은 통합은 모두 조용히 이 멘탈 모델을 비춥니다. API 크레딧을 태우기 전에 prompt/schema를 설계하는 사람용.
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - 공식 TypeScript/JavaScript 클라이언트(`@typesafe-ai/sdk`). 앱이 이미 Node나 브라우저에 있다면 가장 짧은 진입로. 「흥미로운 논문」에서 프로덕션 typed Choice/Score/Boolean까지 데려가는 길로 골랐어요. auth 모서리를 다시 발견하고 싶을 때만 DIY fetch를 하세요.
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - 같은 System One 면의 공식 Python 클라이언트. 노트북·에이전트 옆에 Jev를 두고 싶은 데이터/ML 사람에게 최고이고, TypeScript 필수는 아닙니다. 얇지만 믿을 만함 — 연구 스케치가 아니라 축복받은 클라이언트로 다루세요.
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - 일반 chat LLM을 백엔드로 한 drop-in `TypeSafeClient`. 진짜 모델을 기다리지 않고 A/B·오프라인 비교 가능. 지출을 정하기 전 공정한 baseline이 필요한 팀용. 주의: 대역이지 무료 Jev가 아님 — 평가 노트에 크게 쓰세요.
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - System One API용 공식 agent skills. 「올바른 도구를 꺼낸 뒤 불을 켜라」 팩. [@typesafeai](https://x.com/typesafeai/status/2100376436272173088)가 진지한 빌더의 시작법으로 프레임해서 수록. 빈 레포보다 관례가 필요한 에이전트 작가용.
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Cloudflare AI 플랫폼의 호스팅 모델 목록. 런타임이 이미 Workers 형태면 북마크 가치. 클라이언트 스택 소유보다 엣지 동거가 중요할 때. 튜토리얼이라기보다 「여기 정말 있다」는 영수증.

## 플랫폼

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - AI SDK 7 `evaluate`로 `typesafe-ai/jev` 호출. 비공개 waitlist 대기 없이 — 누가 실험할 수 있는지를 하룻밤 바꾼 진입로. [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)가 접근을 각주가 아니라 제품 이야기로 만들어 위에 둡니다. Next.js/AI SDK 숍용; Gateway 쿼터는 여전히 쿼터.
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - 네이티브 Choice/Score/Boolean. System One 답이 앱 코드에 이미 사는 것처럼 보이는 길. Gateway 항목의 인체공학 쌍둥이로 선정 — 같은 멘탈 모델, 글루 파일은 적게. experimental 이름은 솔직함: API는 아직 발밑에서 움직입니다.

## 브라우저 & 컴퓨터 사용

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - Browser Use 플래그십 루프이자, 여전히 인터넷에서 가장 선명한 「왜 Jev인가」 데모. DOM → 인덱싱된 ops/targets → Jev 한 왕복, 작은 LLM은 타이핑만. Zürich→London Flights(~7s/~$0.0039)와 [@gregpr07](https://x.com/gregpr07/status/2100411066966749359)가 지연 서사를 스타 차트보다 멀리 보냈어요. 유한·관측 가능한 action space면 이 설계를 훔치세요; 아직 「뭐든 해」 에이전트면 패스.
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS computer-use: OCR + Jev. 저자 표의 비용(~$0.0002/step)에 사람들이 허리를 편 글. [@awlevin](https://x.com/awlevin/status/2100262612428894676)이 데스크톱 자동화를 분위기 영상이 아니라 측정 가능한 System One 이야기로 만들어 수록. Mac 네이티브용; 완벽한 접근성 트리를 건너뛴 세금이 OCR 노이즈입니다.
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - 라이브러리형 pilot(surface·perception·policy·verify·safety·traces). Ultrafast를 포크하지 않고 루프를 설계하는 사람용. 스타는 조용하고 구조는 안 조용함 — 그래서 여기 있어요. 갈아끼울 이음매가 필요하면 선택; 오늘 밤 항공권 데모만 되면 Ultrafast 먼저.

**주차장:** 새 측정/X 없는 Ultrafast 얇은 래퍼(모바일 포함).

## 코딩 에이전트

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code 플러그인. Jev가 tool call/결과를 채점하고 남긴 컨텍스트는 원문 유지 — compaction은 게이트이지, 지어내는 요약기가 아님. 널리 인용된 런치가 없어도 고스타/강세 트렌드라 「관찰」에서도 이름 부름. tool 소음에 빠진 Claude Code 헤비 유저용; 지루해도 필요한 긴 꼬리를 너무 세게 자르지 마세요.
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - 소프트웨어 팩토리 감독. Jev가 단계마다 심판 — 「PR 써 줘」보다 「이 스테이지 진짜 통과했나」. [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717)의 Codex 감독 각도가 좋아 수록. 멀티 에이전트 팩토리용; 단일 review 봇만 필요하면 과함.
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - 단계적 review + 로컬 dashboard. 커뮤니티가 좋아하는 「게이트를 보여 줘」 형태. [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556) 같은 roundup 인용으로 열기 충분. 사람 눈에 보이는 단계가 필요하면; 한 방 MCP보다 무겁습니다.
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - 로컬 우선 MCP `jev_review`. 스택이 이미 MCP 형태면 이쪽. Claude/Cursor 도구가 정문이면 이 형제; X는 단계 review보다 약해도 괜찮아요. 주의: MCP 쾌감이 먼저, dashboard 광택은 나중.
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) - Pi용 결정 레이어. tool-call 게이트 + `jev_ask`로 움직이기 전에 묻게 함. 특정 런타임 안의 깔끔한 「System One = 허가」 패턴으로 선정. 타입드 거부권이 필요한 Pi 사용자용; 단독 범용 코딩 에이전트는 아님.
- [pi-warden](https://github.com/DevMortimer/pi-warden) ![GitHub stars](https://img.shields.io/github/stars/DevMortimer/pi-warden?style=flat) - 되돌릴 수 없는 도구·루프·가짜 「완료」를 막는 Pi 가드레일. Jev가 조향. 안전 쇼를 진짜 체크로 만들고 싶을 때 pi-jev와 잘 맞음. 「너무 일찍 끝냈다」에 데인 운영자용.

## 라우터

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - Claude Code/Codex용 턴마다 cheap/strong 라우팅. 여전히 가장 많이 인용되는 라우터 패턴. X는 브라우저 데모보다 조용해도 실용으로 남김. 「쉬운」 턴이 싼 모델에 무너지면 비용 회귀를 보세요.
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Hono 의미론적 HTTP 라우팅. Jev가 경로를 고르고 핸들러는 지루하게. System One이 코딩 에이전트 장난감만이 아님을 보여 주는 작은 증명. Hono/엣지 API용; 정적 path 표로 충분하면 과함.

## 데이터 & 라이브러리

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - PostgreSQL 확장. 평문으로 테이블에 묻고 답은 Jev — 드문 「결정 모델이 데이터 옆에 산다」 각도. X는 조용하고 니치 실용은 커서 충분. SQL 네이티브 팀용; 분석 웨어하우스 이야기의 대체재는 아님.

## 연구할 만한 데모

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - Monad 블록마다 Kuru MON-USDC 매수/매도 한 번 — 뜨거운 루프 + 보정된 choice. 「강세 느낌」 챗봇이 아님. [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346)가 템플릿을 실어 날림. 리듬을 훔치세요; 투자 조언·프로덕션 데스크로는 쓰지 마세요.
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - 구조화된 에뮬레이터 상태로 Mario. 장난감 표면에 진지한 교훈: 가능하면 픽셀이 아니라 관측 상태를 먹이세요. action-space 위생 교육용으로 남김. 재미가 1순위; 프로덕션은 2순위(또는 영원히 없음).

## Jev-like & 관련 모델

TypeSafe 미사용 가능. **논의 열기·학습 가치**로 판단. 모두 **비공식·비제휴**.

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - 집 3090에서 오픈 모델로 만든 「semantic if」. 명시적으로 독립, TypeSafe와 **무관**. X는 희소(예: [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010))해도 로컬 조건문을 만지고 싶은 사람에게 inspired-by로 충분. DIY GPU용; 연구 모서리는 남고, 닦인 SaaS 쌍둥이는 아님.
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - 원패스 선택 확률용 소모델 학습(Doom/chess/Wikispeedia). 독립/inspired-by 교재. X 희소 + HN ~161 pts. System One 형태 출력이 어떻게 학습되는지 느끼고 싶을 때; **Jev 대체재도, 제휴도 아님**.
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - 오픈 「Jev 레시피」(LoRA＋constrained serving). TypeSafe **비제휴**; 레시피 자체가 제품. [@madiator](https://x.com/madiator/status/2100990591215783946)와 HN이 열기를 줌. System One 맛을 직접 끓이려는 팀용; ML ops 인내를 가져오세요.
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - SGLang 위 prefill-only Jev 호환형 API. 독립·**비제휴**. HN 논의가 입장권: serving 형태는 가중치만큼 중요. 「호환」은 「모양이 비슷」이지 「공식」이 아님. SGLang 주민 infra용.
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - 로컬 Gemma/MLX option scoring. TypeSafe **비제휴**; HN 호기심과 노트북 실험용으로 수록. Apple/로컬 탐험가용; 점수는 교재, 프로덕션 보정이 아님.
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - Qwen3 letter-logits 소실험. 독립·**비제휴**; HN이 자리 이유. logits를 찌르는 연구자용 — 귀엽지만 제품 아님.
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - Apple Silicon MLX 병렬 결정. **비제휴**; [@beni_il_](https://x.com/beni_il_/status/2100617387116568956)와 HN 열기. 병렬 Choice형을 쫓는 Mac MLX 네이티브용; 평가 하네스는 직접.
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - 병렬 constrained/다중 필드 결정 HF 모델. 독립·TypeSafe **비제휴**. [@harshagundal](https://x.com/harshagundal/status/2100044305536889015)의 강한 X가 자리를 삼. API 키보다 다운로드 뇌가 필요할 때; 다중 필드 출력은 제약을 검증한 뒤 믿으세요.
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - 임의 LLM을 Jev-like `/v1/systemone` 면으로 감쌈. **비제휴**; [@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337)가 어댑터 패턴을 지도에 올림. 프로토콜 실험에 편리; 래퍼가 마법으로 System One 품질이 되지는 않음.

## 관련 목록

- [awesomejev.com](https://awesomejev.com/) - 자동 새로고침 대형 디렉터리(repos·sites·threads). 우리가 일부러 거절하는 범위가 필요할 때. 발견은 거기서, 결정은 여기로. 좋은 동반자이지 취향의 대체재는 아님.
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) ![GitHub stars](https://img.shields.io/github/stars/yibie/awesome-jev?style=flat) - 커뮤니티 Jev awesome list. 그물은 넓고 편집 목소리는 우리보다 가벼움. 동료 레이더로 좋아함. 조용한 항목은 노트를 교차 확인하세요.
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) ![GitHub stars](https://img.shields.io/github/stars/AbdelStark/awesome-typesafe?style=flat) - TypeSafe+System One+Jev를 더 넓게. API 호출 앱 너머 지형도용. 매운 한 줄보다 링크 밀도가 높을 예상.
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - SDK·Gateway·`evaluate` 장문 해설. 탭 열다섯 개 싫다는 동료에게 건네는 한 장. 따뜻하고 실무적이며, 좋은 의미로 조금 의견 있음. 온보딩용; 살아있는 카탈로그는 아님.

## Grok Bot이 유지보수

이 목록은 **[Grok Bot](https://grok.com)** 이 돌봅니다(중요한 선택은 사람이 한 번 봐요). 커뮤니티가 만들고 이야기하는 걸 보고, 노트를 솔직하게 유지해요.

도움이 됐거나 의견이 다르면 issue나 PR 주세요. **마음에 들면 좋겠어요.** 좋은 스레드와 명확한 ‘왜’가 있는 PR은 환영합니다.

## 기여

[contributing.md](contributing.md) 참고. repo, 유용한 이유, 선정 기준, (있으면) 공개 스레드를 적어 주세요.

## 라이선스

[CC0](license) — 공유·fork·개작 자유. 다른 awesome list와 같은 정신입니다.
