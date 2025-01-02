Hi Devin! This playbook will guide you through Phase 2 of documenting Python code, focusing specifically on method documentation.

### Prerequisites
- Completed Phase 1 (Module/Class Documentation)
- Access to the target Python project folder
- Knowledge of Python documentation standards
- Understanding of PEP 257

### Instructions

1. **Initial Setup**
   - Ensure Phase 1 documentation is complete and approved
   - Review the list of modules/classes from Phase 1

2. **Method Documentation Process**
   For each method:

   ```python
   def method_name(param1: Type1, param2: Type2) -> ReturnType:
       """
       [Brief method description]

       Detailed explanation of what the method does, focusing on behavior
       rather than implementation details.

       Args:
           param1: Description of first parameter
           param2: Description of second parameter

       Returns:
           Description of return value

       Raises:
           ErrorType: Description of when this error occurs

       Example:
           Basic usage example (if helpful for understanding)
       """
       # Implementation
   ```

3. **Phase 2 Documentation Checklist**
   For each method:
   - [ ] Clear, concise description of purpose
   - [ ] All parameters documented with types and descriptions
   - [ ] Return value documented with type and description
   - [ ] Exceptions/errors documented if applicable
   - [ ] Complex logic or algorithms explained
   - [ ] Side effects documented (if any)
   - [ ] Type hints included (PEP 484)

4. **Example Documentation**
   ```python
   from typing import Dict, Optional
   from datetime import datetime

   def update_user_profile(
       user_id: int,
       profile_data: Dict[str, str],
       notify: bool = True
   ) -> Optional[Dict[str, str]]:
       """
       Update a user's profile information in the database.

       Validates the provided profile data, updates the user's information
       in the database, and optionally sends notifications to relevant
       services about the change.

       Args:
           user_id: The unique identifier of the user
           profile_data: Dictionary containing the new profile information
               Must include 'name' and 'email' keys
           notify: Whether to send notifications about the update

       Returns:
           Updated user profile dictionary if successful, None if user
           not found

       Raises:
           ValidationError: If profile_data is missing required fields
           DatabaseError: If database update fails
           NotificationError: If notify=True and notification fails
       """
       # Implementation details
   ```

5. **Validation**
   - Review each documented method
   - Ensure documentation is clear and helpful
   - Verify all checklist items are complete
   - Get approval before proceeding to Phase 3

Remember:
- Focus only on method documentation in this phase
- Variables and attributes will be documented in Phase 3
- Get approval before proceeding to the next phase

Need help? Refer to the "Python Code Documentation KB" in your knowledge base for detailed guidelines and best practices.
