---
name: changelog-entry-for-pr
description: Workflow command scaffold for changelog-entry-for-pr in wails.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /changelog-entry-for-pr

Use this workflow when working on **changelog-entry-for-pr** in `wails`.

## Goal

Adds or updates a changelog entry referencing a specific pull request after a feature or fix is merged.

## Common Files

- `v3/UNRELEASED_CHANGELOG.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit the UNRELEASED_CHANGELOG.md file.
- Add a new entry summarizing the PR and referencing its number.
- Commit the changelog update.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.