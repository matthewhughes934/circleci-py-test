# CircleCI Python Test

A quick demonstrating the difference when using `pip` and `poetry` with the
`circleci/python@2.0.3` orb.

This package checks its own metadata in order to set its version and so must be
installed. For the sake of testing this package can be built by both `poetry`
and `pip/setuptools`.

## Testing Poetry

```console
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install poetry
$ poetry install
$ pytest
```

## Testing pip/setuptools

```console
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install --requirement requirements-dev.txt .
$ pytest
