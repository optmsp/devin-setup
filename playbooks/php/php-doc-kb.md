### PHP Code Documentation KB

Devin, add this to your knowledge base for future reference. File it as "PHP Code Documentation KB" to make it easy to reference.

#### General Principles

-   Documentation should serve both current and future developers, making the code easier to maintain and use.
-   Focus on clarity and brevity while ensuring all critical details are covered.

#### Documentation Steps

1. **Prepare a Class List**

    - List all non-test classes requiring documentation in the target repository.

2. **Class-Level Documentation**

    - Add docblocks at the class level, including a summary and description.
        - Avoid prefixes like "Description:" or "Summary:" in these docblocks.

3. **Method Documentation**

    - Document all methods with clear docblocks
    - Use `@inheritdoc` for inherited methods to avoid duplicating tags from parent classes
    - For overridden methods, document the changes/additions while using `@inheritdoc` for unchanged aspects
    - Keep method documentation clear and focused on implementation details

4. **Property Documentation**

    - Document all class properties with clear docblocks
    - Use `@inheritdoc` for inherited properties to avoid duplicating tags from parent classes
    - Keep property documentation succinct and focused on purpose
    - Document magic properties in the class docblock

5. **Documentation Tags**

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
