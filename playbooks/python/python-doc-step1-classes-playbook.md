Hi Devin! This playbook will guide you through Phase 1 of documenting Python code, focusing specifically on module and class-level documentation.

### Prerequisites
- Access to the target Python project folder
- Knowledge of Python documentation standards (refer to "Python Code Documentation KB" in your knowledge base)
- Understanding of PEP 257 and PEP 484

### Instructions

1. **Initial Setup**
   ```bash
   # List all Python files
   find . -type f -name "*.py" > python_files.txt
   ```

2. **Module and Class Documentation Process**
   For each module and class:

   ```python
   """
   [Brief module/class description]

   [Detailed explanation of module/class purpose and functionality]
   Focus on the module/class's overall responsibility and role in the system.
   Describe what problem it solves and how it fits into the application.
   Do not document methods or attributes in this phase.

   Examples:
       Basic usage example (without implementation details)
   """
   ```

3. **Phase 1 Documentation Checklist**
   For each module/class:
   - [ ] Module/class has clear, concise docstring
   - [ ] Purpose and responsibility is well documented
   - [ ] Documentation follows no-prefix rule (avoid "Description:" or "Summary:")
   - [ ] Documentation is focused on module/class-level concerns only
   - [ ] Documentation explains role in the application
   - [ ] Documentation helps new developers understand the system

4. **Example Documentation**
   ```python
   """
   User Authentication Module

   A comprehensive authentication system that manages user access and
   security within the application. This module serves as the central
   authority for all authentication-related operations, ensuring
   consistent and secure user authentication across the entire system.

   The module is designed with security best practices in mind and
   integrates seamlessly with the application's user management and
   authorization systems.

   Examples:
       Basic module usage (implementation details in later phases):
       >>> from auth import Authenticator
       >>> auth = Authenticator()
   """

   class Authenticator:
       """
       Core authentication service for the application.
       
       This class serves as the primary authentication provider,
       implementing industry-standard security practices and providing
       a robust foundation for user authentication. It coordinates
       with other security services to maintain a secure environment
       and manages the complete authentication lifecycle.
       
       The authenticator is designed to be scalable and maintainable,
       supporting various authentication methods and security policies
       while remaining easy to extend for future requirements.
       """
       # Methods and attributes will be documented in later phases
       pass
   ```

5. **Validation**
   - Review each documented module and class
   - Ensure documentation is clear and helpful
   - Verify all checklist items are complete
   - Get approval before proceeding to Phase 2

Remember:
- Focus only on module/class-level documentation in this phase
- Methods and attributes will be documented in Phase 2
- Get approval before proceeding to the next phase

Need help? Refer to the "Python Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
