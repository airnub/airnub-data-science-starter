# Airnub Data Science Starter

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![Code style: ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![Tests: pytest](https://img.shields.io/badge/tested_with-pytest-007ec6.svg)](https://pytest.org)

Standard starter template for Data Science projects at Airnub Technologies.


**Note:** This repository is configured as a GitHub template. You can use the "Use this template" button on the repository page to generate a new project with this structure.

## Goal

This template provides a standardized, best-practice foundation for initiating Data Science projects at Airnub. It aims to accelerate development by providing a consistent structure, pre-configured tooling for environment management, linting, formatting, testing, and documentation, enabling developers to focus quickly on the core data science tasks.

## Project Organization

```
├── LICENSE            <- MIT License file.
├── Makefile           <- Makefile with convenience commands like `make requirements`, `make data`, `make test`.
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project for documentation.
│   ├── mkdocs.yml     <- MkDocs configuration file.
│   └── docs/          <- Documentation source files (Markdown).
│
├── models             <- Trained and serialized models, model predictions, or model summaries.
│
├── notebooks          <- Jupyter notebooks. Naming convention: number-initials-description.
│                         e.g., `1.0-jqp-initial-data-exploration.ipynb`.
│
├── pyproject.toml     <- Project configuration file:
│                         - Defines dependencies (for `uv sync`).
│                         - Configures tools like Ruff.
│                         - Specifies build system (flit) and package metadata.
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting.
│
├── tests              <- Unit and integration tests (using pytest).
│   └── test_data.py   <- Example test file.
│
└── airnub_data_science_starter/ <- Source code for use in this project (Python package).
    │
    ├── __init__.py    <- Makes this directory a Python package.
    │
    ├── config.py      <- Stores configuration variables.
    │
    ├── dataset.py     <- Scripts to download or generate data (e.g., via `make data`).
    │
    ├── features.py    <- Code to create features for modeling.
    │
    ├── modeling/
    │   ├── __init__.py
    │   ├── predict.py <- Code to run model inference.
    │   └── train.py   <- Code to train models.
    │
    └── plots.py       <- Code to create visualizations.

```

## Getting Started

### Prerequisites

* Python `~=3.12.0` (as specified in `pyproject.toml`)
* [uv](https://github.com/astral-sh/uv) (for environment management and package installation)
* `make` (for using the Makefile commands)

### Setup

1.  **Create Project from Template or Clone:**
    * **Option A (Recommended):** Click the "Use this template" button on the GitHub repository page to create a new repository based on this starter.
    * **Option B (Manual Clone):**
        ```bash
        git clone <your-repo-url> airnub-data-science-starter
        cd airnub-data-science-starter
        ```
2.  **Create Virtual Environment:** Use `make` to create a virtual environment using the specified Python version.
    ```bash
    make create_environment
    ```
3.  **Activate Environment:** Follow the instructions printed by the command above:
    ```bash
    # Example for macOS/Linux:
    source .venv/bin/activate

    # Example for Windows PowerShell:
    # .\.venv\Scripts\Activate.ps1

    # Example for Windows CMD:
    # .\.venv\Scripts\activate
    ```
4.  **Install Dependencies:** Use `make` to install dependencies listed in `pyproject.toml` using `uv`.
    ```bash
    make requirements
    ```

## Usage

This project uses a `Makefile` for common development commands. Run `make help` to see available commands and their descriptions.

* **Install/Update Dependencies:** `make requirements` (uses `uv sync`)
* **Lint Code:** `make lint` (checks formatting and finds issues with Ruff)
* **Format Code:** `make format` (applies formatting and fixes with Ruff)
* **Run Tests:** `make test` (uses `pytest`)
* **Generate Dataset:** `make data` (runs the script defined in `airnub_data_science_starter/dataset.py`)
* **Clean Compiled Files:** `make clean` (removes `*.pyc`, `*.pyo`, `__pycache__`)

## Core Dependencies

The following libraries are installed by default (via `pyproject.toml` and `make requirements`):

### Core Tools & Libraries

These libraries provide essential tooling for development, testing, documentation, and utilities.

* **loguru**: Opinionated logging library for simpler and more powerful logging.
* **mkdocs**: Static site generator for building project documentation from Markdown.
* **pytest**: Framework for writing and running tests.
* **ruff**: Extremely fast Python linter and code formatter.

### PyData Packages (Basic Set)

These libraries form the core of the scientific Python stack.

* **ipython**: Enhanced interactive Python shell, useful for debugging and exploration.
* **jupyterlab**: Web-based interactive development environment for notebooks, code, and data.
* **matplotlib**: Foundational library for creating static, animated, and interactive visualizations.
* **notebook**: Core package providing the Jupyter Notebook format and interface (dependency for JupyterLab).
* **numpy**: Fundamental package for numerical computing with N-dimensional arrays.
* **pandas**: Powerful library for data manipulation and analysis (DataFrames).
* **scikit-learn**: Comprehensive library for machine learning tasks (classification, regression, clustering, model selection, etc.).

## Linting & Formatting

* This project uses [Ruff](https://github.com/astral-sh/ruff) for extremely fast linting, formatting (compatible with Black), and import sorting (compatible with isort).
* Configuration is in the `[tool.ruff]` section of `pyproject.toml`.
* Check code with `make lint`.
* Format code automatically with `make format`.

## Testing

* Tests are located in the `tests/` directory and use [pytest](https://docs.pytest.org/).
* Run tests with `make test`.
* Add new tests for your code modules within the `tests/` directory.

## Documentation

* This project uses [MkDocs](https://www.mkdocs.org/) for documentation.
* Source files are in `docs/docs/`.
* Configuration is in `docs/mkdocs.yml`.
* **Build Docs:** `mkdocs build` (generates HTML site in `site/`)
* **Serve Docs Locally:** `mkdocs serve` (starts a local server, usually at `http://127.0.0.1:8000`)

## Support & Issues

If you encounter any bugs or have suggestions for improving the template, please open an issue on the [GitHub repository issue tracker](<https://github.com/airnub/airnub-data-science-starter/issues>).

## License

This project template is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

