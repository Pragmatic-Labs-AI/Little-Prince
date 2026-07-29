# Always-on integrations

`SKILL.md` in the repo root is for Claude, invoked by name or by matching its
frontmatter `description` — including the negative trigger case, so it stays out
of the way when thoroughness is actually the request.

The files here are for always-on harnesses that don't support that kind of
self-selecting trigger. Same content, condensed, dropped straight into context on
every turn — so the trigger logic (when to fire, when to suspend) had to move
from frontmatter into an inline conditional inside the text itself.

- **`CLAUDE.md`** — Claude Code / Claude Projects. Drop into `~/.claude/CLAUDE.md`
  for a global default, or commit `./CLAUDE.md` at a repo root for team-wide use.
- **`AGENTS.md`** — Codex and anything else that reads the open `AGENTS.md`
  convention. Global: `~/.codex/AGENTS.md`. Project-level and nested files are
  also supported; check your tool's docs for its combined-size cap.

Both files are intentionally short — an always-on file sits in context on every
turn, so length here is a permanent tax, not a one-time read.

**One thing this condensed form can't do as safely as the full skill:** in a
coding context, "never cut necessary complexity" is abstract enough that an
always-on version may still strip error handling or tests unless told to keep
them explicitly — which is why that line is concrete here rather than principled.
For an explicit, more aggressive multi-altitude audit, invoke the full
`SKILL.md` instead of relying on the always-on snippet.
