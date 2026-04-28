# dbt-helper skill

> An [Agent Skill](https://agentskills.io) that helps you work with [dbt](https://www.getdbt.com/) projects — run models, execute tests, compile SQL, generate docs, and check source freshness.

[![Agent Skills](https://img.shields.io/badge/Agent_Skills-compatible-blue)](https://agentskills.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Quick start

### Preview before installing

```bash
gh skill preview erlendhbarstad/tricky-dbt-skill dbt-helper
```

### Install

```bash
# Install as a personal skill (available across all projects)
gh skill install erlendhbarstad/tricky-dbt-skill dbt-helper --scope user

# Or install as a project skill (available only in the current repo)
gh skill install erlendhbarstad/tricky-dbt-skill dbt-helper
```

### Use

Once installed, just ask your AI assistant to help with dbt tasks. The skill activates automatically when relevant:

```
"Run the dbt models in the staging folder"
"Test all models and show me what failed"
"Check source freshness for the raw schema"
"Generate dbt docs for this project"
```

Or invoke it explicitly:

```
Use the /dbt-helper skill to compile and validate my SQL models
```

## What's included

| Feature | Description |
|---------|-------------|
| **Model execution** | Run dbt models with selectors, tags, and full/incremental strategies |
| **Testing** | Execute dbt tests with filtering and output formatting |
| **SQL compilation** | Compile Jinja SQL to raw SQL for debugging |
| **Documentation** | Generate and serve dbt docs |
| **Source freshness** | Check source freshness and flag stale data |

## Skill structure

```
skills/dbt-helper/
├── SKILL.md                          # Skill instructions and metadata
├── references/
│   └── dbt-best-practices.md         # dbt best practices reference
└── scripts/
    └── dbt-run-wrapper.sh            # Helper script for safe dbt execution
```

## Requirements

- [dbt-core](https://docs.getdbt.com/docs/core/installation-overview) installed and configured
- A valid `profiles.yml` with at least one target
- GitHub CLI ≥ 2.90.0 (for `gh skill` commands)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

[MIT](LICENSE)
