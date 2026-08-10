```markdown
# OpenList Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the OpenList repository, a Go-based project with a focus on clear code structure, conventional commit messages, and consistent file organization. You'll learn how to name files, structure imports/exports, write and locate tests, and follow the project's commit and workflow standards.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userHandler.go`, `listManager.go`

### Import Style
- Use **relative imports** within the project.
  - Example:
    ```go
    import "../utils"
    ```

### Export Style
- Use **named exports** for functions, types, and variables.
  - Example:
    ```go
    package list

    func GetListItems() []Item {
        // implementation
    }
    ```

### Commit Messages
- Follow **Conventional Commits** with prefixes like `fix` and `feat`.
  - Example:
    ```
    feat: add pagination to list endpoint
    fix: correct item sorting logic
    ```

## Workflows

### Conventional Commit Workflow
**Trigger:** When making any code change that will be committed.
**Command:** `/conventional-commit`

1. Make your code changes.
2. Stage your changes with `git add`.
3. Commit using a message starting with `feat:` or `fix:`, followed by a concise description (average 56 characters).
   - Example: `git commit -m "feat: implement search filter for lists"`
4. Push your changes as usual.

### File Naming Workflow
**Trigger:** When creating new files.
**Command:** `/file-naming`

1. Name new files using camelCase.
2. Avoid underscores or dashes in file names.
3. Example: Use `listManager.go` instead of `list_manager.go` or `list-manager.go`.

### Import/Export Workflow
**Trigger:** When importing or exporting code across packages.
**Command:** `/import-export`

1. Use relative imports for internal packages.
   - Example: `import "../utils"`
2. Export functions/types using named exports.
   - Example:
     ```go
     func ExportedFunction() {}
     ```

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `listManager.test.go`).
- The testing framework is not specified; use Go's standard `testing` package unless otherwise noted.
- Example test file:
  ```go
  package list

  import "testing"

  func TestGetListItems(t *testing.T) {
      // test implementation
  }
  ```

## Commands
| Command                | Purpose                                            |
|------------------------|----------------------------------------------------|
| /conventional-commit   | Guide for writing conventional commit messages     |
| /file-naming           | Instructions for naming new files                  |
| /import-export         | Steps for importing/exporting code in the project  |
```
