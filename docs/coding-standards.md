# Coding Standards

Organization-wide coding standards for Amenses engineering. Team-specific conventions may extend but not contradict these rules.

## General Principles

1. **Readability over cleverness** — code is read more than written
2. **Small, focused changes** — one concern per PR
3. **Test what matters** — cover business logic and edge cases
4. **No secrets in code** — use environment variables and secret managers
5. **Fail explicitly** — handle errors; don't swallow exceptions silently

## Language-Specific Guidelines

Detailed language standards live in [engineering-standards](https://github.com/amenses-innovation/engineering-standards):

- [Coding Standards](https://github.com/amenses-innovation/engineering-standards/blob/main/Coding-Standards.md)
- [API Design Guidelines](https://github.com/amenses-innovation/engineering-standards/blob/main/API-Design-Guidelines.md)
- [Database Standards](https://github.com/amenses-innovation/engineering-standards/blob/main/Database-Standards.md)

## Cross-Cutting Rules

### Naming

- Use descriptive names: `getUserById` not `getData`
- Booleans: `isActive`, `hasPermission`, `canEdit`
- Constants: `UPPER_SNAKE_CASE`
- Files: match language conventions (kebab-case for configs, PascalCase for React components)

### Functions

- Single responsibility — one reason to change
- Max ~30 lines where practical
- Avoid deep nesting (prefer early returns)

### Comments

- Explain *why*, not *what*
- Keep comments up to date with code changes
- Use TODO with issue reference: `// TODO(#123): remove after migration`

### Error Handling

- Return meaningful error messages
- Log errors with context (request ID, user ID where appropriate)
- Never log secrets, tokens, or PII

### Dependencies

- Pin versions in lockfiles
- Justify new dependencies in PR description
- Prefer well-maintained, widely-used libraries

## Code Review Checklist

Reviewers should verify:

- [ ] Logic is correct and handles edge cases
- [ ] Tests cover the change
- [ ] No security vulnerabilities introduced
- [ ] No unnecessary complexity
- [ ] Documentation updated if behavior changed
- [ ] Performance impact considered

## Tooling

Projects should configure:

- **Linter** — ESLint, Ruff, golangci-lint, etc.
- **Formatter** — Prettier, Black, gofmt, rustfmt
- **Type checker** — TypeScript, mypy, etc. (where applicable)
- **Pre-commit hooks** — recommended for local validation

## Related Documents

- [Pull Request Guidelines](pull-request-guidelines.md)
- [Repository Standards](repository-standards.md)
