### Vue.js Code Documentation KB

Devin, add this to your knowledge base for future reference. File it as "Vue.js Code Documentation KB" to make it easy to reference.

#### General Principles

- Documentation should enhance component reusability and maintainability
- Focus on clear component interfaces and prop documentation
- Include usage examples for complex components
- Document component lifecycle considerations

#### Documentation Steps

1. **Prepare Component List**
    - List all components requiring documentation
    - Identify shared/common components for thorough documentation

2. **Component-Level Documentation**
    - Document all components with:
        - Component's purpose and use cases
        - Dependencies and plugins
        - Browser compatibility considerations
        - Performance optimizations
    - Use `@inheritdoc` for inherited component documentation

3. **Props Documentation**
    - Document all props with:
        - Type definitions
        - Default values
        - Required/optional status
        - Validation rules
    - Use `@inheritdoc` for inherited props to avoid duplicating parent documentation

4. **Events Documentation**
    - Document all events with:
        - Event names and triggers
        - Payload structure and types
        - Usage examples
    - Use `@inheritdoc` for inherited events to avoid duplicating parent documentation

5. **Methods Documentation**
    - Document all methods with:
        - Purpose and return values
        - Parameter types
        - Usage examples
    - Use `@inheritdoc` for inherited methods to avoid duplicating parent documentation

6. **Slots Documentation**
    - Document only slots defined in the component:
        - Component-specific slot purposes
        - Local scoped slot props
        - Usage examples showing unique features

7. **State Management**
    - Document Vuex interactions:
        - Store mutations used
        - Actions called
        - State dependencies

8. **Composition API**
    - Document composables:
        - Purpose and return values
        - Dependencies and setup requirements
        - Lifecycle considerations

---

#### Directory-Wide Documentation Process

When documenting a Vue.js project:

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
    - Check for missing prop/event documentation
    - Validate examples and usage instructions
