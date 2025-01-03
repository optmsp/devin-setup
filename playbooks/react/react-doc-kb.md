### React Code Documentation KB

Devin, add this to your knowledge base for future reference. File it as "React Code Documentation KB" to make it easy to reference.

#### General Principles

- Documentation should enhance component reusability and maintainability
- Focus on clear component interfaces and prop types
- Include usage examples for complex components
- Document hooks and their lifecycle implications

#### Documentation Steps

1. **Prepare Component List**
    - List all components requiring documentation
    - Identify shared/reusable components
    - Note custom hooks that need documentation

2. **Component-Level Documentation**
    - Document non-inherited components with:
        - Component's unique purpose and specific use cases
        - Component-specific dependencies or context requirements
        - Browser compatibility considerations if different from parent
        - Performance optimizations specific to this component

3. **Props Documentation**
    - Document only component-specific props (not inherited):
        - PropTypes or TypeScript interfaces for new props
        - Default values for component-specific props
        - Required/optional status for added props
        - Custom validation requirements

4. **Hooks Documentation**
    - Document only custom hooks defined in the component:
        - Hook's specific purpose and return values
        - Component-specific dependencies
        - Local cleanup functions
        - Usage examples showing unique features

5. **Methods Documentation**
    - Document only component-specific methods:
        - Purpose and parameters of new methods
        - Return values and component-specific effects
        - Usage examples for overridden behavior

6. **Context Documentation**
    - Document Context providers/consumers:
        - Available context values
        - Provider configuration
        - Consumer usage patterns

7. **State Management**
    - Document Redux/state management:
        - Actions and reducers used
        - Selectors
        - State dependencies

8. **Event Handlers**
    - Document event handlers:
        - Event types and triggers
        - Parameters and return values
        - Side effects and state updates

---

#### Directory-Wide Documentation Process

When documenting a React project:

1. **Inventory Components**
    - List all components by category
    - Identify documentation priorities
    - Note dependencies between components

2. **Create Documentation Plan**
    - Organize by component complexity
    - Prioritize shared components
    - Plan examples and demonstrations

3. **Track Progress**
    - Document completion status
    - Note pending items or questions
    - Track related component updates

4. **Ensure Coverage**
    - Verify all components are documented
    - Check for missing prop documentation
    - Validate examples and usage instructions
