Hi Devin! This playbook will guide you through documenting React code in a project folder. Please follow these instructions carefully.

### Prerequisites
- Access to the target React project folder
- Knowledge of React documentation standards (refer to "React Code Documentation KB" in your knowledge base)
- React Developer Tools for component inspection (if available)

### Instructions

1. **Initial Setup**
   ```bash
   # List all React component files
   find /path/to/folder -name "*.jsx" -o -name "*.tsx" -type f
   ```

2. **Component Inventory**
   - Create a list of all components needing documentation
   - For each component:
     ```jsx
     /**
      * UserProfile Component
      *
      * Displays user information with editable fields and
      * handles profile updates through a form interface.
      *
      * @component
      * @example
      * ```jsx
      * <UserProfile
      *   userId={123}
      *   editable={true}
      *   onUpdate={(data) => handleUpdate(data)}
      * />
      * ```
      */
     ```

3. **Documentation Process**
   For each component:

   a. **Component Documentation**
   ```jsx
   /**
    * [Brief component description]
    *
    * [Detailed explanation of component purpose and functionality]
    *
    * @component
    */
   ```

   b. **Props Documentation**
   ```jsx
   import PropTypes from 'prop-types';
   // or using TypeScript
   interface UserProfileProps {
     /**
      * The user's unique identifier
      */
     userId: number;
     /**
      * Whether the profile is editable
      * @default false
      */
     editable?: boolean;
   }
   ```

   c. **Hooks Documentation**
   ```jsx
   /**
    * Custom hook for managing user data
    *
    * @param {number} userId - The user's unique identifier
    * @returns {Object} User data and update functions
    */
   const useUserData = (userId) => {
     // Implementation
   };
   ```

4. **Documentation Checklist**
   For each component:
   - [ ] Component has clear description
   - [ ] Props are documented with types
   - [ ] Custom hooks are documented
   - [ ] Methods have parameter documentation
   - [ ] Examples provided for complex features
   - [ ] Context usage documented if present
   - [ ] Event handlers documented

5. **Validation Steps**
   - Test documentation in IDE
   - Verify prop types work
   - Check hook documentation
   - Review with component examples

6. **Final Review**
   - Ensure all components are documented
   - Verify documentation matches implementation
   - Check for missing prop documentation
   - Confirm documentation helps new developers

### Example Documentation

Here's a complete example of a well-documented component:

```jsx
import React from 'react';
import PropTypes from 'prop-types';

/**
 * UserCard Component
 *
 * Displays user information in a card format with
 * optional editing capabilities.
 *
 * @component
 * @example
 * ```jsx
 * <UserCard
 *   userName="John Doe"
 *   role="Admin"
 *   onEdit={(userData) => handleEdit(userData)}
 * />
 * ```
 */
const UserCard = ({ userName, role, onEdit, editable = false }) => {
  /**
   * Handles the edit button click
   * @param {React.MouseEvent} event - The click event
   */
  const handleEditClick = (event) => {
    onEdit({ userName, role });
  };

  return (
    <div className="user-card">
      <h3>{userName}</h3>
      <p>{role}</p>
      {editable && (
        <button onClick={handleEditClick}>Edit</button>
      )}
    </div>
  );
};

UserCard.propTypes = {
  /**
   * The user's full name
   */
  userName: PropTypes.string.isRequired,
  
  /**
   * The user's role in the system
   */
  role: PropTypes.string.isRequired,
  
  /**
   * Callback fired when the edit button is clicked
   * @param {Object} userData - The current user data
   */
  onEdit: PropTypes.func,
  
  /**
   * Whether the card is editable
   * @default false
   */
  editable: PropTypes.bool
};

export default UserCard;
```

### Completion Checklist

Before considering documentation complete:

1. [ ] All components are documented
2. [ ] Documentation is clear and helpful
3. [ ] Props have type definitions
4. [ ] Custom hooks are documented
5. [ ] Methods have clear documentation
6. [ ] Component examples are provided
7. [ ] Context usage is documented
8. [ ] Event handlers are documented

Remember to integrate any existing documentation and ensure all documentation makes the components more maintainable and reusable.

Need help? Refer to the "React Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
