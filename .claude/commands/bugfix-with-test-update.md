---
name: bugfix-with-test-update
description: Workflow command scaffold for bugfix-with-test-update in wails.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bugfix-with-test-update

Use this workflow when working on **bugfix-with-test-update** in `wails`.

## Goal

Fixes a bug in the codebase and updates or adds corresponding tests to ensure the fix is covered.

## Common Files

- `**/*.go`
- `**/*.js`
- `**/*_test.go`
- `**/*.test.js`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify and fix the bug in the relevant implementation file(s).
- Update or add test files to cover the bug scenario.
- Commit both the fix and the test update together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.