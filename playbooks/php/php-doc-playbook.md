Hi Devin! This playbook provides a high-level overview of the phased approach to documenting PHP code. The documentation process is divided into three distinct phases to ensure thorough and organized documentation.

### Overview

The documentation process is broken down into three phases:

1. **Phase 1: Class Documentation**
   - Focus on class-level documentation
   - Document overall purpose and responsibilities
   - Refer to `php-doc-step1-classes-playbook.md` for implementation

2. **Phase 2: Method Documentation**
   - Document method signatures and behaviors
   - Include parameter and return types
   - Refer to `php-doc-step2-methods-playbook.md` for implementation

3. **Phase 3: Variable Documentation**
   - Document class properties and variables
   - Include type information and constraints
   - Refer to `php-doc-step3-variables-playbook.md` for implementation

### Prerequisites
- Access to the target PHP project folder
- Knowledge of PHP documentation standards (refer to "PHP Code Documentation KB")
- PHPStan or similar static analysis tool (if available)

### Process Flow
1. Begin with Phase 1 (Class Documentation)
2. Request user approval of Phase 1 documentation
3. Proceed to Phase 2 (Method Documentation)
4. Request user approval of Phase 2 documentation
5. Complete Phase 3 (Variable Documentation)
6. Request final user approval

### Important Notes
- Each phase must be completed and approved before proceeding
- Follow the PHP Code Documentation KB guidelines
- Use PHPStan for validation when available
- Focus on clarity and maintainability

For detailed implementation steps, refer to the phase-specific playbooks:
- Phase 1: `php-doc-step1-classes-playbook.md`
- Phase 2: `php-doc-step2-methods-playbook.md`
- Phase 3: `php-doc-step3-variables-playbook.md`
