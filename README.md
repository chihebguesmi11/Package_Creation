# Package_Creation

A complete example of how to **build, test, document, and publish a Python package** using modern best practices.

This project was developed as part of the **Hi! PARIS – Python Package practical session**, and demonstrates the full lifecycle of a Python package: from local development to CI/CD and PyPI publication.

---

##  Features

- Python package built with **Poetry**
- Clean **src/ layout**
- Fully typed functions with **docstrings**
- Unit tests with **pytest**
- Test coverage with **pytest-cov**
- Linting & formatting with **Ruff**
- Automated checks with **pre-commit**
- Documentation generated with **Sphinx**
- CI pipelines using **GitHub Actions**
- Package published on **PyPI**

---

# Project Structure

```text
.
├── src/
│   └── package_creation_tutorial/
│       ├── __init__.py
│       ├── string_ops.py
│       └── main.py
├── tests/
│   └── test_string_ops.py
├── docs/
│   ├── conf.py
│   ├── index.rst
│   └── modules.rst
├── .github/
│   └── workflows/
│       ├── tests.yaml
│       └── sphinx_doc.yaml
├── pyproject.toml
├── README.md
└── .pre-commit-config.yaml
