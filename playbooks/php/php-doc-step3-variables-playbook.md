Hi Devin! This playbook will guide you through Phase 3 of documenting PHP code, focusing specifically on class properties and constants.

### Prerequisites
- Completed Phase 1 (Class Documentation)
- Completed Phase 2 (Method Documentation)
- Access to the target PHP project folder
- Knowledge of PHP documentation standards
- Understanding of PHPDoc standards

### Instructions

1. **Initial Setup**
   - Ensure Phase 1 and 2 documentation is complete and approved
   - Review the list of classes from previous phases

2. **Class Properties Documentation Process**
   ```php
   class ExampleClass
   {
       /**
        * [Brief property description]
        *
        * [Additional details if needed]
        *
        * @var Type Description of the property type
        */
       private $propertyName;

       /**
        * @inheritdoc
        */
       protected $inheritedProperty;

       /**
        * @var Type
        */
       public const CONSTANT_NAME = value;
   }
   ```

3. **Magic Properties Documentation Process**
   ```php
   /**
    * Class docstring (documented in Phase 1)
    *
    * @property Type $propertyName Description of magic property
    * @property-read Type $readOnlyProperty Description of read-only property
    * @property-write Type $writeOnlyProperty Description of write-only property
    */
   class ExampleClass
   {
       // Implementation
   }
   ```

4. **Phase 3 Documentation Checklist**
   For each property:
   - [ ] Clear, concise description
   - [ ] Type information documented
   - [ ] Visibility documented
   - [ ] Default values documented (if applicable)
   - [ ] @inheritdoc used for inherited properties
   - [ ] Magic properties documented in class docblock
   - [ ] Validation rules documented (if any)

5. **Example Documentation**
   ```php
   /**
    * User Manager Class (documented in Phase 1)
    *
    * @property-read DateTime $lastLoginTime User's last login timestamp
    * @property-write string $password User's password (write-only for security)
    * @property array $preferences User's customizable preferences
    */
   class UserManager
   {
       /**
        * Maximum number of failed login attempts
        *
        * Used for security rate limiting and account protection.
        *
        * @var int
        */
       public const MAX_LOGIN_ATTEMPTS = 5;

       /**
        * User's unique identifier
        *
        * Primary key used in database operations and API calls.
        *
        * @var int
        */
       private $userId;

       /**
        * User's current session token
        *
        * Regenerated on each successful authentication.
        * Null if user is not authenticated.
        *
        * @var string|null
        */
       private $sessionToken;

       /**
        * @inheritdoc
        */
       protected $rolePermissions;

       /**
        * Cache of user's recent activities
        *
        * Limited to last 100 actions for performance.
        * Auto-pruned on new entries.
        *
        * @var array<int, array{
        *   action: string,
        *   timestamp: DateTime,
        *   details: array<string, mixed>
        * }>
        */
       private $activityLog = [];
   }
   ```

6. **Validation**
   - Review each documented property
   - Ensure documentation is clear and helpful
   - Verify all checklist items are complete
   - Get final approval for the class's documentation

Remember:
- Focus on properties and constants in this phase
- Keep descriptions succinct but informative
- Use @inheritdoc for inherited properties
- Document magic properties in class docblock
- Ensure documentation helps with IDE integration
- Document any validation rules or constraints

Need help? Refer to the "PHP Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
