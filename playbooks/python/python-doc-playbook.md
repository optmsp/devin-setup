Hi Devin! This playbook will guide you through Phase 1 of documenting Python code, focusing specifically on module and class-level documentation. This is part of a phased approach where we'll document modules and classes first, then methods, and finally variables and properties.

### Prerequisites
- Access to the target Python project folder
- Knowledge of Python documentation standards (refer to "Python Code Documentation KB" in your knowledge base)
- Understanding of PEP 257 and PEP 484

### Phase 1: Module and Class Documentation Instructions

1. **Initial Setup**
   ```bash
   # List all Python files
   find /path/to/folder -name "*.py" -type f
   ```

2. **Module Inventory**
   - Create a list of all modules needing documentation
   - For each module:
     ```python
     """User management module.

     This module handles all user-related operations including
     authentication, authorization, and profile management.

     Examples:
         >>> from user_management import UserManager
         >>> manager = UserManager()
         >>> user = manager.create_user("john@example.com")
     """
     ```

3. **Module and Class Documentation Process**
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

   Note: Methods and attributes documentation will be handled in Phase 2 and Phase 3 respectively.

4. **Phase 1 Documentation Checklist**
   For each module/class:
   - [ ] Module/class has clear, concise docstring
   - [ ] Purpose and responsibility is well documented
   - [ ] Documentation follows no-prefix rule (avoid "Description:" or "Summary:")
   - [ ] Documentation is focused on module/class-level concerns only
   - [ ] Documentation explains role in the application
   - [ ] Documentation is clear and helpful for new developers

5. **Validation Steps**
   - Test documentation with doctest
   - Verify type hints with mypy
   - Check docstring format
   - Review with module examples

6. **Final Review**
   - Ensure all modules are documented
   - Verify documentation matches implementation
   - Check for missing type hints
   - Confirm documentation helps new developers

### Example Phase 1 Documentation

Here's an example of well-documented module and class-level documentation:

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

### Phase 1 Completion Checklist

Before proceeding to Phase 2:

1. [ ] All modules and classes have clear, concise descriptions
2. [ ] Module/class purposes and responsibilities are well documented
3. [ ] Documentation follows no-prefix rule
4. [ ] Documentation focuses on module/class-level concerns
5. [ ] Documentation explains roles in the application
6. [ ] Documentation helps new developers understand the system

Remember:
- Focus only on module/class-level documentation in this phase
- Methods and attributes will be documented in later phases
- Get approval before proceeding to Phase 2 (Method Documentation)

Need help? Refer to the "Python Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
