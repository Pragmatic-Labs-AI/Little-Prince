# Little Prince

> "Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away." — Antoine de Saint-Exupéry

A [Claude skill](https://www.anthropic.com/news/skills) for minimalist distillation. It finds the actual problem underneath a request and fills only the narrowest band needed to solve it — no less than the problem requires, no more.

## What it does

Most requests arrive wrapped in hedges, assumed requirements, and padding that aren't part of the actual target. Little Prince operates in two moves:

1. **Find the actual problem** — the smallest true description of what "solved" looks like.
2. **Fill the narrowest band that solves it** — not the shortest possible output, the *right-sized* one. Genuinely hard problems keep their real complexity, undiluted. The test is waste, not word count.

It cuts restated questions, non-decisive hedges, unrequested options, throat-clearing, and self-narration. It does **not** cut necessary complexity, anything that would force a follow-up to become usable, or a caveat that's actually load-bearing.

## Install

Add the folder via **Settings → Capabilities → Skills** in Claude, or drop it into your local skills directory if you're running Claude Code / an agent harness that reads `SKILL.md` files.

## Use

Trigger it by name — "Little Prince," "distill this," "strip this down" — or just ask for the essence/leanest version of a document, plan, decision, or piece of code. See [`SKILL.md`](./SKILL.md) for the full operating instructions and worked example.

## License

MIT — see [LICENSE](./LICENSE).
