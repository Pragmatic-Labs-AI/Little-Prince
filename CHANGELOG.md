# Changelog

## v2.1 — 2026-07-26

Self-audit pass. v2 didn't pass its own test in three places.

**Changed**

- **"Four diagnostics" merged into The test.** Three of the four restated things already stated — the first was the load-bearing test verbatim, the others were level 3 and the fence guardrail inverted. Two sections doing one job under two names, which is the exact thing the skill tells you to merge.
- **Frontmatter gains a negative trigger.** v2 widened the trigger surface to architecture, specs, roadmaps, and org design, with no case for *not* firing — so it would engage on requests where exhaustive coverage was the actual point. Wanting all of something is not the same as being bloated.

**Added**

- **Deliver the artifact, not just the finding.** v2 correctly said the highest-value move is often telling someone the thing they asked you to tighten shouldn't exist — and then stopped, leaving a model free to hand over critique and no work. Observed in practice: repeated rounds of upstream analysis where the requested deliverable was never produced until asked for again. The finding comes first and the requested work still ships.

## v2 — 2026-07-26

Restructured around a single generative principle instead of a list of tactics.

**Added**

- **The load-bearing test** as the one governing rule, explicitly scale-agnostic: it reads the same on a clause, a feature, a domain, a process step, or an abstraction layer.
- **Leverage ordering** (concept → scope → structure → execution → expression). Cuts happen top-down, because upstream cuts erase everything downstream. This was the largest gap in v1: nothing stopped the skill from tightening the prose of a spec for a feature that shouldn't exist.
- **Four diagnostics** — what breaks without it; are two things doing one job; stated need or imagined need; fossil of a dead constraint.
- **A structural example** (five-domain taxonomy collapsed to three) alongside the existing decision example, so both conceptual and textual reduction are demonstrated rather than described.
- **Chesterton's-fence guardrail** — check whether something pointless-looking is a fence with a forgotten reason before removing it.
- **Protection for working slack** — redundancy in safety-critical systems, deliberate margin, repetition that aids retention.

**Changed**

- **Frontmatter description rewritten.** v1's triggers were text-editing verbs (distill, de-bloat, "no fluff"), so it wouldn't fire on "review this architecture" or "here's our product spec" — exactly the requests where the leverage is. Now names architecture, specs, feature lists, taxonomies, roadmaps, and process design.
- "What gets cut" merged into the leverage ladder; it was a flat list of expression-level tactics presented as if it covered the whole method.

**Rationale**

v1 was effective at reducing textual complexity and weak at conceptual complexity. The fix wasn't to add a "conceptual" section — that reproduces the same failure one level up, handling the domains named and missing the rest. It was to replace the tactic list with one test that transfers across altitudes, plus an order of operations that puts the expensive cuts first.

## v1 — 2026-07-26

Initial release. Two moves: find the actual problem, fill the narrowest band that solves it.
