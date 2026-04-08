---
name: pr
description: Generate a markdown file describing changes in the current branch compared to a target branch.
allowed-tools: Bash(git log:*), Bash(git diff:*), Bash(git status:*), Bash(git branch:*)
argument-hint: <target-branch>
---

# Instructions

Generate a markdown file that describes the changes in the current branch compared to `$ARGUMENTS` (the target branch).

1. Run `git branch --show-current` to get the current branch name
2. Run `git log $ARGUMENTS..HEAD --oneline` to list commits in this branch
3. Run `git diff $ARGUMENTS...HEAD --stat` to see which files changed
4. Run `git diff $ARGUMENTS...HEAD` to understand the actual changes
5. Write a file named `pr-<current-branch>.md` in the project root with the structure below
6. Do not open a GitHub PR — only create the markdown file

## Output format

```markdown
# PR: <current branch>

**Target branch:** <target-branch>

## Summary

<2-4 sentences describing what this branch does and why>

## Changes

- <bullet per logical change, grouped by concern — not per file>

## Files changed

<list files with a one-line note on what changed in each>
```

Note:
- Keep the summary focused on intent, not implementation details
- Group related file changes under the same bullet in "Changes"
- Do not include the raw diff or commit hashes in the output
- Write each bullet in plain English as a complete action, e.g. "Add retry logic to the API client" not "retry logic added / api_client.py modified"
- Avoid technical jargon, file paths, or variable names in bullets unless essential for clarity
- Each bullet should be understandable without reading the code
