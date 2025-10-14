# Contributing to AbsyssLab VTOM Connectors

[🇫🇷 Version française](CONTRIBUTING.fr.md)

Thank you for considering contributing to AbsyssLab VTOM connectors! 🎉

We welcome contributions from the community and are pleased to have you join us.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Testing](#testing)
- [Documentation](#documentation)

## 📜 Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## 🤝 How Can I Contribute?

### Reporting Bugs 🐛

- Use the [Bug Report template](https://github.com/AbsyssLab/.github/issues/new?template=bug_report.yml)
- Check if the bug has already been reported
- Include detailed steps to reproduce
- Provide logs and error messages
- Specify your environment (VTOM version, OS, etc.)

### Suggesting Features ✨

- Use the [Feature Request template](https://github.com/AbsyssLab/.github/issues/new?template=feature_request.yml)
- Clearly describe the feature and its benefits
- Provide use cases and examples
- Explain why this feature would be useful to most users

### Proposing New Connectors 🔌

- Use the [Connector Request template](https://github.com/AbsyssLab/.github/issues/new?template=connector_request.yml)
- Describe the tool/platform to integrate
- Explain the use cases
- Provide information about available APIs
- Indicate if you're willing to contribute to development

### Contributing Code 💻

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit following our guidelines
5. Push to your fork
6. Open a Pull Request

## 🛠️ Development Setup

### Prerequisites

- Python 3.8 or higher
- Visual TOM 6.x installed (for testing)
- Git
- Docker (optional, for containerized testing)

### Local Setup

```bash
# Clone the repository
git clone https://github.com/AbsyssLab/<connector-name>.git
cd <connector-name>

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt  # If available

# Run tests
pytest tests/
```

## 📝 Coding Standards

### Python Style Guide

We follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) with some specific rules:

- **Line length**: Maximum 120 characters
- **Indentation**: 4 spaces (no tabs)
- **Quotes**: Use double quotes for strings
- **Naming**:
  - `snake_case` for functions and variables
  - `PascalCase` for classes
  - `UPPER_CASE` for constants

### Code Quality Tools

```bash
# Format code
black .

# Lint code
flake8 .
pylint **/*.py

# Type checking
mypy .

# Security checks
bandit -r .
```

### Documentation

- Add docstrings to all functions and classes (Google style)
- Comment complex logic
- Update README.md if adding new features
- Keep comments concise and meaningful

Example:
```python
def execute_job(job_name: str, parameters: dict) -> dict:
    """
    Execute a VTOM job with specified parameters.
    
    Args:
        job_name: Name of the job to execute
        parameters: Dictionary of job parameters
        
    Returns:
        Dictionary containing execution status and logs
        
    Raises:
        ConnectionError: If unable to connect to VTOM
        JobExecutionError: If job execution fails
    """
    # Implementation
    pass
```

## 📝 Commit Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

### Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks
- `ci`: CI/CD changes

### Examples

```bash
feat(azure): add support for managed identities

Implement authentication using Azure managed identities
for more secure credential management.

Closes #123

fix(jenkins): handle connection timeout properly

Add retry logic with exponential backoff when Jenkins
API is temporarily unavailable.

Fixes #456

docs: update installation instructions

Add troubleshooting section for common issues.
```

## 🔄 Pull Request Process

1. **Update documentation** - Ensure README, CHANGELOG, and relevant docs are updated
2. **Add tests** - All new features must include tests
3. **Pass CI checks** - All automated checks must pass
4. **Request review** - At least one maintainer review is required
5. **Update changelog** - Add your changes to CHANGELOG.md (if present)
6. **Squash commits** - Consider squashing commits before merge

### Pull Request Checklist

- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex code
- [ ] Documentation updated
- [ ] Tests added and passing
- [ ] No new warnings introduced
- [ ] Sensitive information removed (passwords, tokens, etc.)

## 🧪 Testing

### Running Tests

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=. --cov-report=html

# Run specific test file
pytest tests/test_connector.py

# Run with verbose output
pytest -v
```

### Writing Tests

- Place tests in the `tests/` directory
- Use descriptive test names: `test_should_connect_successfully_with_valid_credentials`
- Test both success and failure scenarios
- Mock external API calls
- Aim for >80% code coverage

Example:
```python
import pytest
from unittest.mock import Mock, patch

def test_should_execute_job_successfully():
    """Test successful job execution."""
    # Arrange
    connector = VTOMConnector(host="localhost")
    
    # Act
    result = connector.execute_job("test_job", {"param": "value"})
    
    # Assert
    assert result["status"] == "success"
    assert "job_id" in result
```

## 📚 Documentation

### README Structure

All connector READMEs should include:

1. **Description** - What the connector does
2. **Prerequisites** - Requirements and dependencies
3. **Installation** - Step-by-step setup
4. **Configuration** - All configuration options
5. **Usage** - Examples and use cases
6. **Troubleshooting** - Common issues and solutions
7. **Contributing** - Link to this guide
8. **License** - Apache License 2.0

### Code Comments

- Write self-documenting code when possible
- Add comments for non-obvious logic
- Keep comments up-to-date with code changes
- Avoid redundant comments

## 🏷️ Versioning

We use [Semantic Versioning](https://semver.org/):

- **MAJOR**: Breaking changes
- **MINOR**: New features (backward compatible)
- **PATCH**: Bug fixes (backward compatible)

Example: `v1.2.3`

## 📞 Getting Help

- 📖 Read the [Support Guide](SUPPORT.md)
- 💬 Join [Discussions](https://github.com/orgs/AbsyssLab/discussions)
- 🐛 Report issues using issue templates
- 📧 Contact maintainers for sensitive topics

## 🎯 Good First Issues

Looking for a place to start? Check issues labeled:

- `good first issue` - Perfect for newcomers
- `help wanted` - We need community help
- `documentation` - Improve our docs

## 🌟 Recognition

Contributors will be:

- Listed in CONTRIBUTORS.md (if present)
- Mentioned in release notes
- Credited in commit history

## 📄 License

By contributing, you agree that your contributions will be licensed under the Apache License 2.0.

---

**Thank you for contributing to AbsyssLab! 🙏**

<div align="center">
  <sub>Together, we're making VTOM integrations better for everyone</sub>
</div>

