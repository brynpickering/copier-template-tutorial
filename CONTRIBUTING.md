# Contributing to copier-template-tutorial

Thank you for considering contributing to this Copier template! We appreciate your time and effort.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/brynpickering/copier-template-tutorial.git`
3. Create a new branch: `git checkout -b feature/your-feature-name`

## Development Setup

This project uses [pixi](https://pixi.sh) for dependency management. Install pixi following the [official instructions](https://pixi.sh/latest/).

Install dependencies:

```bash
pixi install
```

## Working with the Template

### Testing the Template

Generate a test project from the template:

```bash
pixi run test-template
```

This will create a test project in `/tmp/test-project`.

### Template Structure

```
copier-template-tutorial/
├── copier.yml              # Template configuration
├── template/               # Template files
│   ├── src/
│   ├── docs/
│   ├── tests/
│   ├── .github/
│   └── ...
├── pixi.toml              # Project dependencies
└── README.md
```

## Making Changes

1. Make your changes in your feature branch
2. Test the template by generating a project
3. Verify the generated project works correctly
4. Run the linter: `pixi run lint`
5. Format your code: `pixi run format`
6. Commit your changes with a descriptive message

## Pull Request Process

1. Update the CHANGELOG.md with details of your changes
2. Ensure the template generates working projects
3. Push your branch to your fork
4. Submit a pull request to the main repository
5. Wait for review and address any feedback

## Code Style

This project uses:
- [Ruff](https://github.com/astral-sh/ruff) for linting and formatting
- [Pre-commit](https://pre-commit.com/) for automated checks

## Template Guidelines

When adding or modifying template files:
- Use Jinja2 templating syntax for dynamic content
- Keep templates minimal and focused
- Document any new template variables in copier.yml
- Ensure generated projects follow Python best practices
- Test with different template variable combinations

## Questions?

Feel free to open an issue if you have any questions or need clarification.
