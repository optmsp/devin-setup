Hi Devin! This playbook will guide you through Phase 1 of documenting PHP code, focusing specifically on class-level documentation. This is part of a phased approach where we'll document classes first, then methods, and finally variables.

### Prerequisites
- Access to the target PHP project folder
- Knowledge of PHP documentation standards (refer to "PHP Code Documentation KB" in your knowledge base)
- PHPStan or similar static analysis tool for validation (if available in the project)

### Phase 1: Class Documentation Instructions

1. **Initial Setup**
   ```bash
   # First, list all PHP files in the target directory
   find /path/to/folder -name "*.php" -type f | grep -v "/tests/"
   ```

2. **Class Inventory**
   - Create a list of all non-test classes that need documentation
   - For each file:
     ```php
     // Example class documentation
     /**
      * Handles user authentication and session management
      *
      * Provides methods for user login, logout, and session validation
      * with support for multiple authentication providers.
      */
     class AuthenticationManager
     {
     ```

3. **Class Documentation Process**
   For each class in your inventory:

   ```php
   /**
    * [Brief class description]
    *
    * [Detailed explanation of class purpose and functionality]
    * Focus on the class's overall responsibility and role in the system.
    * Do not document methods or properties in this phase.
    */
   ```

   Note: Method and property documentation will be handled in Phase 2 and Phase 3 respectively.

4. **Phase 1 Documentation Checklist**
   For each file, ensure:
   - [ ] Class has a clear, concise description
   - [ ] Class purpose and responsibility is well documented
   - [ ] Documentation follows no-prefix rule (avoid "Description:" or "Summary:")
   - [ ] Documentation is focused on class-level concerns only
   - [ ] Documentation is clear and helpful for new developers

5. **Validation Steps**
   ```bash
   # If PHPStan is available, run:
   vendor/bin/phpstan analyse /path/to/folder --level=max
   ```
   - Review PHPStan output for documentation-related issues
   - Ensure IDE can properly interpret all type hints
   - Verify documentation renders correctly in IDE tooltips

6. **Final Review**
   - Check that all files in inventory are documented
   - Verify documentation follows project standards
   - Ensure no @see tags are used (as per KB guidelines)
   - Confirm documentation is helpful for new developers

### Example Class Documentation

Here's an example of well-documented class-level documentation:

```php
/**
 * Manages user preferences and settings
 *
 * Handles storage, retrieval, and validation of user-specific
 * configuration options with support for default values and
 * type validation. Provides a centralized way to manage user
 * preferences while ensuring type safety and proper defaults.
 * 
 * This class serves as the primary interface for all user
 * preference operations in the system.
 */
class UserPreferences
{
    // Properties and methods will be documented in later phases
}

### Phase 1 Completion Checklist

Before proceeding to Phase 2:

1. [ ] All non-test classes have clear, concise descriptions
2. [ ] Class-level documentation explains purpose and responsibilities
3. [ ] No prefixes are used in documentation
4. [ ] Documentation follows project standards
5. [ ] PHPStan/IDE validation passes for class documentation
6. [ ] Documentation is helpful for new developers

Remember:
- Focus only on class-level documentation in this phase
- Methods and properties will be documented in later phases
- Ensure documentation serves to make the code more maintainable
- Get approval before proceeding to Phase 2 (Method Documentation)

Need help? Refer to the "PHP Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
