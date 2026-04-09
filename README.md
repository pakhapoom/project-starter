# Project Starter Kit

A Python project starter template with [Claude Code](https://claude.ai/code) integration pre-configured.

## What's included

| Path | Purpose |
|---|---|
| `.gitignore` | Ignores `.venv`, `__pycache__`, build artifacts |
| `CLAUDE.md` | Claude Code instructions — enforces `uv`, code style, and response preferences |
| `.claude/settings.local.json` | Pre-approved Claude Code tool permissions |
| `.claude/commands/commit.md` | `/commit` slash command — stages and commits using Conventional Commits |
| `.claude/commands/pr.md` | `/pr` slash command — generates a PR description markdown file |

## Getting started

```bash
# 1. Clone
# HTTPS
git clone https://github.com/pakhapoom/project-starter.git my-project

# SSH
git clone git@github.com:pakhapoom/project-starter.git my-project

# Strip the remote
cd my-project
git remote remove origin

# 2. Initialize project
uv init

# 3. Install dependencies
uv sync

# 4. Add packages as needed
uv add <package>
```

## Requirements

- Python 3.12+
- [`uv`](https://docs.astral.sh/uv/) — used for all dependency and execution tasks

## Claude Code slash commands

| Command | Description |
|---|---|
| `/commit` | Stage all changes and commit following Conventional Commits |
| `/pr <branch>` | Generate a `pr-<branch>.md` describing changes vs. a target branch |
