# Install — Claude Code

## Quick install

```bash
# 1. Copy cognitive protocol to Claude's config
cp cognitive-protocol.md ~/.claude/frame-auditing.md

# 2. Add reference in CLAUDE.md
echo '@~/.claude/frame-auditing.md' >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/frame-auditing.md` | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/frame-auditing/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/frame-auditing/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/frame-auditing/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules
cp cognitive-protocol.md ~/.claude/frame-auditing.md

# 2. Skill files
mkdir -p ~/.claude/skills/frame-auditing
cp SKILL.md ~/.claude/skills/frame-auditing/
cp anti-patterns.md ~/.claude/skills/frame-auditing/
cp examples.md ~/.claude/skills/frame-auditing/

# 3. Register in CLAUDE.md
echo '@~/.claude/frame-auditing.md' >> ~/.claude/CLAUDE.md
```

## Verify

Ask Claude Code: "What are the frame-auditing cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: detect the frame before analyzing, audit your encoding, check attribution direction, calibrate to actual stage, separate form from content.

## Stacking with other cognitive bases

If `~/.claude/first-principles.md` or `~/.claude/tacit-knowledge.md` are already referenced in `CLAUDE.md`, no changes needed. All protocols load independently.

- Frame Auditing governs problem perception (which frame are we in?)
- First Principles governs input quality (are the foundations solid?)
- Tacit Knowledge governs output quality (how are conclusions presented?)

No conflicts. They operate at different stages of reasoning.

## Uninstall

```bash
rm ~/.claude/frame-auditing.md
rm -rf ~/.claude/skills/frame-auditing
# Remove the @~/.claude/frame-auditing.md line from ~/.claude/CLAUDE.md
```
