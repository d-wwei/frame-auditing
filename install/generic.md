# Install — Generic (Any Agent/Framework)

## Universal principle

Frame Auditing is a cognitive base — it changes how the agent perceives problem structure, not what tools it uses. Installation means injecting `cognitive-protocol.md` into the agent's always-on instructions (system prompt, rules file, or configuration).

## Platform mapping

| Platform | Where to inject | File to use |
|---|---|---|
| Claude Code | `~/.claude/frame-auditing.md` + ref in `CLAUDE.md` | `cognitive-protocol.md` |
| Codex | Prepend to `AGENTS.md` | `cognitive-protocol.md` |
| Gemini | `system_instruction` field | `cognitive-protocol.md` |
| Cursor | Prepend to `.cursorrules` | `cognitive-protocol.md` |
| ChatGPT | Custom Instructions -> system prompt | `cognitive-protocol.md` |
| LangChain | System message in chain | `cognitive-protocol.md` |
| AutoGPT / CrewAI | Agent system prompt | `cognitive-protocol.md` |
| Any other | Find the "always-on instructions" config and inject there | `cognitive-protocol.md` |

## Step by step

1. Locate your agent's system prompt or always-on rules file
2. Copy the contents of `cognitive-protocol.md` (~30 lines)
3. Paste it into the system prompt, BEFORE any domain-specific instructions
4. If using other cognitive bases, place Frame Auditing first (it operates on problem perception, which precedes reasoning and output)

## File selection guide

| Need | File | Size |
|---|---|---|
| Minimal install (core rules only) | `cognitive-protocol.md` | ~30 lines |
| Full reference framework | + `SKILL.md` | ~200 lines |
| Anti-pattern detection | + `anti-patterns.md` | ~130 lines |
| Teaching examples | + `examples.md` | ~130 lines |

For most agents, `cognitive-protocol.md` alone is sufficient. The additional files are reference material for when the agent needs deeper guidance.

## Troubleshooting

- **Agent ignores the rules**: Move `cognitive-protocol.md` content to the beginning of the system prompt, not the end. Most models weight earlier instructions more heavily.
- **Rules conflict with domain instructions**: Frame Auditing should never conflict — it changes problem perception, not output format. If conflict appears, the domain instruction likely contains an unexamined frame. That's a feature, not a bug.
- **Context window pressure**: `cognitive-protocol.md` is ~30 lines. If that's too much, something else in your prompt needs trimming first.
- **Agent over-applies frame auditing**: If every response starts with lengthy frame analysis on trivial questions, add: "Apply full frame auditing only when the frame is non-obvious or when the question contains implicit assumptions. For routine tasks, run the self-check silently."
