```markdown
# repomix Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `repomix` TypeScript codebase. It covers file naming, import/export styles, commit message conventions, and testing patterns. While no specific workflows were detected, this guide provides best practices and command suggestions to streamline your development process.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    user-profile.ts
    data-fetcher.test.ts
    ```

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './data-fetcher';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In data-fetcher.ts
    export function fetchData(url: string): Promise<Data> { ... }
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `chore` prefix for routine tasks.
- Keep commit messages concise (average ~77 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

_No explicit workflows detected in the repository. Below are suggested common workflows for TypeScript projects._

### Run Tests
**Trigger:** When you want to execute the test suite.
**Command:** `/run-tests`

1. Ensure dependencies are installed.
2. Run the test command (commonly `npm test` or `yarn test`).
3. Review test output for failures.

### Lint Code
**Trigger:** Before committing code to ensure style consistency.
**Command:** `/lint-code`

1. Run the linter (commonly `npm run lint` or `yarn lint`).
2. Fix any reported issues.
3. Re-run until no errors remain.

### Make a Commit
**Trigger:** After making changes to the codebase.
**Command:** `/make-commit`

1. Stage your changes:  
   ```
   git add .
   ```
2. Write a conventional commit message, e.g.:  
   ```
   git commit -m "chore: refactor data-fetcher module"
   ```
3. Push your changes:  
   ```
   git push
   ```

## Testing Patterns

- Test files use the `*.test.*` naming pattern.
  - Example:  
    ```
    data-fetcher.test.ts
    ```
- The specific testing framework is not detected; use standard TypeScript testing practices.
- Example test file:
  ```typescript
  import { fetchData } from './data-fetcher';

  describe('fetchData', () => {
    it('should return data for a valid URL', async () => {
      const data = await fetchData('https://api.example.com/data');
      expect(data).toBeDefined();
    });
  });
  ```

## Commands
| Command      | Purpose                                    |
|--------------|--------------------------------------------|
| /run-tests   | Run the test suite                         |
| /lint-code   | Lint the codebase for style issues         |
| /make-commit | Commit changes with a conventional message |
```
