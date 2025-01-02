# Devin Setup Best Practices

A collection of best practices and initialization templates for Devin development sessions. This repository serves as a community-driven knowledge base for starting new Devin sessions with appropriate context and configuration preferences.

## Purpose

This repository aims to standardize and optimize the initialization of Devin sessions by providing:

- Best practices for different types of projects
- Project-specific configuration templates
- Common development preferences and standards
- Easy-to-use initialization templates

## Repository Structure

```
├── playbooks/        # Collection of initialization playbooks
│   ├── vuejs/       # Vue.js best practices
│   │   └── vuejs-playbook.md         # Vue.js setup
│   ├── react/       # React best practices
│   │   └── react-playbook.md         # React setup
│   ├── python/      # Python best practices
│   │   └── python-playbook.md        # Python setup
│   ├── php/         # PHP best practices
│   │   └── php-doc-kb.md            # PHP documentation (Knowledge Bank)
│   └── meta/        # Meta playbooks
       └── playbook-creation-playbook.md
```

### File Naming Conventions

- **Playbooks**: Use `-playbook.md` suffix for all playbooks (e.g., `vuejs-playbook.md`, `vuejs-primevue-playbook.md`)
- **Knowledge Bank**: Use `-kb.md` suffix for files meant to be added to Devin's Knowledge Bank (e.g., `php-doc-kb.md`)

## Usage

1. Choose your technology (Vue.js, React, or Python)
2. Navigate to the corresponding playbook in the `playbooks` directory
3. Copy the configuration and follow the setup instructions

### Example: Vue.js Project Initialization
```
Please set up a Vue.js project with:
- ESLint and Prettier for code quality
- Semicolons required at end of statements
- Single quotes for strings
- 2-space indentation
- GitHub Actions CI/CD with linting and testing
```

See [playbooks/vuejs/vuejs-playbook.md](playbooks/vuejs/vuejs-playbook.md) for complete configuration.

## Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository
2. Create a feature branch
3. Add or update best practices following the existing structure
4. Submit a pull request

Please ensure your contributions:
- Follow the established directory structure
- Use appropriate file naming conventions:
  - `-playbook.md` for all playbooks (e.g., `vuejs-playbook.md`, `vuejs-primevue-playbook.md`)
  - `-kb.md` for Knowledge Bank files
- Include clear documentation in markdown format
- Provide practical examples and configurations
- Follow existing formatting conventions

## Benefits

- Consistent development environments across sessions
- Standardized code quality and style configurations
- Reduced setup time for new projects
- Community-driven best practices
- Easy to read, contribute, and maintain
