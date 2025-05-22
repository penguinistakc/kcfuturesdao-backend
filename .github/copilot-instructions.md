# Operator Interaction

- When asked to fix code, first explain the problems found.
- When asked to generate tests, first explain what tests will be created.
- When making multiple changes, provide a step-by-step overview first.

## Security

- Check the code for vulnerabilities after generating.
- Avoid hardcoding sensitive information like credentials or API keys.
- Use secure coding practices and validate all inputs.

## Environment Variables

- If a .env file exists, use it for local environment variables
- Document any new environment variables in README.md
- Provide example values in .env.example

## Version Control

- Keep commits atomic and focused on single changes
- Follow conventional commit message format
- Update .gitignore for new build artifacts or dependencies

## Code Style

- Follow existing project code style and conventions
- Add type hints and docstrings for all new functions
- Include comments for complex logic

## Change Logging

- Each time you generate code, note the changes in changelog.md
- Follow semantic versioning guidelines
- Include date and description of changes

## Testing Requirements

- Include unit tests for new functionality
- Maintain minimum 80% code coverage
- Add integration tests for API endpoints

## For Python Projects Only

- Always use a Python3 virtual environment: if no venv exists, create one and activate
- Use uv package and project manager
  - All dependencies should be placed in appropriate sections of pyproject.toml in the project root
- Always create a requirements.txt file using uv:

```bash
uv pip compile -o requirements.txt
```

- Follow PEP 8 style guidelines
- Include type hints (PEP 484)
- Use pytest for unit tests
- If a .python-version file exists in the project root, use it to set the Python version. If it does not exist, use the version specificed in pyproject.toml. If that does not exist, use the latest stable version of Python 3.
- use `ruff` for linting and code formatting
