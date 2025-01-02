Hi Devin! This playbook will guide you through documenting Python code in a project folder. Please follow these instructions carefully.

### Prerequisites
- Access to the target Python project folder
- Knowledge of Python documentation standards (refer to "Python Code Documentation KB" in your knowledge base)
- Understanding of PEP 257 and PEP 484

### Instructions

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

3. **Documentation Process**
   For each module:

   a. **Module Documentation**
   ```python
   """
   [Brief module description]

   [Detailed explanation of module purpose and functionality]

   Examples:
       [Usage examples]
   """
   ```

   b. **Class Documentation**
   ```python
   from typing import Optional, List

   class UserProfile:
       """
       User profile management class.

       Handles creation, updates, and deletion of user profiles
       with proper validation and error handling.

       Args:
           user_id: Unique identifier for the user
           name: User's full name
           email: User's email address

       Attributes:
           id (int): The user's unique identifier
           email (str): The user's email address
           is_active (bool): Whether the user account is active
       """

       def __init__(self, user_id: int, name: str, email: str) -> None:
           self.id = user_id
           self.name = name
           self.email = email
   ```

   c. **Method Documentation**
   ```python
   def update_profile(self, 
                     name: Optional[str] = None, 
                     email: Optional[str] = None) -> bool:
       """
       Update the user's profile information.

       Args:
           name: New name for the user
           email: New email address for the user

       Returns:
           bool: True if update was successful, False otherwise

       Raises:
           ValueError: If email format is invalid
           UserNotFoundError: If user doesn't exist
       """
   ```

4. **Documentation Checklist**
   For each module:
   - [ ] Module has clear docstring
   - [ ] Classes are documented with docstrings
   - [ ] Methods have parameter documentation
   - [ ] Type hints are included
   - [ ] Examples provided for complex features
   - [ ] Exceptions are documented
   - [ ] Variables have type annotations

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

### Example Documentation

Here's a complete example of a well-documented Python module:

```python
"""
User Authentication Module

This module provides user authentication functionality including
login, logout, and session management.

Examples:
    >>> from auth import Authenticator
    >>> auth = Authenticator()
    >>> user = auth.login("user@example.com", "password123")
    >>> print(user.is_authenticated)
    True
"""

from typing import Optional, Dict, Any
from datetime import datetime

class Authenticator:
    """
    Handles user authentication and session management.

    This class provides methods for user login, logout, and
    session validation with proper security measures.

    Attributes:
        session_timeout (int): Session timeout in minutes
        max_attempts (int): Maximum login attempts before lockout
    """

    def __init__(self, session_timeout: int = 30, max_attempts: int = 3) -> None:
        """
        Initialize the authenticator.

        Args:
            session_timeout: Timeout in minutes for user sessions
            max_attempts: Maximum number of failed login attempts
        """
        self.session_timeout = session_timeout
        self.max_attempts = max_attempts

    def login(self, email: str, password: str) -> Optional['User']:
        """
        Authenticate a user and create a session.

        Args:
            email: User's email address
            password: User's password

        Returns:
            User: Authenticated user object if successful,
                 None if authentication fails

        Raises:
            ValueError: If email or password is empty
            AccountLockedException: If account is locked
        """
        if not email or not password:
            raise ValueError("Email and password required")
        
        # Implementation details...
        return user

    def validate_session(self, session_id: str) -> bool:
        """
        Check if a session is valid and not expired.

        Args:
            session_id: The session identifier to validate

        Returns:
            bool: True if session is valid, False otherwise
        """
        # Implementation details...
        return True
```

### Completion Checklist

Before considering documentation complete:

1. [ ] All modules are documented
2. [ ] Documentation follows PEP 257
3. [ ] Type hints follow PEP 484
4. [ ] Classes have docstrings
5. [ ] Methods have parameter docs
6. [ ] Examples are provided
7. [ ] Exceptions are documented
8. [ ] Variables have type hints

Remember to integrate any existing documentation and ensure all documentation follows Python's documentation standards.

Need help? Refer to the "Python Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
