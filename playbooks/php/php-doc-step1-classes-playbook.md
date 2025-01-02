Hi Devin! This playbook will guide you through Phase 1 of documenting PHP code, focusing specifically on class-level documentation.

### Prerequisites
- Access to the target PHP project folder
- Knowledge of PHP documentation standards (refer to "PHP Code Documentation KB" in your knowledge base)
- Understanding of PHPDoc standards

### Instructions

1. **Initial Setup**
   ```bash
   # List all PHP files
   find . -type f -name "*.php" > php_files.txt
   ```

2. **Class Documentation Process**
   For each class:

   ```php
   /**
    * [Brief class description]
    *
    * [Detailed explanation of class purpose and functionality]
    * Focus on the class's overall responsibility and role in the system.
    * Describe what problem it solves and how it fits into the application.
    * Do not document methods or properties in this phase.
    */
   ```

3. **Phase 1 Documentation Checklist**
   For each class:
   - [ ] Class has clear, concise description
   - [ ] Class's purpose and responsibility is well documented
   - [ ] Documentation follows no-prefix rule (avoid "Description:" or "Summary:")
   - [ ] Documentation is focused on class-level concerns only
   - [ ] Documentation explains class's role in the application
   - [ ] Documentation helps new developers understand the system

4. **Example Documentation**
   ```php
   <?php

   /**
    * User Authentication Service
    *
    * A comprehensive authentication service that manages user access and
    * security within the application. This class serves as the central
    * authority for all authentication-related operations, ensuring
    * consistent and secure user authentication across the entire system.
    *
    * The service is designed with security best practices in mind and
    * integrates seamlessly with the application's user management and
    * authorization systems. It provides a robust foundation for handling
    * user authentication while maintaining flexibility for different
    * authentication methods.
    */
   class AuthenticationService
   {
       // Methods and properties will be documented in later phases
   }
   ```

5. **Validation**
   - Review each documented class
   - Ensure documentation is clear and helpful
   - Verify all checklist items are complete
   - Get approval before proceeding to Phase 2

Remember:
- Focus only on class-level documentation in this phase
- Methods and properties will be documented in Phase 2
- Get approval before proceeding to the next phase


Need help? Refer to the "PHP Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
