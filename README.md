# Claude Code Configuration Template

> Ready-to-use template for AI-powered development with Claude Code

## Quick Start

```bash
# 1. Use this template (click "Use this template" on GitHub)
# 2. Clone your new repo
git clone git@github.com:YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO

# 3. Start using with Claude Code
claude .
```

## What's Included

```
.claude/
├── agents/          # Autonomous review & improvement agents
│   └── reviewer.md  # Code review with philosophy compliance
├── commands/        # Slash commands (/pr, /release, etc.)
└── skills/          # Complex workflow skills

knowledge/
├── philosophy.md           # 15 core principles for AI collaboration
└── extension-mechanisms.md # When to use skills vs MCP vs subagent

CLAUDE.md            # AI entry point (customize this!)
```

## Core Features

### 1. Philosophy-Driven Development
15 principles including SSOT, MECE, Simplicity First, AI-First, and more.
See [knowledge/philosophy.md](knowledge/philosophy.md).

### 2. Extension Mechanism Guide
Clear decision tree for choosing between:
- **Skills**: Code execution workflows
- **MCP**: External service integration
- **Subagent**: Autonomous judgment tasks
- **Commands**: Simple slash commands
- **Hooks**: Fully automated scripts

### 3. Reviewer Agent
Automated code review that checks:
- Philosophy compliance
- Code quality & security
- Test coverage
- Release notes updates

## Customization

1. Edit `CLAUDE.md` with your project-specific context
2. Add your own agents in `.claude/agents/`
3. Create slash commands in `.claude/commands/`
4. Add MCP integrations in `.mcp.json`

## Example MCP Configuration

```json
{
  "mcpServers": {
    "notion": {
      "type": "stdio",
      "command": "npx",
      "args": ["-y", "@notionhq/notion-mcp-server"],
      "env": {
        "NOTION_API_KEY": "${NOTION_API_KEY}"
      }
    }
  }
}
```

## Philosophy Highlights

| Principle | Description |
|-----------|-------------|
| SSOT | One source of truth, no duplication |
| AI-First | Structure docs for AI consumption |
| Autonomous Execution | Act first, ask only when blocked |
| Trust-based Delegation | AI owns execution, human sets direction |

See all 15 principles in [knowledge/philosophy.md](knowledge/philosophy.md).

## License

MIT
