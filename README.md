# Cairo hooks for pre-commit

[Cairo](https://www.cairo-lang.org/) tools package for [pre-commit](https://pre-commit.com).

## Using cairo tools with pre-commit
1. Install pre-commit with pip (or check [pre-commit](https://pre-commit.com/#install) docs).

2. Create a .pre-commit-config.yaml in your root project

3. Add the hooks that you want in your pre-commit configuration
```yaml
-   repo: https://github.com/dubzn/pre-commit-cairo
    rev: v0.1.0 
    hooks:
    -   id: scarb-fmt
    -   id: scarb-build
    -   id: scarb-clean
    -   id: scarb-test

    -   id: foundry-test
```

4. Execute pre-commit install

5. Enjoy!

⚠️ This repository uses 
- [Scarb](https://docs.swmansion.com/scarb/) 
- [Foundry](https://foundry-rs.github.io/starknet-foundry/getting-started/installation.html)
