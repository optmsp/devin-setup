Hi Devin! This playbook will guide you through Phase 1 of documenting Vue.js code, focusing specifically on component-level documentation.

### Prerequisites
- Access to the target Vue.js project folder
- Knowledge of Vue.js documentation standards (refer to "Vue.js Code Documentation KB" in your knowledge base)
- Vue.js DevTools for component inspection (if available)

### Instructions

1. **Initial Setup**
   ```bash
   # List all Vue component files
   find . -type f -name "*.vue" > components.txt
   ```

2. **Component Documentation Process**
   For each component:

   ```vue
   /**
    * [Brief component description]
    *
    * [Detailed explanation of component purpose and functionality]
    * Focus on the component's overall responsibility and role in the system.
    * Describe what problem it solves and how it fits into the application.
    * Do not document props, events, or methods in this phase.
    */
   ```

3. **Phase 1 Documentation Checklist**
   For each component:
   - [ ] Component has clear, concise description
   - [ ] Component's purpose and responsibility is well documented
   - [ ] Documentation follows no-prefix rule (avoid "Description:" or "Summary:")
   - [ ] Documentation is focused on component-level concerns only
   - [ ] Documentation explains component's role in the application
   - [ ] Documentation helps new developers understand the system

4. **Example Documentation**
   ```vue
   <template>
     <div class="user-card">
       <!-- Template implementation will be documented in later phases -->
     </div>
   </template>

   <script>
   /**
    * User Card Component
    *
    * A reusable card component for displaying user information with a 
    * consistent layout across the application. This component serves as
    * the primary user interface element for showing user details in lists,
    * grids, and individual profile views.
    *
    * The component is designed to be flexible and maintainable, supporting
    * various display modes and customization options through its API.
    * It integrates with the application's design system and follows
    * accessibility best practices.
    */
   export default {
     name: 'UserCard'
     // Props, methods, and events will be documented in later phases
   }
   </script>
   ```

5. **Validation**
   - Review each documented component
   - Ensure documentation is clear and helpful
   - Verify all checklist items are complete
   - Get approval before proceeding to Phase 2

Remember:
- Focus only on component-level documentation in this phase
- Props, events, and methods will be documented in Phase 2
- Get approval before proceeding to the next phase

Need help? Refer to the "Vue.js Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
