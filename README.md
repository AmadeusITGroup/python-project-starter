# python-project-starter

This is a template repo to act as a reference when starting up a new project in python. It consolidates best practices in regards to minimal level of documentation as well as the CI aspects.

Local installation can be done using [`uv`](https://github.com/astral-sh/uv):

```bash
$ uv venv -p python3.10
$ uv pip install -e .
$ source .venv/bin/activate
$ python
>>> from package import square
>>> square(3)
9
```

After installation a command-line tool is also available:

```bash
$ square 4
Square of 4 is 16
```

Running the tests can be done using [`tox`](https://tox.wiki/):

```bash
$ tox -p
```

Building the packages can also be done using `tox`:

```bash
$ tox -e packages
$ ls dist/
```

Packaging uses [`setuptools-scm`](https://github.com/pypa/setuptools-scm), so the version of the software is based on git tags.

To run the linting, we recommend `ruff`, a standard configuration is in the repo in `pyproject.toml`.

# Releasing
To release a new version of the package, you can create a pre-release from the main branch using GitHub UI, which will then trigger the release workflow. Alternatively, you can use the `gh` command line tool to create a release:

```bash
gh release create v[a.b.c] --prerelease --title "Kick starting the release"  --target main
```


# Contributing
We welcome contributions to this project! If you have an idea for a new feature, bug fix, or improvement, please open an issue or submit a pull request. Before contributing, please read our [contributing guidelines](./CONTRIBUTING.md).