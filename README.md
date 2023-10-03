# Cairo hooks for pre-commit

[Cairo](https://www.cairo-lang.org/) tools package for [pre-commit](https://pre-commit.com).

## Using cairo tools with pre-commit

```yaml
-   repo: https://github.com/dubzn/pre-commit-cairo
    rev: master
    hooks:
    -   id: fmt
    -   id: test
```
⚠️ This repository uses [Scarb](https://docs.swmansion.com/scarb/) commands, so it is a necessary dependency.
