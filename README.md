# Little Prince

> "Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away."
> — Antoine de Saint-Exupéry

A [Claude skill](https://www.anthropic.com/news/skills) for reducing complexity — not just in what gets written, but in what gets conceived, scoped, structured, and built.

Built by [Pragmatic Labs](https://pragmaticlabs.ai).

**v2** — see [CHANGELOG](./CHANGELOG.md) for what changed and why.

## The problem this fixes: Subtractive AI

Every model ships with some version of "you are a helpful assistant" as its first instruction, and models are slavishly literal about fulfilling it. Left alone, they're additive by default — a rewritten email gets an extra line "for completeness," a Jira ticket balloons into something a Fortune 50 scrum master would write to justify their existence, a business plan grows padding that scales with the size of the ask rather than the size of the problem. None of it is wrong, exactly. All of it costs the reader time, and at scale it costs budgets and calendars: a plan dense enough to look impressive can be dense enough to become unbuildable.

The same reflex operates above the prose layer, where it's more expensive. Additive design invents a fifth service domain because four looked thin, keeps a feature nobody asked for because removing it feels like a loss, and preserves a process step whose original constraint disappeared two years ago.

Little Prince is the prescription, applied at every altitude.

## The idea

Most simplification advice operates on wording. That's the cheapest layer and the least valuable one. Tightening the prose of a spec for a feature that shouldn't exist is motion, not progress.

Little Prince applies a single test at every scale:

> **What is this carrying, and what breaks if it's gone?**

If nothing breaks, it's residue. The test reads identically on a clause, a feature, a domain in a taxonomy, a step in a process, an abstraction layer, or a standing meeting — which is what makes it a principle rather than a checklist.

## Cut from the top down

Complexity compounds downward. A concept spawns designs; a design spawns implementation; implementation spawns process, documentation, and explanation. Cutting upstream erases everything downstream. Cutting downstream erases only itself.

So the skill works in descending order of leverage:

| # | Level | Question |
|---|-------|----------|
| 1 | Concept | Is the problem real? |
| 2 | Scope | Are these requirements load-bearing, or assumed and defensive? |
| 3 | Structure | Are two things doing one job? Does this serve a stated need or an imagined one? |
| 4 | Execution | Do these steps change the outcome, or survive by habit? |
| 5 | Expression | Hedges, restatement, unrequested options, throat-clearing |

Most requests arrive pointed at level 5. The skill checks the others first anyway. The highest-value response is often *"the document you asked me to tighten describes something you shouldn't build."*

## Why not just ask for "be concise"?

Because brevity and distillation solve different problems. "Be concise" compresses sentences and risks cutting content the problem actually needs — and it only ever operates on level 5. Little Prince re-derives the target from the problem first, then fills only that: a hard problem gets a long, undiluted answer; a simple one gets a short one. The instruction isn't "say less," it's "carry only what's load-bearing, starting with the most expensive thing you could remove."

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

**And one level up.** Given a content taxonomy with five domains — Articles, Guides, Tutorials, Case Studies, Resources — it doesn't tighten the category descriptions:

> Guides and Tutorials differ in tone, not in what a reader does with them — one category. Resources is a bucket for things that didn't fit elsewhere, which means it isn't a category, it's an admission the taxonomy is incomplete; distribute its contents and delete it. Three domains. Every item now has one obvious home, which was the point of having a taxonomy.

## What it protects

Aggressive simplification has a real failure mode: cutting margin that existed for a reason nobody wrote down. The skill explicitly preserves —

- **Necessary complexity.** The answer should be exactly as hard as the problem and no harder.
- **Anything whose absence forces a follow-up.** That's truncation, not distillation.
- **Load-bearing caveats.** Real risks and real unknowns. This mode governs shape, not honesty.
- **Slack doing real work.** Redundancy in safety-critical systems, deliberate margin, repetition that aids retention.

And before cutting something that looks pointless, it checks whether it's a fence with a forgotten reason — Chesterton's rule, applied to features and process as much as to prose.

## Install

**Claude apps** — Settings → Capabilities → Skills → upload this folder.

**Claude Code / agent harnesses** — clone into your skills directory:

```bash
git clone https://github.com/Pragmatic-Labs-AI/Little-Prince.git ~/.claude/skills/little-prince
```

Any harness that reads `SKILL.md` frontmatter will pick it up.

## Use

Trigger by name — *"Little Prince,"* *"distill this,"* *"strip this down"* — or just hand it something and ask whether it's more complicated than it needs to be. It's designed to fire on architecture reviews, product specs, feature lists, taxonomies, roadmaps, and process design, not only on prose.

Good prompts:

- *"Little Prince this spec."*
- *"We have five service domains. Should we?"*
- *"Review this architecture — what's not earning its place?"*
- *"Give me the leanest version of this plan that still works."*

See [`SKILL.md`](./SKILL.md) for the full operating instructions and worked examples.

## Design notes

A few decisions worth knowing if you fork it:

- **One test, not a taxonomy of tests.** v1 listed tactics by artifact type. That version handled the cases it named and missed everything else. A single generative principle transfers; a list doesn't.
- **Leverage ordering is the core mechanic.** Without it, the skill happily optimizes the wrong layer.
- **The guardrails are load-bearing.** They cost length, and they're what keep "ruthless" from becoming "reckless."

## License

MIT — see [LICENSE](./LICENSE).
