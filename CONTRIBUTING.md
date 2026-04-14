# Contributing to RepoLens

Thank you for your interest in contributing to RepoLens! This guide explains how to get involved.

## How to Contribute

### Reporting Bugs

Open a [GitHub issue](https://github.com/TheMorpheus407/RepoLens/issues) with:

- A clear description of the bug
- Steps to reproduce
- Expected vs. actual behavior
- Your environment (OS, bash version, agent CLI used)

### Suggesting Features

Open an issue with the `enhancement` label. Describe the use case and why it would benefit the project.

### Submitting Code

1. Fork the repository
2. Create a feature branch from `master`
3. Make your changes
4. Run the test suite: `make check`
5. Submit a pull request against `master`

### Adding a New Lens

RepoLens is designed to make adding analysis lenses easy:

1. Create `prompts/lenses/<domain>/<lens-id>.md` with YAML frontmatter (`id`, `domain`, `name`, `role`) and a `## Your Expert Focus` body
2. Add the lens ID to the appropriate domain in `config/domains.json`
3. No code changes needed

### Code Style

- All shell scripts use `set -uo pipefail`
- Functions should be pure where possible
- Config is JSON parsed with `jq`
- Logs follow the format: `[LEVEL] [timestamp] message`

## Development Setup

### Prerequisites

- Bash 4.0+
- `jq` for JSON processing
- `git` for repository operations
- At least one supported AI agent CLI (`claude`, `codex`, `opencode`, or `sparc`)

### Running Tests

```bash
make check
```

## License

By contributing, you agree that your contributions will be licensed under the [Apache License 2.0](LICENSE).
