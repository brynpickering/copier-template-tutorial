# Copier Template Tutorial - simple example

A simple [Copier](https://copier.readthedocs.io/) template for learning the templating ropes.

## Setting up

Clone this repository, then install [copier](https://copier.readthedocs.io/en/stable/) however you like.
I recommend using [pixi](https://pixi.sh/latest/installation/):

```bash
pixi global install copier
```

## Usage

You can either generate your templated project from your [local repository clone](#local-usage) or [directly from the remote repository](#direct-github-usage).

### Local usage

To generate a new project from a local clone of this template:

```bash
cd /path/to/your-cloned-template-repository
copier copy --vcs-ref simple-template . build
```

You will then find your built project inside the `build` directory.

>[!WARNING]
>Copier isn't really designed to work with _local_ templates.
>You can only reliably build projects in the same directory as the cloned repository.
>When not testing, for greater flexibility and long-term maintainability, you should generate directly from the remote repository.

### Direct GitHub usage

To generate a new project from the remote repository of this template:

```bash
copier copy gh:brynpickering/copier-template-tutorial --vcs-ref simple-template /path/to/your-project-destination
```

## Updating your project

You can keep your project up-to-date with any changes made in the template, just call:

```bash
copier update --vcs-ref simple-template build
```

>[!NOTE]
>This will update to the latest HEAD commit on the.
>To only update if there has been a _tagged release_, remove `--vcs-ref HEAD` from your call.

## Development

This template repository uses [pixi](https://pixi.sh) for development.

### Setup

```bash
# Install pixi (if not already installed)
curl -fsSL https://pixi.sh/install.sh | bash

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

Pre-commit includes linting and formatting hooks.
You can therefore use it directly to check for errors:

```bash
pixi run pre-commit --all-files
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a history of changes to this template.

## License

This template is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Projects generated from this template can use any license chosen during generation.
