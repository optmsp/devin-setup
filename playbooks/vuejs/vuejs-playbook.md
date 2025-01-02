Hi Devin! I need you to help me set up a Vue.js project following our team's best practices and configuration standards.

## Project Requirements

Please implement the following configurations and standards for this Vue.js project:

1. Please set up ESLint and Prettier with these exact configurations:

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

2. Create this GitHub Actions workflow file at `.github/workflows/ci.yml`:

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

3. Set up the following project structure and ensure all new code follows this organization:

```
src/
  assets/      # Static files like images and fonts
  components/  # Reusable Vue components
  views/       # Page-level components
  router/      # Vue Router configuration
  store/       # State management (Vuex/Pinia)
  utils/       # Helper functions and utilities
```

4. Install and configure these essential development tools:
   - Volar for Vue.js language support
   - ESLint for code linting
   - Prettier for code formatting
   - GitLens for Git integration
   - npm Intellisense for package management

Additional Requirements:
- Use semantic commit messages (feat:, fix:, docs:, etc.)
- Set up pre-commit hooks to run linting before commits
- Follow Vue.js style guide for component naming (PascalCase)
- Add JSDoc comments for components and functions
- Include README.md with setup and development instructions

Please create a pull request once you've implemented these configurations. Make sure to test the linting and CI workflow before submitting.
