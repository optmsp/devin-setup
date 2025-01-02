Hi Devin! I need you to help me create a new playbook for this repository following our team's best practices and standards.

## Project Requirements

Please implement the following steps to create a new playbook:

1. Create a new playbook file in the correct location:
   - Place the file under `/playbooks/{technology}/` directory
   - Name the file `{technology}-playbook.md`
   - Example: `/playbooks/vuejs/vuejs-playbook.md`

2. Follow this exact structure for the playbook content:

```markdown
Hi Devin! I need you to help me set up a {technology} project following our team's best practices and configuration standards.

## Project Requirements

Please implement the following configurations and standards for this {technology} project:

1. Please set up {linting/formatting tools} with these exact configurations:

[Configuration code blocks with comments]

2. Create this GitHub Actions workflow file at `.github/workflows/ci.yml`:

[CI/CD configuration with comments]

3. Set up the following project structure and ensure all new code follows this organization:

[Project structure with comments explaining each directory]

4. Install and configure these essential development tools:
   [List of required tools with their purposes]

Additional Requirements:
- Use semantic commit messages
- Set up pre-commit hooks
- Follow {technology} naming conventions
- Add appropriate documentation
- Include README.md with setup instructions
- [Technology-specific requirements]

Please create a pull request once you've implemented these configurations. Make sure to:
- Test all configurations
- Verify CI workflow passes
- Include necessary documentation
```

3. Essential elements every playbook must include:
   - Direct instructions to Devin
   - Clear, numbered steps
   - Exact configuration examples
   - Project structure with comments
   - Required tools and extensions
   - Additional requirements section
   - Final verification steps

4. Format requirements:
   - Use clear, direct language
   - Include detailed comments in code blocks
   - Maintain consistent indentation
   - Use markdown formatting properly
   - Keep instructions actionable

Additional Requirements:
- Test the playbook by creating a sample project
- Ensure all configurations are valid and tested
- Include clear error handling instructions
- Make the content copy-paste friendly
- Follow markdown best practices

Please create a pull request once you've created the playbook template. Make sure to:
- Verify the markdown formatting
- Test by creating a sample playbook
- Include clear usage instructions
- Document any special considerations
