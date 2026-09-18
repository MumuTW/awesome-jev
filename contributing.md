# Contribution Guidelines

Thanks for helping keep this list small and useful. Our differentiator is **editorial notes + community research**, not coverage.

## What belongs here

Your entry should meet **at least two** of:

1. Verified TypeSafe / Jev (System One) usage, or official TypeSafe / platform docs.
2. A pattern someone can reuse (action space, cost/latency, routing, review, data Q&A).
3. Real public discussion (X thread, launch post, measured benchmark others cite).

## What does not

- Name collisions unrelated to TypeSafe Jev.
- Another thin wrapper of [jev-ultrafast](https://github.com/browser-use/jev-ultrafast) with no new surface or numbers.
- Mega-list dumps or “add my 40 repos.”
- Open replicas that call themselves Jev — put them under **Open replicas** and say they are independent.

## PR format

1. One suggestion per pull request.
2. Add the entry in the right section (bottom of the section is fine).
3. Format: `- [name](url) - Description ends with a period.`
4. In the PR body, answer:
   - Why is this useful or high-potential?
   - Which curation criteria does it hit?
   - Link to discussion or measurements (strongly preferred).
   - If similar to an existing entry: how is it better?
5. Update **English** [readme.md](readme.md) first, then mirror structure/entries in [readme.zh-TW.md](readme.zh-TW.md) and [readme.zh-CN.md](readme.zh-CN.md) (or note that translation follow-up is needed).
6. Keep grammar clean; no trailing spaces; English descriptions in `readme.md` (translations carry the same facts, not marketing fluff).

## Editorial notes

Maintainers may rewrite descriptions into short **observations** (why it matters, caveats). Stars alone are not enough. We may also add a “Skipped for now” note instead of merging a weak entry — that is intentional.

## Lessons we steal from other lists

- High bar, not “niche by default” ([awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs)).
- Clear scope and honest out-of-scope buckets ([awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted)).
- Language switcher + English as merge source of truth ([standard-readme](https://github.com/RichardLitt/standard-readme) i18n practice).

## Creating an entry for sindresorhus/awesome

Do not submit this list upstream until it has matured at least 30 days and still follows the [Awesome guidelines](https://github.com/sindresorhus/awesome/blob/main/pull_request_template.md).
