# Python Documentation Process Overview

This guide provides developers with a high-level overview of the phased approach to documenting Python code. It outlines the process that will occur when using Devin to document your Python codebase. The documentation process is divided into three distinct phases to ensure thorough and organized documentation.

### Overview

The documentation process is broken down into three phases:

1. **Phase 1: Module and Class Documentation**
   - Focus on module and class-level documentation
   - Document overall purpose and responsibilities
   - Refer to `python-doc-step1-classes-playbook.md` for implementation

2. **Phase 2: Method Documentation**
   - Document method signatures and behaviors
   - Include parameter and return types
   - Refer to `python-doc-step2-methods-playbook.md` for implementation

3. **Phase 3: Variable Documentation**
   - Document module/class attributes and variables
   - Include type hints and constraints
   - Refer to `python-doc-step3-variables-playbook.md` for implementation

### Prerequisites
- Access to the target Python project folder
- Knowledge of Python documentation standards (refer to "Python Code Documentation KB")
- Understanding of PEP 257 and PEP 484
- Mypy or similar type checker (if available)

### Process Flow
1. Copy the Phase 1 playbook (`python-doc-step1-classes-playbook.md`) to Devin
2. Devin will document modules/classes and request your approval
3. Copy the Phase 2 playbook (`python-doc-step2-methods-playbook.md`) to Devin
4. Devin will document methods and request your approval
5. Copy the Phase 3 playbook (`python-doc-step3-variables-playbook.md`) to Devin
6. Devin will document variables and request your final approval

### Important Notes
- Each phase must be completed and approved before proceeding to the next
- Devin will follow the Python Code Documentation KB guidelines
- Devin will use mypy for type hint validation when available
- Documentation will focus on clarity and maintainability

### Implementation Steps
To begin documentation with Devin, copy and paste the following playbooks in sequence:
1. Phase 1 (Modules/Classes): Copy `python-doc-step1-classes-playbook.md` to Devin
2. Phase 2 (Methods): Copy `python-doc-step2-methods-playbook.md` to Devin after Phase 1 approval
3. Phase 3 (Variables): Copy `python-doc-step3-variables-playbook.md` to Devin after Phase 2 approval
