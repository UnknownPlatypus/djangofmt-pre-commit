# djangofmt-pre-commit

A [pre-commit](https://pre-commit.com/) hook for [djangofmt](https://github.com/UnknownPlatypus/djangofmt).

Distributed as a standalone repository to enable installing djangofmt via prebuilt wheels from
[PyPI](https://pypi.org/project/djangofmt/).

### Installation

Add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
- repo: https://github.com/UnknownPlatypus/djangofmt-pre-commit
  rev: v1.0.0
  hooks:
    - id: djangofmt
```

To also lint your templates, add the `djangofmt-check` hook:

```yaml
- repo: https://github.com/UnknownPlatypus/djangofmt-pre-commit
  # Djangofmt version.
  rev: v1.0.0
  hooks:
    # Run the linter.
    - id: djangofmt-check
      args: [--fix]
    # Run the formatter.
    - id: djangofmt
```

Pass `args: [--fix]` to `djangofmt-check` to apply safe fixes automatically.
