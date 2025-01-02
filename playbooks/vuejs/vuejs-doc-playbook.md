Hi Devin! This playbook will guide you through documenting Vue.js code in a project folder. Please follow these instructions carefully.

### Prerequisites
- Access to the target Vue.js project folder
- Knowledge of Vue.js documentation standards (refer to "Vue.js Code Documentation KB" in your knowledge base)
- Vue.js DevTools for component inspection (if available)

### Instructions

1. **Initial Setup**
   ```bash
   # List all Vue component files
   find /path/to/folder -name "*.vue" -type f
   ```

2. **Component Inventory**
   - Create a list of all components needing documentation
   - For each component:
     ```vue
     <!-- Example component documentation -->
     <template>
       <!-- Component template -->
     </template>

     <script>
     /**
      * User profile card component
      *
      * Displays user information in a card format with customizable
      * slots for header and footer content.
      */
     export default {
       name: 'UserProfileCard',
     }
     </script>
     ```

3. **Documentation Process**
   For each component:

   a. **Component Documentation**
   ```vue
   /**
    * [Brief component description]
    *
    * [Detailed explanation of component purpose and functionality]
    */
   ```

   b. **Props Documentation**
   ```vue
   export default {
     props: {
       /**
        * The user's unique identifier
        */
       userId: {
         type: Number,
         required: true
       },
       /**
        * Display mode for the profile card
        */
       mode: {
         type: String,
         default: 'compact',
         validator: value => ['compact', 'full'].includes(value)
       }
     }
   }
   ```

   c. **Events Documentation**
   ```vue
   /**
    * Emitted when the user profile is updated
    * @event update:profile
    * @property {Object} profile - Updated user profile data
    */
   this.$emit('update:profile', profile)
   ```

4. **Documentation Checklist**
   For each component:
   - [ ] Component has clear description
   - [ ] Props are documented with types and descriptions
   - [ ] Events are documented with payload types
   - [ ] Slots are documented with expected content
   - [ ] Methods have parameter and return type documentation
   - [ ] Examples provided for complex features
   - [ ] Vuex interactions documented if present

5. **Validation Steps**
   - Test documentation in IDE
   - Verify prop validation works
   - Check event documentation accuracy
   - Review with component examples

6. **Final Review**
   - Ensure all components are documented
   - Verify documentation matches implementation
   - Check for missing prop/event documentation
   - Confirm documentation helps new developers

### Example Documentation

Here's a complete example of a well-documented component:

```vue
<template>
  <div class="user-card">
    <slot name="header"></slot>
    <div class="user-info">{{ userName }}</div>
    <slot name="footer"></slot>
  </div>
</template>

<script>
/**
 * User Card Component
 *
 * Displays user information in a customizable card layout
 * with support for header and footer slots.
 */
export default {
  name: 'UserCard',

  props: {
    /**
     * User's full name
     */
    userName: {
      type: String,
      required: true
    },

    /**
     * Card display mode
     */
    mode: {
      type: String,
      default: 'standard',
      validator: value => ['compact', 'standard', 'full'].includes(value)
    }
  },

  /**
   * Emitted when the card is clicked
   * @event click:card
   * @property {Object} user - User data object
   */
  methods: {
    handleClick() {
      this.$emit('click:card', {
        name: this.userName,
        mode: this.mode
      })
    }
  }
}
</script>
```

### Completion Checklist

Before considering documentation complete:

1. [ ] All components are documented
2. [ ] Documentation is clear and helpful
3. [ ] Props have type definitions and descriptions
4. [ ] Events are documented with payload types
5. [ ] Slots are documented with usage examples
6. [ ] Methods have clear documentation
7. [ ] Component examples are provided
8. [ ] Vuex interactions are documented

Remember to integrate any existing documentation and ensure all documentation makes the components more maintainable and reusable.

Need help? Refer to the "Vue.js Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
