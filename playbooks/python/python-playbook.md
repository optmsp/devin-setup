Hi Devin! I need you to help me set up a Python project following our team's best practices and configuration standards.

## Project Requirements

Please implement the following configurations and standards for this Python project:

1. Please set up the following code style tools with these exact configurations in pyproject.toml:

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

2. Create this GitHub Actions workflow file at `.github/workflows/ci.yml`:

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

3. Set up the following project structure and ensure all new code follows this organization:

```
src/
  core/       # Core business logic
  utils/      # Helper functions and utilities
  services/   # External service integrations
  models/     # Data models and schemas
tests/
  unit/      # Unit tests
  integration/# Integration tests
```

4. Install and configure these essential development tools:
   - Python extension for language support
   - Pylance for type checking
   - Black Formatter for code formatting
   - GitLens for Git integration
   - Python Test Explorer for test management

Additional Requirements:
- Use semantic commit messages (feat:, fix:, docs:, etc.)
- Set up pre-commit hooks for Black, Flake8, and Pylint
- Follow PEP 8 style guide strictly
- Add type hints to all functions and classes
- Include detailed docstrings for all modules, classes, and functions
- Set up pytest as the testing framework
- Create a comprehensive README.md with setup instructions

Please create a pull request once you've implemented these configurations. Make sure to:
- Test all linting configurations
- Verify CI workflow passes
- Include example tests
- Document development setup process
