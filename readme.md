# Awesome Jev [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

**Languages:** [English](readme.md) · [正體中文](readme.zh-TW.md) · [简体中文](readme.zh-CN.md)

> Curated, high-signal projects built on [Jev](https://typesafe.ai) — TypeSafe AI's System One model for typed decisions (choice, score, boolean with confidence).

## What makes this list different

Mega-directories already cover **breadth** ([awesomejev.com](https://awesomejev.com/), [yibie/awesome-jev](https://github.com/yibie/awesome-jev), [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe)). We cover **judgment**.

| Others often do | We do |
| --- | --- |
| Scrape / mirror hundreds of repos | Keep a short list you can finish in one sitting |
| One-line marketing blurbs | **Editorial notes** — why it matters, caveats, who it is for |
| Stars as the ranking signal | **Community research** — measured loops, launch threads (especially X), patterns people actually quote |
| Treat every fork as equal | Prefer best-in-class per pattern; skip thin Ultrafast wrappers |

Borrowed from lists we admire (and adapted):

- [sindresorhus/awesome](https://github.com/sindresorhus/awesome) / [awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs) — curation over collection; high bar; say *why* something is awesome.
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) — sharp scope, honest “not here” buckets (our [Open replicas](#open-replicas-not-jev) / “Skipped for now”).
- Multilingual READMEs ([standard-readme](https://github.com/RichardLitt/standard-readme), cheat-sheet style) — English is canonical for OSS discovery; 正體／简体 are first-class mirrors.

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
- [Open replicas (not Jev)](#open-replicas-not-jev)
- [Related lists](#related-lists)
- [Contributing](#contributing)

## How we curate

Keep an entry when **at least two** of these are true:

1. Real TypeSafe / Jev API usage (or official docs / SDK), not a name collision.
2. You could ship or steal a pattern from it this week (cost, latency, action space, routing, review).
3. Public discussion beyond a quiet README (launch threads, cost/latency numbers, forks that cite it).

Drop: dump directories, unused renames, clones without a decision-loop idea, and “inspired by” projects that never call Jev (those go under [Open replicas](#open-replicas-not-jev) only if they teach something).

If your project is similar to one already listed, argue in the PR **how it is better** — same rule as mature awesome lists.

## Observations

- **Jev wins when the action space is finite and observed.** The projects that moved the needle on X (Browser Use's flight demo, Mac computer-use cost tables) all turn the world into an indexed table, then ask Jev one parallel pass. Free-form “do whatever” agents are the wrong fit.
- **Small LLM only for text generation.** Ultrafast and computer-use both keep a text model for `TYPE_TEXT` / typing. That split is the recurring architecture, not “replace the whole agent with Jev.”
- **Coding-agent use is about gates, not authorship.** Compaction, review, tool allow/deny, and model routing are natural System One jobs. Expect more MCP/skill wrappers than full coding agents rewritten around Jev.
- **Latency narratives travel farther than star counts.** ~7s / ~$0.004 flights and ~$0.0002/step desktop posts are what people quote. Prefer repos that publish a measured loop.
- **Access path matters.** TypeSafe waitlist vs [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) (`typesafe-ai/jev`) changed who could experiment overnight — list Gateway next to official SDKs.
- **Replicas are useful, affiliation is not optional.** SemIf / jevlike teach open alternatives; label them clearly so nobody mistakes them for TypeSafe.

## Official

- [TypeSafe](https://typesafe.ai) - Product home and early-access console for Jev.
- [System One docs](https://docs.typesafe.ai) - What Jev is good at (atomic typed questions) and what it is not (long System-2 prose).
- [typesafe-sdk-js](https://github.com/typesafe-ai/typesafe-sdk-js) - Official TypeScript/JavaScript client (`@typesafe-ai/sdk`).
- [typesafe-sdk-python](https://github.com/typesafe-ai/typesafe-sdk-python) - Official Python client.
- [system-one-adapter-python](https://github.com/typesafe-ai/system-one-adapter-python) - Drop-in `TypeSafeClient` backed by chat LLMs for A/B and offline comparison.
- [skills](https://github.com/typesafe-ai/skills) - Official agent skills for building with the System One API (Claude Code / Codex oriented).
- [Cloudflare Workers AI — typesafe/jev](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Hosted model listing on Cloudflare's AI platform.

## Platforms

- [Jev on Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - Call `typesafe-ai/jev` through AI SDK 7 `evaluate` without waiting on the TypeSafe list. This is the practical on-ramp for many builders.
- [AI SDK `experimental_evaluate`](https://sdk.vercel.ai) - Native Choice / Score / Boolean path that matches how System One answers look in application code.

## Browser & computer use

- [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) - Browser Use's flagship loop: DOM → indexed ops/targets → one Jev round trip; small LLM only for typing. The Zürich→London Flights demo (~7s, ~$0.0039) and [@gregpr07](https://x.com/gregpr07) launch thread are the reference narrative most people share.
- [typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use) - macOS computer use via OCR + Jev action pick (~$0.0002/step in the author's table). Same “decision model + tiny text helper” pattern off the browser.
- [mobile-jev](https://github.com/droidrun/mobile-jev) - Mobile automation with Jev in the decision seat; useful if you care about phone surfaces instead of Chrome.
- [jev-browser-pilot](https://github.com/aidil2105/jev-browser-pilot) - Library-shaped pilot (surface, perception, policy, verify, safety, traces). Low stars today; strong structure if you are designing your own loop rather than cloning a demo.

**Skipped for now:** extra browser wrappers that mostly restate Ultrafast without a new measurement or surface. Revisit when they publish a distinct benchmark or voice/UX angle with traction.

## Coding agents

- [fast-jev-compaction](https://github.com/tamaratran/fast-jev-compaction) - Claude Code plugin that scores tool calls/results with Jev and keeps verbatim only what stays. Highest-signal “put System One inside the coding loop” example so far; large public attention.
- [foreman](https://github.com/thruwire/foreman) - “Software factory” supervision with Jev judging factory steps — closer to orchestration than chat.
- [jev-review (devagrawal09)](https://github.com/devagrawal09/jev-review) - Staged review workflow + local dashboard on Jev. Prefer this over sibling review repos unless you specifically need MCP packaging.
- [jev-review (NiazMorshed2007)](https://github.com/NiazMorshed2007/jev-review) - Local-first MCP `jev_review` for continuous quality feedback while the coding agent still owns edits. Keep if your stack is MCP-first.
- [pi-jev](https://github.com/y0usaf/pi-jev) - Decision layer for the Pi agent: tool-call gate + `jev_ask` for typed answers.
- [pi-warden](https://github.com/DevMortimer/pi-warden) - Guardrails on Pi (irreversible tools, loops, fake “done”) steered by Jev instead of hard interrupts.
- [building-with-jev-skill](https://github.com/dbreunig/building-with-jev-skill) - Community skill for writing better Jev-calling programs; pairs well with official `skills`.

## Routers

- [jev-router](https://github.com/gargpratyush/jev-router) - Per-turn cheap/strong routing for Claude Code and Codex while keeping each CLI's native UX. Most-cited router pattern; watch for cost regressions in the wild.
- [jev-codex-router](https://github.com/0xNatoshi/jev-codex-router) - Codex-focused routing of model + thinking depth + speed mode each turn. Narrower than jev-router; useful Codex-only comparison.
- [hono-jev-router](https://github.com/yusukebe/hono-jev-router) - Semantic HTTP routing for Hono. Small but clean “Jev picks a route” example outside coding agents.

## Data & libraries

- [pg-jev](https://github.com/realZachi/pg-jev) - PostgreSQL extension: ask tables questions in plain language with Jev behind the scenes. Rare “Jev inside the database” angle.
- [advocaat](https://github.com/pithings/advocaat) - Small typed client for asking questions about your data via Jev. Lightweight alternative when you do not want a full agent stack.

## Demos worth studying

- [jev-trader](https://github.com/jarrodwatts/jev-trader) - One buy/sell decision per Monad block on Kuru MON-USDC with a tight RPC budget. Good template for “hot loop + calibrated choice,” even if you never trade.
- [typesafe-mario](https://github.com/fhshaik/typesafe-mario) - Mario from structured emulator state. Toy surface, serious lesson: feed observed state, not pixels, when you can.
- [jev-search](https://github.com/superagents-lab/jev-search) - Source selection / query understanding / ranking with Jev + Search1API. Early; listed for the retrieval-shaped decision set.

## Open replicas (not Jev)

Independent projects that explore System One–style decisions **without** claiming TypeSafe affiliation. Study the idea; do not treat as drop-in Jev.

- [SemIf](https://github.com/TheoLeeCJ/SemIf) - “Semantic ifs” from open models on a home 3090. Explicitly independent.
- [jevlike](https://github.com/vinnylarouge/jevlike) - Train a small model for one-pass option probabilities (Doom / chess / Wikispeedia demos).

## Related lists

Use these when you want coverage over curation:

- [awesomejev.com](https://awesomejev.com/) - Large auto-refreshed directory (repos, sites, threads).
- [yibie/awesome-jev](https://github.com/yibie/awesome-jev) - Community awesome list for Jev projects.
- [AbdelStark/awesome-typesafe](https://github.com/AbdelStark/awesome-typesafe) - Broader TypeSafe + System One + Jev resources.
- [Flavio Copes — deep dive](https://flaviocopes.com/jev/) - Long-form explainer (SDK, Gateway, evaluate).

## Contributing

See [contributing.md](contributing.md). Open a PR with: repo URL, one-sentence why it is useful, which criterion it hits, and (if any) a public thread with discussion. Low-signal “also mentions Jev” PRs will be closed.

Translations: keep [readme.zh-TW.md](readme.zh-TW.md) / [readme.zh-CN.md](readme.zh-CN.md) in sync when you change structure or entries; English `readme.md` is the source of truth for merges.

## License

[CC0](license) — same spirit as other awesome lists.
