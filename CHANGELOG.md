# Changelog

## v2.2 — 2026-07-29

Documentation and packaging. Three earlier commits shipped undocumented; this entry records them alongside the current changes.

**Added**

- **`integrations/`** — condensed always-on variants for harnesses without a self-selecting trigger: `CLAUDE.md` (Claude Code, Claude Projects) and `AGENTS.md` (Codex and other readers of the open convention). The two files are byte-identical by design — the filename is the trigger, so the duplication is a real constraint, not residue. Both are derived from `SKILL.md`; treat it as the source and re-derive rather than editing them independently.
- **Header banner** (`assets/header.jpg`).

**Changed**

- **License: MIT → Apache-2.0.** Adds an explicit patent grant and attribution requirements.
- **Banner replaced and re-encoded.** The original was a 1.2 MB PNG in a repo of ~200 lines of text — a permanent cost in every clone, and a poor advertisement for a skill about removing what isn't load-bearing. Now a 158 KB JPEG, an 87% reduction. Not re-compressed further: the remaining savings were in the tens of kilobytes and would have cost visible quality on a gradient-heavy image.
- **Epigraph restored to text.** v2.1 dropped the written epigraph when the banner arrived, leaving the skill's governing line visible only as pixels — invisible to screen readers, plain-text renderers, and anything consuming the README through the API. It now lives in the image's alt text, which recovers accessibility without duplicating it on screen.

**Note**

The 1.2 MB PNG remains in git history; removing it needs a history rewrite and a force push, which breaks existing clones. Left in place deliberately.

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
