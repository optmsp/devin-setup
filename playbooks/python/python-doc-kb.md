### Python Code Documentation KB

Devin, add this to your knowledge base for future reference. File it as "Python Code Documentation KB" to make it easy to reference.

#### General Principles

- Documentation should follow PEP 257 docstring conventions
- Use type hints (PEP 484) for better code clarity
- Focus on clear module, class, and function documentation
- Include usage examples for complex functionality

#### Documentation Steps

1. **Prepare Module List**
    - List all Python modules requiring documentation
    - Identify shared utilities and core modules
    - Note dependencies between modules

2. **Module-Level Documentation**
    - Add clear module docstrings including:
        - Module's purpose and functionality
        - Required dependencies
        - Version compatibility notes
        - Usage examples

3. **Class Documentation**
    - Document all classes with:
        - Class purpose and behavior
        - Constructor parameters
        - Class attributes
        - Method overview
        - Usage examples
    - Use `@inheritdoc` for inherited class documentation to avoid duplicating docstrings

4. **Method Documentation**
    - Document all methods with clear docstrings
    - Use `@inheritdoc` for inherited methods to avoid duplicating docstrings
    - For overridden methods, document changes while using `@inheritdoc` for unchanged aspects
    - Include:
        - Purpose and functionality
        - Parameters with type hints
        - Return value types
        - Exceptions
        - Usage examples

5. **Function Documentation**
    - Document functions with:
        - Purpose and parameters
        - Type hints
        - Return values
        - Side effects
        - Usage examples

6. **Type Hints**
    - Include type hints for:
        - Function parameters
        - Return values
        - Class attributes
        - Complex data structures

7. **Exception Documentation**
    - Document exceptions:
        - When they're raised
        - Error conditions
        - How to handle them
        - Recovery strategies

8. **Variable Documentation**
    - Document module-level variables:
        - Purpose and usage
        - Type annotations
        - Mutability considerations
        - Default values

---

#### Directory-Wide Documentation Process

When documenting a Python project:

1. **Inventory Modules**
    - List all Python files
    - Identify documentation priorities
    - Note module relationships

2. **Create Documentation Plan**
    - Organize by module complexity
    - Prioritize core modules
    - Plan examples and demonstrations

3. **Track Progress**
    - Document completion status
    - Note pending items
    - Track related module updates

4. **Ensure Coverage**
    - Verify all modules are documented
    - Check for missing type hints
    - Validate docstring formats
