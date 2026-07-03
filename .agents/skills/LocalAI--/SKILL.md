```markdown
# LocalAI-- Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on contributing to the LocalAI-- repository, which is primarily written in Python with no specific framework detected. The repository emphasizes maintainable code through consistent conventions, conventional commit messages, and repeatable workflows for backend updates, gallery model management, and importer logic/testing. This document outlines the key coding conventions, common workflows, and testing patterns to help you contribute effectively.

## Coding Conventions

- **File Naming:**  
  Use camelCase for file names.  
  _Example:_  
  ```
  modelImporter.py
  tempDirectoryHandler.py
  ```

- **Import Style:**  
  Prefer relative imports within modules.  
  _Example:_  
  ```python
  from .utils import loadConfig
  from .handlers import processRequest
  ```

- **Export Style:**  
  Use named exports (i.e., explicitly define what is exported from a module).  
  _Example:_  
  ```python
  # In myModule.py
  def process_data(...):
      ...

  def validate_input(...):
      ...

  __all__ = ["process_data", "validate_input"]
  ```

- **Commit Messages:**  
  Follow the [Conventional Commits](https://www.conventionalcommits.org/) style, using prefixes like `feat` and `fix`.  
  _Example:_  
  ```
  feat: add support for custom temp directory in backend.py
  fix: resolve import error in modelImporter.py
  ```

## Workflows

### Backend Python Backend Update
**Trigger:** When a cross-backend behavior or configuration needs to be updated (e.g., temp directory handling, dependency management) in Python backends.  
**Command:** `/update-backend-python`

1. Identify the pattern or configuration to be changed across backends.
2. Edit `backend.py` files in each relevant `backend/python/*/` directory to apply the change.
3. Optionally update related `requirements-*.txt` files if dependencies are affected.
4. Document or reference the change in the commit message.

_Example:_  
```python
# backend/python/llama/backend.py
import tempfile

def get_temp_dir():
    return tempfile.gettempdir()
```

### Gallery Model Metadata Update
**Trigger:** When a new model is added to the gallery or existing model metadata/tags need updating.  
**Command:** `/update-gallery-model`

1. Edit `gallery/index.yaml` to add or update model entries or tags.
2. Include detailed descriptions and file references as needed.
3. Commit with a message referencing the models and changes.

_Example:_  
```yaml
# gallery/index.yaml
- name: llama-2
  tags: [transformer, openai-compatible]
  description: "Llama 2 model for general purpose inference"
```

### Importer Logic and Test Update
**Trigger:** When importer logic (e.g., for model importers) needs to be changed or enhanced, and the change should be covered by tests.  
**Command:** `/update-importer`

1. Edit the importer implementation file (e.g., `core/gallery/importers/modelImporter.py`).
2. Edit or add corresponding test file (e.g., `core/gallery/importers/modelImporter.test.py`) to cover the new or changed logic.
3. Commit both implementation and test changes together.

_Example:_  
```python
# core/gallery/importers/modelImporter.py
def import_model(path):
    # New logic here
    pass

# core/gallery/importers/modelImporter.test.py
def test_import_model():
    assert import_model("test-path") == expected_result
```

## Testing Patterns

- **Test File Pattern:**  
  Test files follow the `*.test.*` naming convention (e.g., `modelImporter.test.py`).

- **Framework:**  
  No specific testing framework detected; use Python's built-in `unittest` or `pytest` as appropriate.

- **Test Example:**  
  ```python
  # modelImporter.test.py
  import unittest
  from .modelImporter import import_model

  class TestModelImporter(unittest.TestCase):
      def test_import(self):
          self.assertEqual(import_model("dummy-path"), "expected")
  ```

## Commands

| Command                | Purpose                                                      |
|------------------------|--------------------------------------------------------------|
| /update-backend-python | Update or refactor logic/configuration in Python backends    |
| /update-gallery-model  | Add or update model metadata/tags in the gallery             |
| /update-importer       | Update importer logic and corresponding tests                |
```
