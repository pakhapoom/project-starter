# Claude Instructions

## Package Manager
Use `uv` for all Python dependency and execution tasks — never use `pip`, `python`, or `python3` directly.

| Task | Command |
|---|---|
| Sync dependencies / prepare venv | `uv sync` |
| Install a package | `uv add <package>` (space-separated for multiple) |
| Run a Python file | `uv run <path/to/file.py>` |
| Run a module command (e.g. pytest) | `uv run pytest <path/to/tests>` |

## Code Style
- Python 3.12+
- Prefer simple, direct code over abstractions
- No unnecessary comments, docstrings, or type annotations on unchanged code

## General Preferences
- Short, concise responses — lead with the answer
- No trailing summaries after completing a task
- Ask before taking irreversible actions (force push, deleting files, etc.)
