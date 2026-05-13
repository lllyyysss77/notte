```markdown
# notte Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the core development patterns and workflows for the `notte` Python codebase. The repository is organized into modular packages (e.g., `notte-core`, `notte-sdk`, `notte-browser`) and emphasizes clear coding conventions, test-driven development, and maintainable documentation practices. Whether you're adding new features, fixing bugs, or updating documentation, this guide will help you follow the established standards.

## Coding Conventions

- **File Naming:** Use `snake_case` for all Python files.
  - Example: `notte_utils.py`, `test_feature_x.py`
- **Import Style:** Prefer *relative imports* within packages.
  - Example:
    ```python
    from .notte_utils import helper_function
    ```
- **Export Style:** Use *named exports* (explicitly define what is exported).
  - Example:
    ```python
    __all__ = ['MyClass', 'helper_function']
    ```
- **Commit Messages:** Freeform, no strict prefix, average length ~52 characters.

## Workflows

### Feature Implementation with Tests
**Trigger:** When you want to add a new feature or fix a bug and ensure it is tested  
**Command:** `/new-feature-with-tests`

1. Modify or add implementation files in the relevant package, e.g.:
    - `packages/notte-core/src/notte_core/your_module.py`
2. Update or add corresponding test files:
    - In `tests/`, e.g., `tests/test_your_module.py`
    - Or in `docs/src/testers/`, e.g., `docs/src/testers/test_your_module.py`
3. Run the test suite to verify your changes.
4. Commit your changes with a clear message.

**Example:**
```python
# packages/notte-core/src/notte_core/feature_x.py
def new_feature():
    return "Hello, notte!"

# tests/test_feature_x.py
from notte_core.feature_x import new_feature

def test_new_feature():
    assert new_feature() == "Hello, notte!"
```

### Documentation Update with Scripted Content
**Trigger:** When you need to update documentation, especially after SDK/API changes, ensuring examples and reference docs are current  
**Command:** `/update-docs`

1. Modify or add documentation files in `docs/src/`, e.g., `docs/src/usage_guide.mdx`
2. Run or update scripts in `docs/src/scripts/` to generate or inline content.
    - Example: `python docs/src/scripts/generate_reference.py`
3. Update SDK reference files in `docs/src/sdk-reference/`
4. Update or add example/tester files in `docs/src/testers/` or `docs/src/snippets/`
5. Review the rendered docs to ensure accuracy.

**Example:**
```python
# docs/src/scripts/generate_reference.py
def generate_reference():
    # Script to auto-generate SDK docs
    pass
```

## Testing Patterns

- **Framework:** Unknown (use standard Python testing frameworks like `pytest` or `unittest` if unsure)
- **Test File Pattern:** Files matching `*.test.*` or located in `tests/` or `docs/src/testers/`
- **Test Example:**
    ```python
    # tests/test_sample.py
    def test_addition():
        assert 1 + 1 == 2
    ```

## Commands

| Command                   | Purpose                                                |
|---------------------------|--------------------------------------------------------|
| /new-feature-with-tests   | Start a new feature or bugfix with corresponding tests |
| /update-docs              | Update documentation and regenerate scripted content   |
```
