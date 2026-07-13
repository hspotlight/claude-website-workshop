# Claude 101 Workshop (May 7, 2026)

A hands-on workshop for learning Claude Code fundamentals — from installation to building with AI-assisted development.

## Prerequisites

- [Node.js](https://nodejs.org/) v18+
- npm (comes with Node.js)
- An [Anthropic API key](https://console.anthropic.com/)

## Getting Started

### 1. Install Claude Code

```bash
# Install globally
npm install -g @anthropic-ai/claude-code

# Or run directly without installing
npx @anthropic-ai/claude-code
```

### 2. Clone this repo

```bash
git clone <repo-url>
cd claude-101-workshop-7-may-2026
```

### 3. Start Claude Code

```bash
# Launch interactive mode
claude

# Start with a prompt
claude "explain this project"

# Resume last conversation
claude --continue

# Non-interactive (headless) mode
claude -p "what does this project do?"
```

## Installed Skills

Skills are slash commands that extend Claude Code with specialized workflows.

| Skill | Command | Description |
|-------|---------|-------------|
| grill-me | `/grill-me` | Stress-test your plan or design through relentless interviewing |
| qa | `/qa` | Interactive QA session — report bugs conversationally, auto-files GitHub issues |
| tdd | `/tdd` | Test-driven development with red-green-refactor loop |
| to-prd | `/to-prd` | Turn current conversation into a PRD and submit as a GitHub issue |

### Installing More Skills

```bash
# Syntax
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code-skills/main/skills.sh | bash -s -- <skill-name>

# Examples
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code-skills/main/skills.sh | bash -s -- tdd
curl -fsSL https://raw.githubusercontent.com/anthropics/claude-code-skills/main/skills.sh | bash -s -- grill-me
```

Discover available skills with `/find-skills` inside Claude Code.

## Project Structure

```
.
├── CLAUDE.md          # Claude Code project context
├── README.md          # This file
├── index.html         # Main application
├── .claude/           # Claude Code settings & skills
└── .agents/           # Agent skills (grill-me, qa, tdd, to-prd)
```

## License

Workshop material for educational purposes.
