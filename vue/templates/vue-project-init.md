# Vue.js Project Initialization Template

This template provides best practices for initializing a new Devin session with Vue.js project configuration knowledge.

## Initial Knowledge Set

When creating a new Devin session for a Vue.js project, provide these configuration preferences:

### Code Style and Linting
```json
{
  "eslint": {
    "semi": ["error", "always"],
    "quotes": ["error", "single"],
    "indent": ["error", 2],
    "vue/component-name-in-template-casing": ["error", "PascalCase"]
  },
  "prettier": {
    "semi": true,
    "singleQuote": true,
    "tabWidth": 2,
    "trailingComma": "es5"
  }
}
```

### CI/CD Configuration
```yaml
name: Vue.js CI/CD

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
      - run: npm run test:unit
```

### Project Structure
```
src/
  assets/
  components/
  views/
  router/
  store/
  utils/
```

## How to Use with Devin

1. Create a new Devin session
2. Provide this configuration as initial knowledge:
   ```
   Please set up a Vue.js project with:
   - ESLint and Prettier for code quality
   - Semicolons required at end of statements
   - Single quotes for strings
   - 2-space indentation
   - GitHub Actions CI/CD with linting and testing
   - Component names in PascalCase
   ```

## Common Extensions and Tools
- Volar (Vue Language Features)
- ESLint
- Prettier
- GitLens
- npm Intellisense
