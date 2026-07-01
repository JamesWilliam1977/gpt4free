```markdown
# gpt4free Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `gpt4free` Python codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to structure and run tests. This guide is ideal for contributors aiming to maintain consistency and quality in the project.

## Coding Conventions

### File Naming
- Use **snake_case** for all Python files.
  - Example: `api_client.py`, `utils/helpers.py`

### Import Style
- Use **relative imports** within the package.
  - Example:
    ```python
    from .utils import process_input
    from ..models import GPTModel
    ```

### Export Style
- Use **named exports** (explicitly define what is exported).
  - Example:
    ```python
    __all__ = ["GPTClient", "process_input"]
    ```

### Commit Messages
- Follow **conventional commit** style.
- Use prefixes such as `fix` for bug fixes.
- Commit messages are descriptive, averaging 120 characters.
  - Example:  
    ```
    fix: resolve token refresh bug in GPTClient when session expires after long inactivity
    ```

## Workflows

### Making a Code Change
**Trigger:** When you need to add a feature or fix a bug  
**Command:** `/code-change`

1. Create a new branch for your change.
2. Make changes following the coding conventions.
3. Write or update tests in files matching `*.test.*`.
4. Run tests to ensure correctness.
5. Commit your changes using the conventional commit style.
6. Open a pull request for review.

### Writing a Test
**Trigger:** When you add new functionality or fix a bug  
**Command:** `/write-test`

1. Create a test file or update an existing one, following the `*.test.*` pattern.
2. Write test functions for your code.
3. Use the project's preferred (unknown) testing framework.
4. Run the tests to verify correctness.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `api_client.test.py`).
- The specific test framework is not specified; check existing test files for examples.
- Place tests close to the code they test, or in a dedicated `tests/` directory if present.

**Example test file:**
```python
# api_client.test.py

from .api_client import GPTClient

def test_gpt_client_response():
    client = GPTClient()
    response = client.query("Hello, world!")
    assert response is not None
```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /code-change   | Start the workflow for making code changes   |
| /write-test    | Begin writing or updating tests              |
```
