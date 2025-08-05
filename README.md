# Python Project Template

A modern, minimal Cookiecutter template to kickstart your Python projects. It comes preconfigured with `uv` and includes all the essential tools for seamless development, testing, and code quality checks.

## Features

- Fast and modern dependency management with **[uv](https://docs.astral.sh/uv/)**.  
- Automated linting, formatting, docstring checks, typo detection, secret scanning, and static analysis via **[pre-commit](https://pre-commit.com/)**.  
- Code quality checks with **[ruff](https://docs.astral.sh/ruff/)** and type safety with **[mypy](https://mypy-lang.org/)**.  
- Parallel test execution and coverage reporting using **[pytest](https://docs.pytest.org/)**.  
- Built-in config and logging setup in `src/config/` using **[pydantic](https://docs.pydantic.dev/)** and **[loguru](https://loguru.readthedocs.io/)**.  
- Example I/O base classes in `src/io/base.py` to promote clean, extensible design.  
- CI/CD workflows powered by **[GitHub Actions](https://docs.github.com/en/actions)**.  
- Preconfigured **Dockerfile** for containerization and deployment.

## Prerequisites

Before using this template, make sure you have the following installed:

- [Cookiecutter](https://cookiecutter.readthedocs.io/en/2.0.2/). Install it using:

    ```bash
    pip install cookiecutter
    ```

- [uv](https://docs.astral.sh/uv/) (check [this link](https://docs.astral.sh/uv/getting-started/installation/) for more details).

## Installation

1. Create the Python project:

    ```bash
    cookiecutter git@github.com:miguelmendesduarte/cookiecutter-python-template.git
    ```

2. Enter project details as prompted (example):

    ```bash
    [1/4] project_name (My Project): my-project-test
    [2/4] project_description (A brief description of the project): This is just a test project.
    [3/4] author_name (Your Name): Miguel Duarte
    [4/4] author_email (): miguel@gmail.com
    ```

    ⚠️ **Note**: The project name should use dashes (`-`) instead of spaces.

3. Navigate to the project folder (replace `<your-project-folder>` with the actual folder name you provided in **Step 2**):

    ```bash
    cd <your-project-folder>
    ```

4. Install all dependencies using **uv**:

    ```bash
    uv sync --all-extras
    ```

5. (Optional) Install `pre-commit`.

    ```bash
    pre-commit install
    ```

## Usage

Once your project is set up, you can start coding right away! The following commands are available to help with common tasks:

### Initialize a Github Repository (Optional)

If you want to create a GitHub repository for your project, follow these steps:

1. Initialize a git repository:

    ```bash
    git init
    ```

2. Add your remote repository (replace with your own GitHub repo URL):

    ```bash
    git remote add origin git@github.com:yourusername/your-repo-name.git
    ```

3. Add and commit your files:

    ```bash
    git add .
    git commit -m "Initial commit"
    ```

4. Push to GitHub:

    ```bash
    git push -u origin main
    ```

### Running Tests

To run tests with coverage (using auto parallelism):

```bash
make test
```

### Static Checks & Fixes

To check and automatically fix code style, formatting, and types:

```bash
make static-fix
```

### Environment Variables

If needed, create your `.env` file by copying the example:

```bash
cp .env.example .env
```

## 🚀 Contributing

Feel free to open a pull request, create an issue, or send an email if you have any feature requests, improvements, or questions!
