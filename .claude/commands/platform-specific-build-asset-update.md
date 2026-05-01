---
name: platform-specific-build-asset-update
description: Workflow command scaffold for platform-specific-build-asset-update in wails.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /platform-specific-build-asset-update

Use this workflow when working on **platform-specific-build-asset-update** in `wails`.

## Goal

Updates platform-specific build assets or configuration templates, often in response to OS or toolchain changes.

## Common Files

- `v3/internal/commands/build_assets/**`
- `v3/internal/commands/updatable_build_assets/**`
- `v3/internal/commands/dot_desktop.go`
- `v3/internal/commands/dot_desktop_test.go`
- `v3/internal/commands/darwin_version_test.go`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update template or configuration files for a specific platform (e.g., macOS, Linux).
- Update or add related test files to validate the change.
- Commit all related files together.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.