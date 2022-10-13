# poetry-aliases-plugin

Poetry plugin to run commands through aliases

## Quick start

```bash
poetry self add poetry-aliases-plugin
poetry l this # ==> poetry run python -m this
```

## Dependencies

```toml
[tool.poetry.dependencies]
python = "^3.10"
poetry = ">=1.2.0"
```

PS. Adaptation for earlier versions of python will someday appear

## Install

```bash
poetry self add poetry-aliases-plugin

# uninstall: poetry self remove poetry-aliases-plugin
# but updated: rm -r ~/.cache/pypoetry/{artifacts,cache} && poetry self update poetry-aliases-plugin
```

## Setup

On `0.N.N` version setup only in `pyproject.toml`:

```toml
[tool.aliases] # config dict, where key - alias ; value - full command / commands with "&&"
alias = "full command / commands with '&&'"
tests = "poetry run pytest"
runserver = "poetry run python manage.py runserver"
```

## Use

plugin command - "l"

```bash
poetry l --help
poetry l tests # ==> poetry run pytest
poetry l runserver # ==> poetry run python manage.py runserver
```
