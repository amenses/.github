# FAQ

Frequently asked questions about the Amenses Innovation GitHub organization.

## General

### What is the `.github` repository?

The `.github` repository provides organization-wide defaults: profile README, issue templates, PR templates, workflows, CODEOWNERS, and documentation. GitHub automatically applies these defaults to repositories in the organization.

### What is `engineering-standards`?

A companion repository containing version-controlled governance policies (branching, commits, security, onboarding, etc.). `.github` focuses on automation; `engineering-standards` focuses on policy documents.

### How do I get access to the organization?

Ask your engineering manager to submit an access request. You'll receive a GitHub org invite and be added to relevant teams.

## Development Workflow

### Which branch should I branch from?

Branch from `main` unless your team uses a `develop` integration branch. See [branching strategy](branching-strategy.md).

### What commit message format should I use?

[Conventional Commits](commit-guidelines.md): `type(scope): description`

### How do I choose a PR template?

When opening a PR, select the template matching your change type:

- Feature → `feature.md`
- Bug fix → `bugfix.md`
- Hotfix → `hotfix.md`
- Release → `release.md`
- Documentation → `documentation.md`

### Do all repos run the same CI?

Repositories inherit starter workflows from `.github/workflows/`. Projects can enable, customize, or extend them. The CI workflow auto-detects project type (Node, Python, Go, Rust).

## Security

### How do I report a security vulnerability?

Email [security@amenses.com](mailto:security@amenses.com). Do **not** open a public issue. See [SECURITY.md](../SECURITY.md).

### Are dependency updates automated?

Dependabot is configured for weekly updates across GitHub Actions, npm, Composer, NuGet, Maven, Gradle, Docker, and pip. Individual repos use the ecosystems relevant to them.

## Repository Management

### How should I name a new repository?

Follow the [repository naming conventions](repository-naming.md): `<category>-<name>` in lowercase with hyphens.

### What files must every repo have?

See [repository standards](repository-standards.md). At minimum: README, LICENSE, .gitignore, and CODEOWNERS.

### Can I rename a repository?

Yes, but update CI/CD configs, documentation links, and notify dependent teams. GitHub provides temporary redirects.

## Getting Help

### Who do I ask for help?

- **Technical:** Team Slack channel
- **Access:** Engineering manager or DevOps
- **Policies:** [engineering-standards](https://github.com/amenses-innovation/engineering-standards)
- **Security:** [SECURITY.md](../SECURITY.md)

See also [SUPPORT.md](../SUPPORT.md).
