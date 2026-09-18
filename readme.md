# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**Languages:** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> Get Jev fast — TypeSafe’s sharp “System One” model for typed decisions (choice, score, boolean with confidence) — plus kindred models worth watching when the community is buzzing.

Tired of mega-directories with 400 quiet clones? Same. This list stays small, ships **notes** (why it matters, who it's for, what to watch), and leans on **community research** — measured loops, launch threads on X, patterns people keep quoting. Hope you find something worth stealing for your next build.

## What makes this list different

Mega-directories already cover **breadth** ([awesomejev.com](https://awesomejev.com/), [yibie/awesome-jev](https://github.com/yibie/awesome-jev), [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)). We cover **taste**.

| Others often do | We do |
| --- | --- |
| Scrape / mirror hundreds of repos | A short list you can finish with coffee |
| One-line marketing blurbs | **Editorial notes** — why it matters, caveats, who it is for |
| Stars as the ranking signal | **Community research** — measured loops, launch threads (especially X), patterns people actually quote |
| Only “calls TypeSafe API” | Also **Jev-like / related models** when X (or HN) shows real interest — clearly labeled not TypeSafe |
| Treat every fork as equal | Best-in-class per pattern; thin Ultrafast wrappers get a polite pass |

Standing on the shoulders of lists we like:

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome) / [awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — curation over collection; high bar; say *why* something is awesome.
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — sharp scope, honest “not here” buckets.

## Contents

- [What makes this list different](#what-makes-this-list-different)
- [Curation](#how-we-curate)
  - [How we curate](#how-we-curate)
  - [Observations](#observations)
- [Official & platforms](#official)
  - [Official](#official)
  - [Platforms](#platforms)
- [Integrations](#browser--computer-use)
  - [Browser & computer use](#browser--computer-use)
  - [Coding agents](#coding-agents)
  - [Routers](#routers)
  - [Data & libraries](#data--libraries)
  - [Demos worth studying](#demos-worth-studying)
- [Jev-like & related models](#jev-like--related-models)
- [Related lists](#related-lists)
- [Maintained by Grok Bot](#maintained-by-grok-bot)
- [Contributing](#contributing)

## How we curate

Two tracks. Be picky on both.

### Direct Jev / TypeSafe

In when **at least two** are true:

1. Real TypeSafe / Jev API usage (or official docs / SDK), not a name collision.
2. You could ship or steal a pattern from it this week (cost, latency, action space, routing, review).
3. Public discussion beyond a quiet README (launch threads, cost/latency numbers, forks that cite it).

### Jev-like / related models (may not call Jev)

In when public discussion (especially **X**, sometimes HN) signals **practical interest or heat**, even if the project never calls TypeSafe. Label clearly as independent / inspired-by. Stars alone are not enough; a quoted thread or measured demo usually is.

Out: dump directories, unused renames, thin Ultrafast clones, and name collisions. If similar to an existing entry, argue in the PR **how it is better**.

## Observations

- **Jev wins when the action space is finite and observed.** Projects that moved the needle on X ([Browser Use flights](https://x.com/gregpr07/status/2100411066966749359), [Mac computer-use cost](https://x.com/awlevin/status/2100262612428894676)) turn the world into an indexed table, then ask one parallel pass. Free-form “do whatever” agents are the wrong fit.
- **Small LLM only for text generation.** Ultrafast and computer-use keep a text model for typing. That split is the recurring architecture.
- **Coding-agent use is about gates, not authorship.** Compaction, review, tool allow/deny, and model routing are natural System One jobs.
- **Latency narratives travel farther than star counts.** Prefer measured loops. [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) is listed for trend and usefulness even without a widely cited launch thread.
- **Access path matters.** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) (`typesafe-ai/jev`) changed who could experiment overnight ([@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)).
- **Jev-like heat is a signal, not affiliation.** SemIf / jevlike teach open alternatives; X/HN chatter is why they sit here — always label independent.

## Official

- [TypeSafe](https://typesafe.ai) - The mothership: product home, early-access console, and the cleanest place to feel what Jev is selling. Start here if you are evaluating whether System One fits your stack — less “docs dump,” more “can I try this.” Caveat: early access still means some doors open slower than the community demos imply.
- [System One docs](https://docs.typesafe.ai) - The sharpest written answer to “what is Jev good at?” Atomic typed questions yes; long System-2 prose no. We list it because every good integration quietly mirrors this mental model. Ideal for architects drafting prompts and schemas before they burn API credits.
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-js?style=flat) - Official TypeScript/JavaScript client (`@typesafe-ai/sdk`) — the default on-ramp if your app already lives in Node or the browser. Selected because it is the path of least resistance from “interesting paper” to typed Choice/Score/Boolean in production code. Skip the DIY fetch wrappers unless you enjoy rediscovering auth edge cases.
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/typesafe-sdk-python?style=flat) - Official Python client for the same System One surface. Best for data/ML folks who want Jev beside notebooks and agents without pretending TypeScript is mandatory. Thin but trustworthy — treat it as the blessed client, not a research sketch.
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/system-one-adapter-python?style=flat) - Drop-in `TypeSafeClient` backed by ordinary chat LLMs so you can A/B and offline-compare without waiting on the real model. We picked it for teams who need a fair baseline before they commit spend. Caveat: it is a stand-in, not a free Jev — keep that label loud in your eval notes.
- [skills](https://github.com/typesafe-ai/skills) ![GitHub stars](https://img.shields.io/github/stars/typesafe-ai/skills?style=flat) - Official agent skills for building against the System One API — the “start cooking with the right utensils” pack. Included because [@typesafeai](https://x.com/typesafeai/status/2100376436272173088) framed it as how serious builders should bootstrap. Aimed at agent authors who want conventions, not another blank repo.
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Hosted model listing on Cloudflare’s AI platform if your runtime already is Workers-shaped. Worth a bookmark when you care more about edge colocations than about owning the client stack. Not a tutorial; more a “yes, it is actually available here” receipt.

## Platforms

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - Call `typesafe-ai/jev` through AI SDK 7 `evaluate` without waiting on a private waitlist — the overnight on-ramp that actually changed who could experiment. We keep it high because [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175) turned access into a product story, not a footnote. Perfect for Next.js / AI SDK shops; just remember Gateway quotas are still quotas.
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - Native Choice / Score / Boolean path that looks like System One answers already live in your application code. Selected as the ergonomic twin of the Gateway entry — same mental model, fewer glue files. Experimental name is honest: APIs can still move under you.

## Browser & computer use

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) ![GitHub stars](https://img.shields.io/github/stars/browser-use/jev-ultrafast?style=flat) - Browser Use’s flagship loop and still the clearest “why Jev” demo on the internet: DOM → indexed ops/targets → one Jev round trip, with a small LLM only for typing. Zürich→London Flights (~7s, ~$0.0039) plus [@gregpr07](https://x.com/gregpr07/status/2100411066966749359) made the latency story travel farther than any star chart. Steal this architecture if you have a finite, observed action space; ignore it if your agent is still “do whatever.”
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) ![GitHub stars](https://img.shields.io/github/stars/awlevin/typesafe-computer-use?style=flat) - macOS computer-use via OCR + Jev, with a cost table that made people sit up (~$0.0002/step in the author’s numbers). Listed because [@awlevin](https://x.com/awlevin/status/2100262612428894676) turned desktop automation into a measured System One story, not a vibes reel. Best for Mac-native builders; OCR noise is the tax you pay for skipping a perfect accessibility tree.
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) ![GitHub stars](https://img.shields.io/github/stars/aidil2105/jev-browser-pilot?style=flat) - Library-shaped pilot (surface, perception, policy, verify, safety, traces) for people designing their own loop instead of forking Ultrafast. Stars are quiet; the structure is not — that is exactly why it is here. Prefer when you want seams you can swap; skip if you just need a working flights demo tonight.

**Parking lot:** thin browser wrappers of Ultrafast with no new measurement or X traction (including mobile ports — ping us when the thread heats up).

## Coding agents

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) ![GitHub stars](https://img.shields.io/github/stars/tamaratran/fast-jev-compaction?style=flat) - Claude Code plugin where Jev scores tool calls/results and kept context stays verbatim — compaction as a gate, not a summarizer that invents. High stars and strong trend even without a widely cited launch thread, which is why our Observations call it out. For Claude Code power users drowning in tool noise; watch for over-aggressive drops if your tasks need long tails of boring context.
- [foreman](https://github.com/thruwire/foreman) ![GitHub stars](https://img.shields.io/github/stars/thruwire/foreman?style=flat) - Software-factory supervision with Jev judging steps — less “write my PR,” more “did this stage actually pass?” We like the Codex-supervision angle [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717) put into the feed. Aimed at multi-agent factory builders; overkill if you only need a single review bot.
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) ![GitHub stars](https://img.shields.io/github/stars/devagrawal09/jev-review?style=flat) - Staged review plus a local dashboard — the community’s favorite “show me the gates” review shape. Cited in roundups such as [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556), which is enough heat for a review tool. Great when you want human-visible stages; heavier than a one-shot MCP call.
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) ![GitHub stars](https://img.shields.io/github/stars/NiazMorshed2007/jev-review?style=flat) - Local-first MCP `jev_review` when your stack is already MCP-shaped. Prefer this sibling if Claude/Cursor tools are your front door; less X signal than the staged-review cousin, and that is fine. Caveat: MCP-first joy, dashboard-second polish.
- [pi-jev](https://github.com/y0usaf/pi-jev) ![GitHub stars](https://img.shields.io/github/stars/y0usaf/pi-jev?style=flat) - Decision layer for Pi: tool-call gate plus `jev_ask` so the agent asks before it acts. Selected as a clean “System One as permissioning” pattern inside a specific agent runtime. For Pi users who want typed vetoes; not a general coding agent on its own.
- [pi-warden](https://github.com/DevMortimer/pi-warden) ![GitHub stars](https://img.shields.io/github/stars/DevMortimer/pi-warden?style=flat) - Pi guardrails against irreversible tools, loops, and fake “done,” steered by Jev. Pairs naturally with pi-jev when you care about safety theater becoming real checks. Best for operators who have already been burned by an agent that “finished” too early.

## Routers

- [jev-router](https://github.com/gargpratyush/jev-router) ![GitHub stars](https://img.shields.io/github/stars/gargpratyush/jev-router?style=flat) - Per-turn cheap/strong routing for Claude Code and Codex — still the most-cited router pattern in this ecosystem. X heat is quieter than the browser demos, but usefulness is why it stays. Watch cost regressions when the “cheap” model starts failing the hard turns you thought were easy.
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) ![GitHub stars](https://img.shields.io/github/stars/yusukebe/hono-jev-router?style=flat) - Semantic HTTP routing for Hono: Jev picks a route, your handlers stay boring. Small, clean proof that System One is not only a coding-agent toy. For Hono / edge API folks; overkill if a static path table already works.

## Data & libraries

- [pg-jev](https://github.com/realZachi/pg-jev) ![GitHub stars](https://img.shields.io/github/stars/realZachi/pg-jev?style=flat) - PostgreSQL extension that lets you ask tables questions in plain language via Jev — rare “decision model lives next to the data” angle. X is quiet; niche utility is loud, which is enough for us. For SQL-native teams; not a substitute for a proper analytics warehouse story.

## Demos worth studying

- [jev-trader](https://github.com/jarrodwatts/jev-trader) ![GitHub stars](https://img.shields.io/github/stars/jarrodwatts/jev-trader?style=flat) - One buy/sell decision per Monad block on Kuru MON-USDC — a hot loop with a calibrated choice, not a chatbot that “feels bullish.” [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346) made the template travel. Study the pacing; do not treat it as financial advice or a production trading desk.
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) ![GitHub stars](https://img.shields.io/github/stars/fhshaik/typesafe-mario?style=flat) - Mario driven from structured emulator state — a toy surface with a serious lesson: feed observed state, not raw pixels, when you can. We keep it for teaching action-space hygiene. Fun first; production second (or never).

## Jev-like & related models

Independent projects and **related / inspired models** that explore System One–style decisions. They may **not** call TypeSafe Jev. Inclusion is driven by **discussion heat and study value**, not affiliation.

- [SemIf](https://github.com/TheoLeeCJ/SemIf) ![GitHub stars](https://img.shields.io/github/stars/TheoLeeCJ/SemIf?style=flat) - “Semantic ifs” from open models on a home 3090 — explicitly independent, not affiliated with TypeSafe. Sparse X (e.g. [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)) but enough inspired-by signal for tinkerers who want local conditionals. For DIY GPU owners; expect research edges, not a polished SaaS twin.
- [jevlike](https://github.com/vinnylarouge/jevlike) ![GitHub stars](https://img.shields.io/github/stars/vinnylarouge/jevlike?style=flat) - Train a small model for one-pass option probabilities (Doom / chess / Wikispeedia). Independent / inspired-by study piece with sparse X plus solid HN traction (~161 pts). Great if you want to feel how System One–shaped outputs are learned; not a drop-in Jev replacement and not affiliated.
- [nimble](https://github.com/bespokelabsai/nimble) ![GitHub stars](https://img.shields.io/github/stars/bespokelabsai/nimble?style=flat) - Open “Jev recipe” (LoRA + constrained serving) — not affiliated with TypeSafe, listed because the recipe itself is the product. [@madiator](https://x.com/madiator/status/2100990591215783946) and HN both gave it heat. For teams who want to cook their own System One–ish model; bring ML ops patience.
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) ![GitHub stars](https://img.shields.io/github/stars/ekzhang/openjev-sglang?style=flat) - Prefill-only Jev-compatible API on SGLang — independent, not affiliated. HN discussion is the inclusion ticket: serving shape matters as much as model weights. For infra folks already living in SGLang; read “compatible” as “shape-alike,” not “official.”
- [open-jev](https://github.com/daseinlabs/open-jev) ![GitHub stars](https://img.shields.io/github/stars/daseinlabs/open-jev?style=flat) - Local Gemma/MLX option scoring. Not affiliated with TypeSafe; on the list for HN curiosity and laptop-friendly experiments. Ideal for Apple/local explorers; treat scores as educational, not production calibration.
- [mini-jev](https://github.com/r-ms/mini-jev) ![GitHub stars](https://img.shields.io/github/stars/r-ms/mini-jev?style=flat) - Small Qwen3 letter-logits experiment toward System One–style choices. Independent, not affiliated; HN is why it sits here. For researchers poking logits with a stick — charming, not a product.
- [jevmlx](https://github.com/bnsd55/jevmlx) ![GitHub stars](https://img.shields.io/github/stars/bnsd55/jevmlx?style=flat) - Parallel decisions on Apple Silicon via MLX. Not affiliated; heat from [@beni_il_](https://x.com/beni_il_/status/2100617387116568956) and HN. Best for Mac MLX natives chasing parallel Choice-shaped calls; bring your own eval harness.
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) ![HF likes](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fmodels%2Fharshatheg%2FQwen-2.5-1B-RLCD&query=%24.likes&label=HF%20likes&style=flat) - Parallel constrained / multi-field decisions as an HF model — independent, not TypeSafe. Strong X from [@harshagundal](https://x.com/harshagundal/status/2100044305536889015) earned the slot. For people who want a downloadable brain, not an API key; verify constraints before you trust multi-field outputs.
- [LitJev](https://github.com/zhengxuyu/LitJev) ![GitHub stars](https://img.shields.io/github/stars/zhengxuyu/LitJev?style=flat) - Wrap an arbitrary LLM into a Jev-like `/v1/systemone` surface. Not affiliated; [@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337) put the adapter pattern on the map. Handy for protocol experiments; remember a wrapper does not magically become System One quality.

More entries welcome when X (or HN) shows sustained practical interest — open a PR with the thread.

## Related lists

Use these when you want coverage over curation:

- [awesomejev.com](https://awesomejev.com/) - The big auto-refreshed directory (repos, sites, threads) when you need breadth we deliberately refuse. Use it to discover; come back here to decide. Great companion, not a substitute for taste.
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) ![GitHub stars](https://img.shields.io/github/stars/yibie/awesome-jev?style=flat) - Community awesome list for Jev projects — wider net, lighter editorial voice than ours. We like it as a peer radar. Cross-check notes before you adopt anything quiet.
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) ![GitHub stars](https://img.shields.io/github/stars/AbdelStark/awesome-typesafe?style=flat) - Broader TypeSafe + System One + Jev resources beyond “apps that call the API.” Selected for people mapping the whole landscape. Expect more links per page than spicy takes.
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - Long-form explainer covering SDK, Gateway, and `evaluate` — the essay you send a teammate who does not want fifteen tabs. Warm, practical, slightly opinionated in a good way. Best as onboarding, not as a living catalog.

## Maintained by Grok Bot

This list is tended by **[Grok Bot](https://grok.com)** (with a human in the loop for the spicy calls). We watch what the community is building and arguing about, then keep the notes honest.

If something here helped you ship — or you disagree with a call — open an issue or PR. **Hope you like it.** Pull requests with a good thread and a clear “why” make our day.

## Contributing

See [contributing.md](contributing.md). Drop a PR with the repo, why it belongs, which criterion it hits, and a public thread when you have one. Low-signal “also mentions Jev” PRs will get a friendly close.

## License

[CC0](license) — share it, fork it, remix it. Same spirit as other awesome lists.
