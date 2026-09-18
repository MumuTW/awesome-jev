# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**Languages:** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md) · [日本語](readme.ja.md) · [한국어](readme.ko.md)

> Curated, high-signal projects built on [Jev](https://typesafe.ai) — TypeSafe AI's System One model for typed decisions (choice, score, boolean with confidence) — plus **Jev-like** models and replicas when public discussion shows real heat.

## What makes this list different

Mega-directories already cover **breadth** ([awesomejev.com](https://awesomejev.com/), [yibie/awesome-jev](https://github.com/yibie/awesome-jev), [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)). We cover **judgment**.

| Others often do | We do |
| --- | --- |
| Scrape / mirror hundreds of repos | Keep a short list you can finish in one sitting |
| One-line marketing blurbs | **Editorial notes** — why it matters, caveats, who it is for |
| Stars as the ranking signal | **Community research** — measured loops, launch threads (especially X), patterns people actually quote |
| Only “calls TypeSafe API” | Also **Jev-like / related models** when X (or HN) discussion shows practical interest — clearly labeled not TypeSafe |
| Treat every fork as equal | Prefer best-in-class per pattern; skip thin Ultrafast wrappers |

Borrowed from lists we admire (and adapted):

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome) / [awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — curation over collection; high bar; say *why* something is awesome.
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — sharp scope, honest “not here” buckets.
- Multilingual READMEs — English is canonical for merges; other languages are first-class mirrors.

## Contents

- [How we curate](#how-we-curate)
- [Observations](#observations)
- [Official](#official)
- [Platforms](#platforms)
- [Browser & computer use](#browser--computer-use)
- [Coding agents](#coding-agents)
- [Routers](#routers)
- [Data & libraries](#data--libraries)
- [Demos worth studying](#demos-worth-studying)
- [Jev-like & related models](#jev-like--related-models)
- [Related lists](#related-lists)
- [Contributing](#contributing)

## How we curate

### Direct Jev / TypeSafe

Keep when **at least two** are true:

1. Real TypeSafe / Jev API usage (or official docs / SDK), not a name collision.
2. You could ship or steal a pattern from it this week (cost, latency, action space, routing, review).
3. Public discussion beyond a quiet README (launch threads, cost/latency numbers, forks that cite it).

### Jev-like / related models (may not call Jev)

Keep when public discussion (especially **X**, sometimes HN) signals **practical interest or heat**, even if the project never calls TypeSafe. Label clearly as independent / inspired-by. Stars alone are not enough; a quoted thread or measured demo usually is.

Drop: dump directories, unused renames, thin Ultrafast clones, and name collisions. If similar to an existing entry, argue in the PR **how it is better**.

## Observations

- **Jev wins when the action space is finite and observed.** Projects that moved the needle on X ([Browser Use flights](https://x.com/gregpr07/status/2100411066966749359), [Mac computer-use cost](https://x.com/awlevin/status/2100262612428894676)) turn the world into an indexed table, then ask one parallel pass. Free-form “do whatever” agents are the wrong fit.
- **Small LLM only for text generation.** Ultrafast and computer-use keep a text model for typing. That split is the recurring architecture.
- **Coding-agent use is about gates, not authorship.** Compaction, review, tool allow/deny, and model routing are natural System One jobs.
- **Latency narratives travel farther than star counts.** Prefer measured loops. **Star ≠ X:** [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) stayed keep for trend/usefulness even without a found launch thread.
- **Access path matters.** [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) (`typesafe-ai/jev`) changed who could experiment overnight ([@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175)).
- **Jev-like heat is a signal, not affiliation.** SemIf / jevlike teach open alternatives; X/HN chatter is why they sit here — always label independent.

## Official

- [TypeSafe](https://typesafe.ai) - Product home and early-access console for Jev.
- [System One docs](https://docs.typesafe.ai) - What Jev is good at (atomic typed questions) and what it is not (long System-2 prose).
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) - Official TypeScript/JavaScript client (`@typesafe-ai/sdk`).
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) - Official Python client.
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) - Drop-in `TypeSafeClient` backed by chat LLMs for A/B and offline comparison.
- [skills](https://github.com/typesafe-ai/skills) - Official agent skills for building with the System One API ([@typesafeai](https://x.com/typesafeai/status/2100376436272173088)).
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Hosted model listing on Cloudflare's AI platform.

## Platforms

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - Call `typesafe-ai/jev` through AI SDK 7 `evaluate` without waiting on the TypeSafe list. Practical on-ramp; see also [@vercel_dev](https://x.com/vercel_dev/status/2100378959653507175).
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - Native Choice / Score / Boolean path that matches how System One answers look in application code.

## Browser & computer use

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) - Browser Use flagship: DOM → indexed ops/targets → one Jev round trip; small LLM only for typing. Zürich→London Flights (~7s, ~$0.0039). Reference X narrative: [@gregpr07](https://x.com/gregpr07/status/2100411066966749359).
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) - macOS via OCR + Jev (~$0.0002/step in the author's table). X: [@awlevin](https://x.com/awlevin/status/2100262612428894676).
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) - Library-shaped pilot (surface, perception, policy, verify, safety, traces). Low stars; strong structure if you design your own loop.

**Skipped for now:** thin browser wrappers of Ultrafast without a new measurement or X traction (including mobile ports until discussion shows up).

## Coding agents

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) - Claude Code plugin: Jev scores tool calls/results; kept context stays verbatim. High stars / strong trend; keep even without a found launch thread (Star ≠ X).
- [foreman](https://github.com/thruwire/foreman) - Software-factory supervision with Jev judging steps. X: [@JoshARosen](https://x.com/JoshARosen/status/2100573432089866717) (Codex supervision angle).
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) - Staged review + local dashboard. Cited in community roundups (e.g. [@0xLogicrw](https://x.com/0xLogicrw/status/2100478725393686556)).
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) - Local-first MCP `jev_review`. Prefer when your stack is MCP-first; less X signal than the staged-review sibling.
- [pi-jev](https://github.com/y0usaf/pi-jev) - Decision layer for Pi: tool-call gate + `jev_ask`.
- [pi-warden](https://github.com/DevMortimer/pi-warden) - Pi guardrails (irreversible tools, loops, fake “done”) steered by Jev.

## Routers

- [jev-router](https://github.com/gargpratyush/jev-router) - Per-turn cheap/strong routing for Claude Code and Codex. Most-cited router pattern; weaker X signal than browser demos — keep for usefulness, watch cost regressions.
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) - Semantic HTTP routing for Hono. Small, clean “Jev picks a route” outside coding agents.

## Data & libraries

- [pg-jev](https://github.com/realZachi/pg-jev) - PostgreSQL extension: ask tables questions in plain language via Jev. Kept for the rare “Jev inside the database” angle (weak X; strong niche utility).

## Demos worth studying

- [jev-trader](https://github.com/jarrodwatts/jev-trader) - One buy/sell decision per Monad block on Kuru MON-USDC. Template for hot loop + calibrated choice. X: [@jarrodwatts](https://x.com/jarrodwatts/status/2100356151468585346).
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) - Mario from structured emulator state. Toy surface; lesson: feed observed state, not pixels, when you can.

## Jev-like & related models

Independent projects and **related / inspired models** that explore System One–style decisions. They may **not** call TypeSafe Jev. Inclusion is driven by **discussion heat and study value**, not affiliation.

- [SemIf](https://github.com/TheoLeeCJ/SemIf) - “Semantic ifs” from open models on a home 3090. Explicitly independent. Sparse X (e.g. [@hhkkmon](https://x.com/hhkkmon/status/2100443314957038010)); keep as inspired-by reference.
- [jevlike](https://github.com/vinnylarouge/jevlike) - Train a small model for one-pass option probabilities (Doom / chess / Wikispeedia). Sparse X + HN traction (~161 pts); keep as inspired-by / open-replica study.
- [nimble](https://github.com/bespokelabsai/nimble) - Open “Jev recipe” (LoRA + constrained serving). Not affiliated. X: [@madiator](https://x.com/madiator/status/2100990591215783946); also on HN.
- [openjev-sglang](https://github.com/ekzhang/openjev-sglang) - Prefill-only Jev-compatible API on SGLang. Not affiliated. Discussed on HN.
- [open-jev](https://github.com/daseinlabs/open-jev) - Local Gemma/MLX option scoring. Not affiliated. HN discussion.
- [mini-jev](https://github.com/r-ms/mini-jev) - Small Qwen3 letter-logits experiment toward System One–style choices. Not affiliated. HN.
- [jevmlx](https://github.com/bnsd55/jevmlx) - Parallel decisions on Apple Silicon via MLX. Not affiliated. X: [@beni_il_](https://x.com/beni_il_/status/2100617387116568956); HN.
- [Qwen-2.5-1B-RLCD](https://huggingface.co/harshatheg/Qwen-2.5-1B-RLCD) - Parallel constrained / multi-field decisions (HF model). Not affiliated. Strong X: [@harshagundal](https://x.com/harshagundal/status/2100044305536889015).
- [LitJev](https://github.com/zhengxuyu/LitJev) - Wrap an arbitrary LLM into a Jev-like `/v1/systemone` surface. Not affiliated. X: [@yuzxfred](https://x.com/yuzxfred/status/2100652136878981337).

More entries welcome when X (or HN) shows sustained practical interest — open a PR with the thread.

## Related lists

Use these when you want coverage over curation:

- [awesomejev.com](https://awesomejev.com/) - Large auto-refreshed directory (repos, sites, threads).
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) - Community awesome list for Jev projects.
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) - Broader TypeSafe + System One + Jev resources.
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - Long-form explainer (SDK, Gateway, evaluate).

## Contributing

See [contributing.md](contributing.md). PR: repo URL, why it is useful, which criterion it hits, and a public thread when possible.

Translations: English `readme.md` is the merge source of truth; keep locale files in sync (or flag follow-up).

## License

[CC0](license) — same spirit as other awesome lists.
