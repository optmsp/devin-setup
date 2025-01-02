# React Project Initialization Template

This template provides best practices for initializing a new Devin session with React project configuration knowledge.

## Initial Knowledge Set

When creating a new Devin session for a React project, provide these configuration preferences:

### Code Style and Linting
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

### CI/CD Configuration
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

### Project Structure
```
src/
  components/
  hooks/
  pages/
  services/
  utils/
  styles/
```

## How to Use with Devin

1. Create a new Devin session
2. Provide this configuration as initial knowledge:
   ```
   Please set up a React project with:
   - ESLint and Prettier for code quality
   - Semicolons required at end of statements
   - Single quotes for strings
   - 2-space indentation
   - GitHub Actions CI/CD with linting and testing
   - Component names in PascalCase
   - JSX brackets on new lines
   ```

## Common Extensions and Tools
- ESLint
- Prettier
- GitLens
- ES7+ React/Redux/React-Native snippets
- npm Intellisense
