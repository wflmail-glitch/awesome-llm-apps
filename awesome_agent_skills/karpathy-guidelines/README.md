# 🧠 Karpathy Guidelines

Four behavioral principles that curb the most common LLM coding failure modes, derived from [Andrej Karpathy's observations](https://x.com/karpathy/status/2015883857489522876) on LLM coding pitfalls.

> Source: [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) by [@forrestchang](https://github.com/forrestchang), MIT License. Mirrored here unmodified apart from the SKILL.md frontmatter.

| Principle | Addresses |
|-----------|-----------|
| **Think Before Coding** | Wrong assumptions, hidden confusion, missing tradeoffs |
| **Simplicity First** | Overcomplication, bloated abstractions |
| **Surgical Changes** | Orthogonal edits, touching code you shouldn't |
| **Goal-Driven Execution** | Verifiable success criteria, tests-first loops |

## Files

| File | Use |
|------|-----|
| [SKILL.md](SKILL.md) | Agent Skill — loaded on demand when writing, reviewing, or refactoring code |
| [CLAUDE.md](CLAUDE.md) | Drop-in always-on project instructions for Claude Code |
| [references/EXAMPLES.md](references/EXAMPLES.md) | Before/after examples for each principle |

## Install

**As a skill** — copy this directory into `~/.claude/skills/` (or your agent's skills directory).

**As a Claude Code plugin** (upstream):
```
/plugin marketplace add forrestchang/andrej-karpathy-skills
/plugin install andrej-karpathy-skills@karpathy-skills
```

**As project instructions** — copy [CLAUDE.md](CLAUDE.md) to your repo root, or append it to an existing one.

## Tradeoff

These guidelines bias toward caution over speed. For trivial tasks (typo fixes, obvious one-liners), use judgment.
