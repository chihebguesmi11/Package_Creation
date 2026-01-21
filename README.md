# Python Package Creation Tutorial

A comprehensive demonstration of modern Python package development, showcasing industry best practices from local development to production deployment.

## Overview

This project serves as a complete reference implementation for building professional Python packages. It demonstrates the entire development lifecycle including dependency management with Poetry, automated testing, code quality enforcement, documentation generation, and CI/CD pipelines.

While the package implements simple string manipulation utilities, its true value lies in demonstrating production-ready development workflows that can be applied to any Python project.

## Key Learning Outcomes

This project demonstrates:

- **Modern Dependency Management**: Using Poetry for reproducible builds and dependency resolution
- **Automated Testing**: Comprehensive test suite with pytest and coverage reporting
- **Code Quality Enforcement**: Pre-commit hooks with Ruff for consistent code style
- **Documentation**: Auto-generated documentation with Sphinx from docstrings
- **CI/CD Pipelines**: GitHub Actions for automated testing and documentation deployment
- **Package Publishing**: Complete workflow from development to PyPI publication

## Features

- String reversal
- Vowel counting in strings
- Word capitalization

## Installation

### From PyPI
```bash
pip install package-creation-tutorial
```

### From Source
```bash
git clone https://github.com/yourusername/package_creation_tutorial.git
cd package_creation_tutorial
poetry install
```

## Usage
```python
from package_creation_tutorial.string_ops import reverse_string, count_vowels, capitalize_words

text = "hello world"
print(reverse_string(text))      # "dlrow olleh"
print(count_vowels(text))         # 3
print(capitalize_words(text))     # "Hello World"
```

### Running the Demo
```bash
python main.py
```

## Development Setup

### Prerequisites

- Python 3.12.4 or higher
- Poetry for dependency management
- Git for version control

### Initial Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/package_creation_tutorial.git
cd package_creation_tutorial

# Install Poetry (if not already installed)
pipx install poetry

# Install dependencies
poetry install

# Activate virtual environment
poetry shell

# Install pre-commit hooks
pre-commit install
```

### Adding Dependencies
```bash
# Add a production dependency
poetry add package-name

# Add a development dependency
poetry add --group dev package-name
```

## Testing
```bash
# Run all tests
poetry run pytest

# Run tests with coverage report
poetry run pytest --cov src/

# Run tests with detailed output
poetry run pytest -v
```

## Code Quality

This project enforces code quality through automated tools:

### Ruff (Linting and Formatting)
```bash
# Check code
ruff check .

# Auto-fix issues
ruff check --fix .
```

### Pre-commit Hooks

Pre-commit hooks automatically run Ruff checks before each commit, ensuring code quality standards are maintained.
```bash
# Install hooks
pre-commit install

# Run manually on all files
pre-commit run --all-files
```

## Documentation

Documentation is automatically generated from docstrings using Sphinx with the Read the Docs theme.

### Building Documentation Locally
```bash
cd docs/
make html
```

Open `docs/build/html/index.html` in your browser to view the documentation.

### Online Documentation

Documentation is automatically deployed to GitHub Pages on every push to master: [View Documentation](https://yourusername.github.io/package_creation_tutorial/)

## Project Structure
```
package_creation_tutorial/
├── src/
│   └── package_creation_tutorial/
│       ├── __init__.py          # Package initialization
│       ├── string_ops.py        # Core string manipulation functions
│       └── main.py              # Demo script
├── tests/
│   └── test_string_ops.py       # Unit tests for string operations
├── docs/
│   ├── conf.py                  # Sphinx configuration
│   ├── index.rst                # Documentation home page
│   └── modules.rst              # API reference structure
├── .github/
│   └── workflows/
│       ├── tests.yaml           # CI pipeline for automated testing
│       └── sphinx_doc.yaml      # CI pipeline for documentation deployment
├── pyproject.toml               # Project metadata and dependencies
├── README.md                    # This file
└── .pre-commit-config.yaml      # Pre-commit hook configuration
```

## Continuous Integration

This project uses GitHub Actions for automated workflows:

### Automated Testing (`tests.yaml`)

Triggers on push and pull requests to master:
- Sets up Python environment
- Installs dependencies
- Runs pytest suite
- Reports test results

### Documentation Deployment (`sphinx_doc.yaml`)

Triggers on push to master:
- Builds Sphinx documentation
- Deploys to GitHub Pages via `gh-pages` branch
- Makes documentation accessible at the GitHub Pages URL

## Publishing to PyPI

This package is published to PyPI using Poetry:
```bash
# Build the package
poetry build

# Publish to PyPI (requires API token)
poetry publish
```

### Setting up PyPI Token
```bash
# Configure Poetry with your PyPI token
poetry config pypi-token.pypi <your-api-token>
```

## What Makes This Project Valuable

1. **Complete Workflow**: Covers the entire package lifecycle from setup to publication
2. **Best Practices**: Implements modern Python development standards
3. **Automation**: Demonstrates CI/CD pipelines for testing and documentation
4. **Reproducibility**: Uses Poetry for consistent dependency management
5. **Code Quality**: Enforces standards through automated tools and pre-commit hooks
6. **Documentation**: Shows how to create professional, auto-generated documentation
7. **Real Example**: Provides a working template that can be adapted for any project

## Links

- **PyPI Package**: [https://pypi.org/project/package-chiheb-creation-tutorial/](https://pypi.org/project/package-chiheb-creation-tutorial/)
- **Documentation**: [https://chihebguesmi11.github.io/Package_Creation/](https://chihebguesmi11.github.io/Package_Creation/)
## Resources

- [Poetry Documentation](https://python-poetry.org/docs/)
- [Pytest Documentation](https://docs.pytest.org/)
- [Ruff Documentation](https://docs.astral.sh/ruff/)
- [Sphinx Documentation](https://www.sphinx-doc.org/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

## License

MIT License

## Author

Your Name

## Acknowledgments

Created as part of the Hi! PARIS Summer School 2024 - Python Package Creation Tutorial
