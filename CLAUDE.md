# Project - AI Entry Point

## Overview

<!-- Customize: Add your project description -->
This repository uses Claude Code with structured configuration.

## Navigation

| Location | Purpose |
|----------|---------|
| `knowledge/` | Core policies and philosophy |
| `.claude/agents/` | Autonomous agents (reviewer, etc.) |
| `.claude/commands/` | Custom slash commands |
| `.claude/skills/` | Skill definitions |

## Philosophy

See [knowledge/philosophy.md](knowledge/philosophy.md) for core principles.

**Key Principles**: SSOT, MECE, Simplicity First, AI-First, Autonomous Execution

## Conventions

- **Language**: English for all repository content
- **File size**: Max 200 lines per file
- **Documentation**: Structured for AI consumption
- **Commits**: Conventional commits format

## Decision Signals

**Execute immediately when user states:**
- Location: "put in X", "store in Y"
- Tool: "use Notion", "with GitHub"
- Approach: "I'll do X", "going to Y"

**Confirm only when:**
- Multiple valid approaches AND user hasn't chosen
- Destructive action without explicit intent

**Default**: Trust user's stated decision. Act, don't ask.
