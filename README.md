# Pre-commit Hooks for Cairo

Enhance your [Cairo](https://www.cairo-lang.org/) development workflow with the [pre-commit](https://pre-commit.com) toolset.

## Integrating Cairo Tools with pre-commit
1. Begin by installing pre-commit using pip (refer to [pre-commit documentation](https://pre-commit.com/#install) if needed).
```sh
pip install pre-commit
```

2. Create a `.pre-commit-config.yaml` file in the root of your project.

3. Populate your pre-commit configuration with the desired hooks:
```yaml
repos:
    - repo: https://github.com/dubzn/pre-commit-cairo.git
      rev: v0.1.4
      hooks:
          - id: scarb-fmt
            args: [--check] # This argument is optional, you can remove '--check' to apply scarb fmt directly
          - id: scarb-test  
            args: []
            # include other hooks   
```

*Note: The available hooks for version `v0.1.4` are:*
```yaml
# Scarb

# Format code using Scarb.
- id: scarb-fmt

# Run Scarb tests to ensure the reliability of the Cairo project.
- id: scarb-test

# Use Scarb to execute the build process for the Cairo project.
- id: scarb-build

# Foundry

# Run Foundry tests to ensure the reliability of the Cairo project.
- id: foundry-test
```

4. Install pre-commit config.
```sh
pre-commit install
```

5. Enjoy the streamlined development process! 🎉 

---

### Make sure you have the dependencies installed according to your project:
- [Scarb](https://docs.swmansion.com/scarb/) 
- [Foundry](https://foundry-rs.github.io/starknet-foundry/getting-started/installation.html)
