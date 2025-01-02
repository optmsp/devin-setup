Hi Devin! I need you to help me set up a React project following our team's best practices and configuration standards.

## Project Requirements

Please implement the following configurations and standards for this React project:

1. Please set up ESLint and Prettier with these exact configurations:

```json
{
  "eslint": {
    "semi": ["error", "always"],
    "quotes": ["error", "single"],
    "indent": ["error", 2],
    "react/jsx-pascal-case": ["error"],
    "react/jsx-closing-bracket-location": ["error", "line-aligned"]
  },
  "prettier": {
    "semi": true,
    "singleQuote": true,
    "tabWidth": 2,
    "trailingComma": "es5",
    "bracketSameLine": false
  }
}
```

2. Create this GitHub Actions workflow file at `.github/workflows/ci.yml`:

```yaml
name: React CI/CD

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
      - uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm ci
      - run: npm run lint
      - run: npm test
```

3. Set up the following project structure and ensure all new code follows this organization:

```
src/
  components/  # Reusable React components
  hooks/       # Custom React hooks
  pages/       # Route components
  services/    # API and external service integrations
  utils/       # Helper functions and utilities
  styles/      # Global styles and theme configuration
```

4. Install and configure these essential development tools:
   - ESLint for code linting
   - Prettier for code formatting
   - GitLens for Git integration
   - ES7+ React/Redux/React-Native snippets
   - npm Intellisense for package management

Additional Requirements:
- Use semantic commit messages (feat:, fix:, docs:, etc.)
- Set up pre-commit hooks to run linting before commits
- Follow React naming conventions (PascalCase for components)
- Add JSDoc comments for components and functions
- Include README.md with setup and development instructions
- Place JSX closing brackets on new lines for better readability

Please create a pull request once you've implemented these configurations. Make sure to test the linting and CI workflow before submitting.
