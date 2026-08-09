```markdown
# wails Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill provides guidance on contributing to the `wails` Go codebase. It covers the project's coding conventions, commit patterns, and common development workflows—including bugfixing with test updates, platform-specific build asset changes, and changelog entry management. Use this as a reference for writing code, structuring commits, and automating routine tasks in the repository.

## Coding Conventions

- **File Naming:**  
  Use `snake_case` for file names.  
  _Example:_  
  ```
  build_assets.go
  dot_desktop_test.go
  ```

- **Imports:**  
  Use **relative imports** within the project.  
  _Example:_  
  ```go
  import "../internal/commands"
  ```

- **Exports:**  
  Use **named exports** for functions, types, and variables.  
  _Example:_  
  ```go
  func BuildAssets() error {
      // implementation
  }
  ```

- **Commit Messages:**  
  Follow the **conventional commit** style.  
  - Prefixes: `fix`, `chore`
  - Example:  
    ```
    fix: correct asset path resolution on Linux
    chore: update build asset templates for macOS Ventura
    ```

## Workflows

### Bugfix with Test Update
**Trigger:** When fixing a bug and ensuring it is tested  
**Command:** `/bugfix-with-test`

1. Identify and fix the bug in the relevant implementation file(s).
2. Update or add test files to cover the bug scenario.
3. Commit both the fix and the test update together.

_Example:_
```go
// Fix in implementation file
func ResolveAssetPath(path string) string {
    // bugfix applied here
}

// Corresponding test update
func TestResolveAssetPath(t *testing.T) {
    // new/updated test case for the bug
}
```
Commit message:
```
fix: handle empty asset paths in build assets
```

### Platform-Specific Build Asset Update
**Trigger:** When platform requirements change or a bug is found in build asset generation  
**Command:** `/update-platform-build-assets`

1. Update template or configuration files for a specific platform (e.g., macOS, Linux).
2. Update or add related test files to validate the change.
3. Commit all related files together.

_Example:_
- Edit: `v3/internal/commands/build_assets/mac_template.go`
- Update test: `v3/internal/commands/darwin_version_test.go`

Commit message:
```
chore: update macOS build asset template for Ventura compatibility
```

### Changelog Entry for PR
**Trigger:** When a PR is merged that requires a changelog entry  
**Command:** `/add-changelog-entry`

1. Edit the `v3/UNRELEASED_CHANGELOG.md` file.
2. Add a new entry summarizing the PR and referencing its number.
3. Commit the changelog update.

_Example:_
```markdown
- fix: resolve asset path issue on Linux (#1234)
```
Commit message:
```
chore: add changelog entry for PR #1234
```

## Testing Patterns

- **Test Files:**  
  Test files use the pattern `*_test.go` for Go and `.test.js` for JavaScript.
- **Framework:**  
  No specific Go testing framework detected; standard Go `testing` package is likely used.
- **Placement:**  
  Tests are located alongside implementation files.

_Example:_
```go
// v3/internal/commands/dot_desktop_test.go
func TestDotDesktopGeneration(t *testing.T) {
    // test logic here
}
```

## Commands

| Command                      | Purpose                                                        |
|------------------------------|----------------------------------------------------------------|
| /bugfix-with-test            | Fix a bug and update/add corresponding tests                   |
| /update-platform-build-assets| Update platform-specific build assets and related tests         |
| /add-changelog-entry         | Add or update a changelog entry for a merged PR                |
```
