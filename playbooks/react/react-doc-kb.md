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
    - Document all components with:
        - Component's purpose and use cases
        - Dependencies and context requirements
        - Browser compatibility considerations
        - Performance optimizations
    - Use `@inheritdoc` for inherited component documentation

3. **Props Documentation**
    - Document all props with:
        - PropTypes or TypeScript interfaces
        - Default values
        - Required/optional status
        - Validation requirements
    - Use `@inheritdoc` for inherited props to avoid duplicating parent documentation

4. **Hooks Documentation**
    - Document all hooks with:
        - Hook's purpose and return values
        - Dependencies and cleanup functions
        - Usage examples
    - Use `@inheritdoc` for inherited hook documentation

5. **Methods Documentation**
    - Document all methods with:
        - Purpose and parameters
        - Return values and side effects
        - Usage examples
    - Use `@inheritdoc` for inherited methods to avoid duplicating parent documentation

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
