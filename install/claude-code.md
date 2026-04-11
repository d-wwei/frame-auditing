# Install — Claude Code

> **Recommended**: Run `./install.sh` from the repo root for automated installation with dual-mode support (@ reference + inline fallback).
> The manual steps below are for reference or troubleshooting.

## Quick install

```bash
# 1. Inject core rules into CLAUDE.md (direct content injection — works on all versions)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/CLAUDE.md` (appended) | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/frame-auditing/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/frame-auditing/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/frame-auditing/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules (inject directly into CLAUDE.md)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md

# 2. Skill files
mkdir -p ~/.claude/skills/frame-auditing
cp SKILL.md ~/.claude/skills/frame-auditing/
cp anti-patterns.md ~/.claude/skills/frame-auditing/
cp examples.md ~/.claude/skills/frame-auditing/

# 3. (Core rules already injected in step 1)
```

## Verify

Ask Claude Code: "What are the frame-auditing cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: detect the frame before analyzing, audit your encoding, check attribution direction, calibrate to actual stage, separate form from content.

## Stacking with other cognitive bases

If First Principles or Tacit Knowledge is already injected into `CLAUDE.md`, no changes needed. All protocols load independently.

- Frame Auditing governs problem perception (which frame are we in?)
- First Principles governs input quality (are the foundations solid?)
- Tacit Knowledge governs output quality (how are conclusions presented?)

No conflicts. They operate at different stages of reasoning.

## Uninstall

```bash
# Remove the Frame Auditing section from ~/.claude/CLAUDE.md (search for "# Frame Auditing — Cognitive Protocol" header)
rm -rf ~/.claude/skills/frame-auditing
```
