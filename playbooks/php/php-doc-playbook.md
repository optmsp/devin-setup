# PHP Documentation Process Overview

This guide provides developers with a high-level overview of the phased approach to documenting PHP code. It outlines the process that will occur when using Devin to document your PHP codebase. The documentation process is divided into three distinct phases to ensure thorough and organized documentation.

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
1. Copy the Phase 1 playbook (`php-doc-step1-classes-playbook.md`) to Devin
2. Devin will document classes and request your approval
3. Copy the Phase 2 playbook (`php-doc-step2-methods-playbook.md`) to Devin
4. Devin will document methods and request your approval
5. Copy the Phase 3 playbook (`php-doc-step3-variables-playbook.md`) to Devin
6. Devin will document variables and request your final approval

### Important Notes
- Each phase must be completed and approved before proceeding to the next
- Devin will follow the PHP Code Documentation KB guidelines
- Devin will use PHPStan for validation when available
- Documentation will focus on clarity and maintainability

### Implementation Steps
To begin documentation with Devin, copy and paste the following playbooks in sequence:
1. Phase 1 (Classes): Copy `php-doc-step1-classes-playbook.md` to Devin
2. Phase 2 (Methods): Copy `php-doc-step2-methods-playbook.md` to Devin after Phase 1 approval
3. Phase 3 (Variables): Copy `php-doc-step3-variables-playbook.md` to Devin after Phase 2 approval
