### PHP Code Documentation Playbook

Devin, add this to your knowledge base for future reference.

#### General Principles
- Documentation should serve both current and future developers, making the code easier to maintain and use.
- Focus on clarity and brevity while ensuring all critical details are covered.

#### Documentation Steps
1. **Prepare a Class List**  
   - List all non-test classes requiring documentation in the target repository.
   
2. **Class-Level Documentation**  
   - Add docblocks at the class level, including a summary and description.  
     - Avoid prefixes like "Description:" or "Summary:" in these docblocks.  

3. **Method Documentation**  
   - Use `@inheritdoc` for methods where applicable to inherit documentation.  

4. **Property Documentation**  
   - Document class variables with `@inheritdoc` when inherited.  
   - Add succinct docblocks for non-inherited properties.  
   - Use `@property` tags to document magic properties.

5. **Avoid `@see` Tags**  
   - `@see` tags are difficult to keep current and should be omitted.

6. **Merge Existing Documentation**  
   - Integrate any existing documentation, retaining important details like caveats or TODOs.

7. **Validation**  
   - Validate each file to ensure it meets the documentation requirements.  
   - Ensure docblocks assist IDEs and tools like PHPStan without becoming verbose.

8. **CI Compliance**  
   - Verify all changes pass CI checks.

---

#### Directory-Wide Documentation Process
When working through a directory of classes:

1. **Inventory All Files**  
   - List all files and classes in the target directory before starting.

2. **Create a Documentation Plan**  
   - Develop a plan that includes every file and class identified.

3. **Track Progress**  
   - Mark each file as complete after updating its documentation.

4. **Ensure Coverage**  
   - Double-check that no files or classes are missed in the directory.

---

By following this playbook, you'll ensure thorough and consistent documentation across the codebase, making it easier for developers to understand and maintain.
