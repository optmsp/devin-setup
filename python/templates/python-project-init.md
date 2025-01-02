# Python Project Initialization Template

This template provides best practices for initializing a new Devin session with Python project configuration knowledge.

## Initial Knowledge Set

When creating a new Devin session for a Python project, provide these configuration preferences:

### Code Style and Linting
```ini
# pyproject.toml
[tool.black]
line-length = 88
target-version = ['py38']
include = '\.pyi?$'

[tool.flake8]
max-line-length = 88
extend-ignore = 'E203'
exclude = ['.git', '__pycache__', 'build', 'dist']

[tool.pylint]
max-line-length = 88
good-names = ['i', 'j', 'k', 'ex', 'Run', '_']
disable = ['C0111', 'C0103']
```

### CI/CD Configuration
```yaml
name: Python CI/CD

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  lint-and-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v4
        with:
          python-version: '3.8'
      - run: |
          python -m pip install --upgrade pip
          pip install black flake8 pylint pytest
          pip install -r requirements.txt
      - run: black --check .
      - run: flake8 .
      - run: pylint **/*.py
      - run: pytest
```

### Project Structure
```
src/
  core/
  utils/
  services/
  models/
tests/
  unit/
  integration/
```

## How to Use with Devin

1. Create a new Devin session
2. Provide this configuration as initial knowledge:
   ```
   Please set up a Python project with:
   - Black for code formatting
   - Flake8 and Pylint for code quality
   - 88 character line length
   - PEP 8 style guide compliance
   - GitHub Actions CI/CD with linting and testing
   - Type hints required
   - Docstrings required
   ```

## Common Extensions and Tools
- Python
- Pylance
- Black Formatter
- GitLens
- Python Test Explorer
