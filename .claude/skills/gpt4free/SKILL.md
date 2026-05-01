```markdown
# gpt4free Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `gpt4free` Python repository. You'll learn about file naming, import/export styles, commit practices, and how to structure and run tests. This guide is ideal for contributors or anyone looking to maintain consistency within the codebase.

## Coding Conventions

### File Naming
- **Style:** `snake_case`
- **Example:**  
  ```python
  # Good
  my_module.py

  # Bad
  MyModule.py
  myModule.py
  ```

### Import Style
- **Style:** Relative imports are preferred.
- **Example:**  
  ```python
  # Good
  from .utils import helper_function

  # Bad
  import utils
  from utils import helper_function
  ```

### Export Style
- **Style:** Named exports via explicit function or class definitions.
- **Example:**  
  ```python
  # Good
  def my_function():
      pass

  class MyClass:
      pass
  ```

### Commit Patterns
- **Type:** Mixed, with a preference for the `feat` prefix for new features.
- **Example:**  
  ```
  feat: add support for new API endpoint
  fix: resolve token refresh bug
  ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new capability or endpoint  
**Command:** `/add-feature`

1. Create a new Python file using `snake_case` naming.
2. Use relative imports to reference other modules.
3. Define functions/classes for your feature.
4. Write or update tests in a corresponding `*.test.*` file.
5. Commit your changes with a `feat:` prefix and a concise description.

### Writing Tests
**Trigger:** When adding or updating functionality  
**Command:** `/write-test`

1. Create or update a test file matching the pattern `*.test.*`.
2. Write test functions for new or changed code.
3. Use the project's preferred (unknown) testing framework.
4. Run tests to ensure correctness.

### Making a Commit
**Trigger:** After completing a unit of work  
**Command:** `/commit-changes`

1. Stage your changes.
2. Write a commit message using the appropriate prefix (`feat`, `fix`, etc.).
3. Keep commit messages concise (around 45 characters).
4. Push your commit to the repository.

## Testing Patterns

- **File Pattern:** Test files follow the `*.test.*` naming convention (e.g., `utils.test.py`).
- **Framework:** Not explicitly specified; check existing tests for clues.
- **Example:**
  ```python
  # utils.test.py

  def test_helper_function():
      assert helper_function(2) == 4
  ```

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /add-feature    | Scaffold and implement a new feature         |
| /write-test     | Create or update tests for your code         |
| /commit-changes | Commit your staged changes with conventions  |
```
