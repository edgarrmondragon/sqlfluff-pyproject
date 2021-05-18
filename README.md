# sqlfluff-pyproject

Example SQLFluff project using pyproject.toml for config.

## Installation

```shell
poetry install
```

## Execution

```shell
poetry run sqlfluff lint
```

If `pyproject.toml` is correctly being used for configuration, you should get the following error message:

```
== [/home/edgarrmondragon/code/sqlfluff-example/example.sql] FAIL
L:   2 | P:   5 | L003 | Line over-indented compared to line #1
L:   2 | P:  12 | L019 | Found trailing comma. Expected only leading.
L:   3 | P:   5 | L003 | Line over-indented compared to line #1
```

## Configuration

### `.sqlfluff`

```ini
[sqlfluff]
dialect = ansi

[sqlfluff:rules]
comma_style = trailing
```

### `pyproject.toml`

```toml
[tool.sqlfluff.rules]
tab_space_size = 2
comma_style = "leading"
```
