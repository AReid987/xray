```markdown
# xray Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `xray` TypeScript codebase. You'll learn how to structure files, write imports and exports, follow commit message conventions, and understand the testing approach. While no specific automation workflows are detected, this guide provides suggested commands and best practices for maintaining code consistency.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myComponent.ts`, `dataProcessor.ts`

### Import Style
- Use **relative imports** for referencing local modules.
  - Example:
    ```typescript
    import { processData } from './dataProcessor';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In dataProcessor.ts
    export function processData(input: string): string { ... }

    // In another file
    import { processData } from './dataProcessor';
    ```

### Commit Messages
- Follow the **conventional commits** style.
- Use the `chore` prefix for routine changes.
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

_No automated workflows detected in this repository. Below are suggested manual workflows for common tasks._

### Code Formatting
**Trigger:** Before committing code  
**Command:** `/format-code`

1. Ensure all files use camelCase naming.
2. Check that all imports are relative.
3. Use named exports exclusively.

### Commit Changes
**Trigger:** When making any code change  
**Command:** `/commit-changes`

1. Write a commit message using the conventional commit format.
2. Use the `chore` prefix for maintenance or non-feature changes.
3. Keep commit messages concise (average ~77 characters).

### Run Tests
**Trigger:** Before pushing changes  
**Command:** `/run-tests`

1. Identify test files matching the `*.test.*` pattern.
2. Run the test suite using the project's test runner (framework unknown; consult project documentation).

## Testing Patterns

- Test files are named using the `*.test.*` pattern (e.g., `myComponent.test.ts`).
- The specific test framework is not detected; check the repository or package.json for details.
- Place test files alongside the modules they test or in a dedicated test directory.
- Example test file name: `dataProcessor.test.ts`

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /format-code    | Check and enforce code style conventions     |
| /commit-changes | Guide for writing conventional commit messages|
| /run-tests      | Run all test files matching `*.test.*`       |
```