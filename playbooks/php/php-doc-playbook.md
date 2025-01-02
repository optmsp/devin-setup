Hi Devin! This playbook will guide you through documenting PHP code in a project folder. Please follow these instructions carefully.

### Prerequisites
- Access to the target PHP project folder
- Knowledge of PHP documentation standards (refer to "PHP Code Documentation KB" in your knowledge base)
- PHPStan or similar static analysis tool for validation (if available in the project)

### Instructions

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

3. **Documentation Process**
   For each class in your inventory:

   a. **Class Documentation**
   ```php
   /**
    * [Brief class description]
    *
    * [Detailed explanation of class purpose and functionality]
    */
   ```

   b. **Property Documentation**
   ```php
   /**
    * Database connection instance
    */
   private $db;

   /**
    * @inheritdoc
    */
   protected $config;

   /**
    * @property string $name User's full name
    * @property-read int $id User's unique identifier
    */
   class User
   ```

   c. **Method Documentation**
   ```php
   /**
    * Authenticates a user with the given credentials
    *
    * @param string $username User's login name
    * @param string $password User's password
    * @return bool True if authentication successful
    * @throws AuthenticationException When credentials are invalid
    */
   public function authenticate(string $username, string $password): bool
   ```

4. **Documentation Checklist**
   For each file, ensure:
   - [ ] Class has a clear, concise description
   - [ ] Properties are documented with types and descriptions
   - [ ] Methods have parameter and return type documentation
   - [ ] Exceptions are documented where thrown
   - [ ] Magic properties are documented with @property tags
   - [ ] Inherited documentation uses @inheritdoc where appropriate

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

### Example Documentation

Here's a complete example of a well-documented class:

```php
/**
 * Manages user preferences and settings
 *
 * Handles storage, retrieval, and validation of user-specific
 * configuration options with support for default values and
 * type validation.
 */
class UserPreferences
{
    /**
     * Default preferences for new users
     */
    private array $defaults;

    /**
     * @inheritdoc
     */
    protected $storage;

    /**
     * Creates a new preferences manager for the specified user
     *
     * @param int $userId User's unique identifier
     * @param array $defaults Optional default preferences
     * @throws UserNotFoundException When user doesn't exist
     */
    public function __construct(int $userId, array $defaults = [])
    {
        $this->defaults = $defaults;
    }

    /**
     * Retrieves a user preference value
     *
     * @param string $key Preference identifier
     * @param mixed $default Value to return if preference not set
     * @return mixed The preference value or default if not found
     */
    public function get(string $key, $default = null)
    {
        // Implementation
    }
}
```

### Completion Checklist

Before considering the documentation complete:

1. [ ] All non-test classes are documented
2. [ ] Documentation is clear and concise
3. [ ] No @see tags are used
4. [ ] All inherited documentation uses @inheritdoc
5. [ ] PHPStan/IDE validation passes
6. [ ] Documentation follows project standards
7. [ ] All magic properties are documented
8. [ ] Exception documentation is complete

Remember to integrate any existing documentation that contains important caveats or TODOs, and ensure all documentation serves to make the code more maintainable for future developers.

Need help? Refer to the "PHP Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
