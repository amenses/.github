# Commit Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/) for clear, machine-readable history.

## Format

```
<type>(<scope>): <subject>

[optional body]

[optional footer(s)]
```

## Types

| Type | Description |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no logic change |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `perf` | Performance improvement |
| `test` | Adding or updating tests |
| `build` | Build system or dependencies |
| `ci` | CI configuration |
| `chore` | Maintenance tasks |
| `revert` | Revert a previous commit |

## Examples

```
feat(auth): add OAuth2 login flow

fix(api): handle null response from payment gateway

docs(readme): add local development setup instructions

ci: enable dependency review on pull requests
```

## Rules

- **Subject line:** imperative mood, max 72 characters, no trailing period
- **Scope:** optional but encouraged (module, package, or area)
- **Body:** explain *why*, not *what* (the diff shows what)
- **Breaking changes:** add `BREAKING CHANGE:` in the footer or `!` after type

```
feat(api)!: remove deprecated v1 endpoints

BREAKING CHANGE: v1 API endpoints removed. Migrate to v2.
```

## Squash Merging

When squash-merging PRs, the squash commit message should follow the same format. GitHub PR titles should be written as valid conventional commit subjects.

## Related Policies

- [Pull Request Guidelines](pull-request-guidelines.md)
- [engineering-standards — Commit Message Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Commit-Message-Policy.md)
