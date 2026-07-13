# Claude 101 Workshop (May 7, 2026)

## Project

Workshop project for learning Claude Code fundamentals.

## Requirements

- [Node.js](https://nodejs.org/) (v18+)
- npm (comes with Node.js)
- Claude Code CLI: `npm install -g @anthropic-ai/claude-code`

## Commands

```bash
# Install Claude Code globally
npm install -g @anthropic-ai/claude-code

# Or run without installing
npx @anthropic-ai/claude-code

# Start Claude Code in current directory
claude

# Start with a specific prompt
claude "explain this project"

# Resume last conversation
claude --continue

# Run in non-interactive (headless) mode
claude -p "what does this project do?"
```

## Conventions

- This is a greenfield project — no existing conventions yet.

## Skills

### Installed Skills

| Skill | Command | Description |
|-------|---------|-------------|
| grill-me | `/grill-me` | Stress-test your plan or design through relentless interviewing |
| qa | `/qa` | Interactive QA session — report bugs conversationally, auto-files GitHub issues |
| tdd | `/tdd` | Test-driven development with red-green-refactor loop |
| to-prd | `/to-prd` | Turn current conversation into a PRD and submit as a GitHub issue |

### How to Use

Invoke any skill by typing its slash command (e.g. `/tdd`, `/grill-me`). Some skills also trigger automatically based on conversation context.

### Installing New Skills

Use the installer from [anthropics/claude-code-skills](https://github.com/anthropics/claude-code-skills):

```bash
# Syntax
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code-skills/main/skills.sh | bash -s -- <skill-name>

# Examples
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code-skills/main/skills.sh | bash -s -- tdd
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code-skills/main/skills.sh | bash -s -- grill-me
```

You can also discover available skills by asking `/find-skills`.
