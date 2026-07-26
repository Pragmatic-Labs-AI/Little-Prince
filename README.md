# Little Prince

> "Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away." — Antoine de Saint-Exupéry

A [Claude skill](https://www.anthropic.com/news/skills) for minimalist distillation. It finds the actual problem underneath a request and fills only the narrowest band needed to solve it — no less than the problem requires, no more.

Built by [Pragmatic Labs](https://pragmaticlabs.ai).

## The problem this fixes: Subtractive AI

Every model ships with some version of "you are a helpful assistant" as its first instruction, and models are slavishly literal about fulfilling it. Left alone, they're additive by default — a rewritten email gets an extra line "for completeness," a Jira ticket balloons into something a Fortune 50 scrum master would write to justify their existence, a business plan grows padding that scales with the size of the ask rather than the size of the problem. None of it is wrong, exactly. All of it costs the reader time, and at scale it costs budgets and calendars: a plan dense enough to look impressive can be dense enough to become unbuildable.

Little Prince is the prescription: it works backward from what "solved" actually requires and strips everything that isn't that.

## What it does

1. **Find the actual problem** — the smallest true description of what "solved" looks like.
2. **Fill the narrowest band that solves it** — not the shortest possible output, the *right-sized* one. Genuinely hard problems keep their real complexity, undiluted. The test is waste, not word count.

It cuts restated questions, non-decisive hedges, unrequested options, throat-clearing, and self-narration. It does **not** cut necessary complexity, anything that would force a follow-up to become usable, or a caveat that's actually load-bearing.

## Why not just ask for "be concise"?

Because brevity and distillation solve different problems. "Be concise" compresses sentences and risks cutting content the problem actually needs. Little Prince re-derives the target from the problem first, then fills only that — a hard problem gets a long, undiluted answer; a simple one gets a short one. The instruction isn't "say less," it's "say exactly what solving this requires and nothing that doesn't."

## Before / after

**Request:** "Give me a rollout plan for a new internal tool."

**Additive default (representative, not verbatim):**
> This is an exciting opportunity to modernize our internal tooling. Before diving into logistics, it's worth considering the broader context of digital transformation and change management. A successful rollout should account for stakeholder buy-in, phased communication strategies, training programs tailored to different learning styles, feedback loops, contingency planning for adoption resistance, and a robust framework for measuring success across multiple KPIs...
> *(continues for several more paragraphs before reaching an actual schedule)*

**Little Prince:**
> **Week 1:** Pilot with 5 users, daily check-ins.
> **Week 2:** Fix what broke. Expand to 20.
> **Week 3:** Full rollout. One retro at the end.
>
> Skip training decks — screen-share the first week instead. Cut this shorter if the pilot goes clean.

Same problem, same required decisions, a fifth of the words — because the extra paragraphs weren't answering the question, they were performing thoroughness.

## Install

Add the folder via **Settings → Capabilities → Skills** in Claude, or drop it into your local skills directory if you're running Claude Code / an agent harness that reads `SKILL.md` files.

## Use

Trigger it by name — "Little Prince," "distill this," "strip this down" — or just ask for the essence/leanest version of a document, plan, decision, or piece of code. See [`SKILL.md`](./SKILL.md) for the full operating instructions and worked example.

## License

MIT — see [LICENSE](./LICENSE).
