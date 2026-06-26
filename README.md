# djangofmt-pre-commit

A [pre-commit](https://pre-commit.com/) hook for [djangofmt](https://github.com/UnknownPlatypus/djangofmt).

Distributed as a standalone repository to enable installing djangofmt via prebuilt wheels from
[PyPI](https://pypi.org/project/djangofmt/).

### Installation

Add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
- repo: https://github.com/UnknownPlatypus/djangofmt-pre-commit
  rev: v0.2.11
  hooks:
    - id: djangofmt
```

To also lint your templates, add the `djangofmt-check` hook:

```yaml
repos:
- repo: https://github.com/UnknownPlatypus/djangofmt-pre-commit
  rev: v0.2.11
  hooks:
    - id: djangofmt
    - id: djangofmt-check
```

Pass `args: [--fix]` to `djangofmt-check` to apply safe fixes automatically.