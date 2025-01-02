Hi Devin! This playbook will guide you through Phase 1 of documenting React code, focusing specifically on component-level documentation. This is part of a phased approach where we'll document components first, then methods, and finally props and hooks.

### Prerequisites
- Access to the target React project folder
- Knowledge of React documentation standards (refer to "React Code Documentation KB" in your knowledge base)
- React Developer Tools for component inspection (if available)

### Phase 1: Component Documentation Instructions

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

3. **Component Documentation Process**
   For each component:

   ```jsx
   /**
    * [Brief component description]
    *
    * [Detailed explanation of component purpose and functionality]
    * Focus on the component's overall responsibility and role in the system.
    * Describe what problem it solves and how it fits into the application.
    * Do not document props, hooks, or methods in this phase.
    *
    * @component
    */
   ```

   Note: Props, hooks, and methods documentation will be handled in Phase 2 and Phase 3 respectively.

4. **Phase 1 Documentation Checklist**
   For each component:
   - [ ] Component has clear, concise description
   - [ ] Component's purpose and responsibility is well documented
   - [ ] Documentation follows no-prefix rule (avoid "Description:" or "Summary:")
   - [ ] Documentation is focused on component-level concerns only
   - [ ] Documentation explains component's role in the application
   - [ ] Documentation is clear and helpful for new developers

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

### Example Phase 1 Documentation

Here's an example of well-documented component-level documentation:

```jsx
import React from 'react';

/**
 * UserCard Component
 *
 * A foundational UI component for displaying user information in a 
 * standardized card format across the application. This component
 * serves as a key building block in user interfaces, providing a
 * consistent way to present user data in various contexts.
 *
 * The component is designed with flexibility in mind, supporting
 * different display modes and interaction patterns. It adheres to
 * the application's design system and accessibility guidelines,
 * making it a reliable choice for user-related displays.
 *
 * @component
 */
const UserCard = () => {
  // Implementation details will be documented in later phases
  return (
    <div className="user-card">
      {/* Component implementation will be documented in later phases */}
    </div>
  );
};

export default UserCard;
```

### Phase 1 Completion Checklist

Before proceeding to Phase 2:

1. [ ] All components have clear, concise descriptions
2. [ ] Component purposes and responsibilities are well documented
3. [ ] Documentation follows no-prefix rule
4. [ ] Documentation focuses on component-level concerns
5. [ ] Documentation explains component roles in the application
6. [ ] Documentation helps new developers understand the system

Remember:
- Focus only on component-level documentation in this phase
- Props, hooks, and methods will be documented in later phases
- Get approval before proceeding to Phase 2 (Method Documentation)

Need help? Refer to the "React Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
