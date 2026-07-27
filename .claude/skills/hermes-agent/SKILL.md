```markdown
# hermes-agent Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns used in the `hermes-agent` TypeScript repository. You'll learn about its coding conventions, commit patterns, file organization, and how to work with and test the codebase effectively. This guide is ideal for contributors looking to maintain consistency and quality in their contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `messageHandler.ts`, `userSessionManager.ts`

### Import Style
- Use **relative imports** for referencing modules within the codebase.
  - Example:
    ```typescript
    import { processMessage } from './messageProcessor';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // In messageProcessor.ts
    export function processMessage(msg: string) { ... }

    // In another file
    import { processMessage } from './messageProcessor';
    ```

### Commit Patterns
- Follow **Conventional Commits** with the `feat` prefix for new features.
  - Example:
    ```
    feat: add support for multi-user sessions
    ```

## Workflows

_No automated workflows detected in this repository._

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example: `messageHandler.test.ts`
- The testing framework is **unknown** (not detected), but tests are likely colocated with source files or in a dedicated test directory.
- To write a test:
  1. Create a file named after the module you are testing, with `.test.ts` as the suffix.
  2. Use named exports for test utilities if needed.
  3. Follow the same import/export and file naming conventions as the main codebase.

  Example:
  ```typescript
  // messageHandler.test.ts
  import { processMessage } from './messageHandler';

  describe('processMessage', () => {
    it('should process a valid message', () => {
      // test implementation
    });
  });
  ```

## Commands

| Command | Purpose |
|---------|---------|
| /test   | Run all test files matching `*.test.*` |
| /commit | Create a conventional commit (e.g., `feat: ...`) |

```