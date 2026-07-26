---
name: little-prince
description: Reduces complexity at every altitude — concept, scope, structure, execution, and expression. Finds what is actually load-bearing, cuts the rest, and works top-down so the highest-leverage cuts happen first. Use when the user says "Little Prince," asks to distill, simplify, strip down, de-bloat, or find the essence of something; when reviewing an architecture, product spec, feature list, taxonomy, roadmap, process, or org design for unnecessary complexity; when a plan or codebase feels over-engineered; or when asked for the leanest version of a document, decision, or solution. Trigger even when the skill isn't named but the user is clearly asking whether something is more complicated than it needs to be.
---

# Little Prince

"Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away." — Antoine de Saint-Exupéry

## The test

Everything present must be load-bearing. For any element, at any scale: what is this carrying, and what breaks if it's gone? If nothing breaks, it's residue, not structure.

This is one test, not several. It reads the same on a clause, a feature, a domain in a taxonomy, a step in a process, an abstraction layer, a recurring meeting. Don't look for the version of the rule that fits the artifact type in front of you — there's one rule.

## Cut from the top down

Complexity compounds downward. A concept spawns designs, a design spawns implementation, implementation spawns process and documentation and explanation. Cutting upstream erases everything downstream; cutting downstream erases only itself.

Work in this order, and don't descend until the level above is settled:

1. **Is the problem real?** Solving an invented problem elegantly is still waste. Ask what happens if nothing is done.
2. **Is the scope right?** Half the requirements in a request are assumed, inherited, or defensive. Name the ones that would actually make it fail.
3. **Does the structure fit?** Merge things doing one job under two names. Cut what serves an imagined need. Five domains that collapse to three were always three.
4. **Is the execution direct?** Steps and tools that don't change the outcome; ceremony that survives only by habit.
5. **Is the expression clean?** Hedges, restatement, unrequested options, throat-clearing, narrating your own edits.

Most requests arrive pointed at level 5. Check the others first anyway. The highest-value move is often telling someone the document they asked you to tighten describes something they shouldn't build.

## Four diagnostics

- **What breaks without it?** Nothing → cut.
- **Are two things doing one job?** → merge.
- **Does this serve a stated need or an imagined one?** Imagined → cut.
- **Is this a fossil of a constraint that no longer holds?** → cut.

## What doesn't get cut

- Necessary complexity. The answer should be exactly as hard as the problem and no harder. Don't flatten a real multi-step process into a false one-liner.
- Anything whose absence forces a follow-up. That's truncation, not distillation.
- A load-bearing caveat — a real risk, a real unknown. This mode governs shape, not honesty.
- Slack that's doing real work: redundancy in safety-critical systems, deliberate margin, a repetition that aids retention.

## Examples

**Level 1 — is the problem real?**

*Input:* "Should we migrate our Postgres database to a NoSQL solution? There's a lot to weigh — performance, team familiarity, cost, migration risk, vendor lock-in, scalability over the next five years..."

*Distilled:* What's driving this — a concrete bottleneck, or a hunch? Without one, don't migrate. Postgres handles far more scale than most teams ever reach, and rewriting the data layer to chase hypothetical load is the standard way to lose a year. If there is a specific bottleneck, name it; that's the one factor deciding this, not the other five.

**Level 3 — does the structure fit?**

*Input:* A content taxonomy with five top-level domains: Articles, Guides, Tutorials, Case Studies, Resources.

*Distilled:* Guides and Tutorials differ in tone, not in what a reader does with them — one category. Resources is a bucket for things that didn't fit elsewhere, which means it isn't a category, it's an admission the taxonomy is incomplete; distribute its contents and delete it. Three domains: Articles, Guides, Case Studies. Every item now has one obvious home, which was the point of having a taxonomy.

## Guardrails

- Distilled ≠ vague. Cutting hedges must not cut information.
- Simplicity in the artifact, not just in the description of it. Fewer moving parts beats fewer characters; a clever one-liner that costs readability is a different kind of bloat.
- Before cutting something that looks pointless, check whether it's a fence with a forgotten reason. Ask rather than assume when the cost of being wrong is high.
- If it's already tight, say so. Don't invent things to trim.
