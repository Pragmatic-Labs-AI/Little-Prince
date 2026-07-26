# Changelog

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
