# AGENTS.md

First: This project expects the working root to be github repo `lgc-NB2Dev/workspace` because some recommended workspace-level files is not stored in this plugin project. If you are not working from that root, stop and notify the user.

## Commands

NOTE: The following command are expected to be run under the plugin repo root rather than the workspace root.

```bash
poe test [...]      # pytest
poe coverage [...]  # pytest (with branch coverage and terminal report)
```

## Structure

Every `example` name below is a placeholder to be renamed when the template is copied.

```text
nonebot_plugin_example/  Placeholder package, renamed when the template is copied
  __init__.py            Plugin metadata, `__version__` and `require` declaration
  __main__.py            Empty placeholder for runtime plugin logic
  config.py              Pydantic `ConfigModel` and `config` instance
.github/
  workflows/             Matrix pytest with Codecov, PyPI publish
  FUNDING.yml            Sponsor links
pyproject.toml           Hatchling build, `poe test`/`coverage` tasks, pytest config
codecov.yml              Codecov comment thresholds
README.md                Template usage and plugin docs
LICENSE                  MIT license text
.gitignore               Python and workspace ignore rules
```

## Rules

- Keep test coverage as high as possible to avoid dead code. Code included in the current runtime's coverage scope should be covered unless it is version-specific, dependency-gated, or an intentional error path that is impractical to trigger safely.

## Gotchas

Currently empty
