# Little Prince

> "Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away."
> — Antoine de Saint-Exupéry

A [Claude skill](https://www.anthropic.com/news/skills) for reducing complexity — not just in what gets written, but in what gets conceived, scoped, structured, and built.

**v2** — see [CHANGELOG](./CHANGELOG.md) for what changed and why.

## The idea

Most simplification advice operates on wording. That's the cheapest layer and the least valuable one. Tightening the prose of a spec for a feature that shouldn't exist is motion, not progress.

Little Prince applies a single test at every altitude:

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

## Design notes

A few decisions worth knowing if you fork it:

- **One test, not a taxonomy of tests.** An earlier draft listed tactics by artifact type. That version handled the cases it named and missed everything else. A single generative principle transfers; a list doesn't.
- **Leverage ordering is the core mechanic.** Without it, the skill happily optimizes the wrong layer.
- **The guardrails are load-bearing.** They cost length, and they're what keep "ruthless" from becoming "reckless."

## License

MIT — see [LICENSE](./LICENSE).
