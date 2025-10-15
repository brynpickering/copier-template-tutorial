# Copier Template for Python Projects

A comprehensive [Copier](https://copier.readthedocs.io/) template for creating Python projects with modern development tools and best practices.

## Features

This template generates a Python project with:

### Project Structure
- 📦 **Package Management**: Uses `pyproject.toml` for dependency management
- 🗂️ **Source Layout**: Standard `src/` layout with proper package structure
- 🧪 **Testing**: Pre-configured pytest with coverage reporting
- 📝 **Documentation**: MkDocs with Material theme for beautiful docs

### Development Tools
- ✅ **Pre-commit Hooks**: Automated code quality checks
- 🎨 **Code Formatting**: Ruff for fast linting and formatting
- 🔤 **Spell Checking**: Codespell for catching typos
- ⚙️ **Editor Config**: Consistent coding styles across editors

### CLI & Features
- 🖥️ **Command Line Interface**: Click-based CLI with example commands
- 📄 **License Management**: REUSE-compliant licensing
- 📋 **Changelog**: Keep a Changelog format
- 🤝 **Contributing Guide**: Clear contribution guidelines

### Automation
- 🔄 **CI/CD**: GitHub Actions workflows for testing and linting
- 🌐 **Multi-platform**: Tests on Linux, macOS, and Windows
- 🐍 **Multi-version**: Supports multiple Python versions

## Prerequisites

- [Copier](https://copier.readthedocs.io/) (>= 9.0.0)
- Python (>= 3.9)

Install Copier:

```bash
pip install copier
```

Or using [pixi](https://pixi.sh):

```bash
pixi global install copier
```

## Usage

Generate a new Python project from this template:

```bash
copier copy gh:brynpickering/copier-template-tutorial /path/to/your-new-project
```

You'll be prompted for:
- Project name
- Project description
- Module name (defaults to snake_case version of project name)
- Author information
- GitHub username
- License choice
- Python version

### Example

```bash
$ copier copy gh:brynpickering/copier-template-tutorial my-awesome-project

🎤 What is your project name?
   my-awesome-project
🎤 A short description of your project
   A Python project that does awesome things
🎤 What is the Python module name (snake_case)?
   my_awesome_project
🎤 What is your name?
   John Doe
🎤 What is your email?
   john@example.com
🎤 What is your GitHub username?
   johndoe
🎤 Which license do you want to use?
   MIT
🎤 Minimum Python version
   3.9
```

## Generated Project Structure

```
your-project/
├── src/
│   └── your_module/
│       ├── __init__.py
│       └── cli.py
├── tests/
│   ├── __init__.py
│   └── test_cli.py
├── docs/
│   ├── index.md
│   ├── getting-started.md
│   ├── api.md
│   ├── contributing.md
│   └── changelog.md
├── .github/
│   └── workflows/
│       └── ci.yml
├── .reuse/
│   └── dep5
├── .editorconfig
├── .gitignore
├── .pre-commit-config.yaml
├── CHANGELOG.md
├── CONTRIBUTING.md
├── mkdocs.yml
├── pyproject.toml
└── README.md
```

## Development

This template repository uses [pixi](https://pixi.sh) for development.

### Setup

```bash
# Install pixi (if not already installed)
curl -fsSL https://pixi.sh/install.sh | bash

# Install dependencies
pixi install

# Install pre-commit hooks
pixi run pre-commit install
```

### Testing the Template

Generate a test project:

```bash
pixi run test-template <path-to-directory>
```

Where `<path-to-directory>` is defined by you, e.g. as a temporary directory `/tmp/test-project`

### Linting and Formatting

```bash
# Run linter
pixi run lint

# Format code
pixi run format

# Check formatting
pixi run format-check
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a history of changes to this template.

## License

This template is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Projects generated from this template can use any license chosen during generation.
