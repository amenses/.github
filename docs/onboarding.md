# Onboarding Guide

Welcome to Amenses Innovation engineering. This guide gets you productive in your first week.

## Day 1 — Access & Accounts

- [ ] GitHub org invite accepted (`amenses-innovation`)
- [ ] Added to relevant GitHub teams (see [GitHub Teams](github-teams.md))
- [ ] Slack workspace access
- [ ] Password manager and 2FA enabled on all accounts
- [ ] Development machine set up (OS updates, Git, IDE)

## Day 1–2 — Orientation

- [ ] Read the [organization README](../README.md)
- [ ] Review [engineering-standards](https://github.com/amenses-innovation/engineering-standards)
- [ ] Read [Contributing Guidelines](../CONTRIBUTING.md) and [Code of Conduct](../CODE_OF_CONDUCT.md)
- [ ] Meet your onboarding buddy and engineering manager

## Week 1 — Development Setup

- [ ] Clone your team's primary repository
- [ ] Complete local development setup (see repo README)
- [ ] Run the test suite locally
- [ ] Make a small documentation PR to verify your workflow

### Essential Reading

| Document | Location |
|----------|----------|
| Branching strategy | [docs/branching-strategy.md](branching-strategy.md) |
| Commit guidelines | [docs/commit-guidelines.md](commit-guidelines.md) |
| Coding standards | [docs/coding-standards.md](coding-standards.md) |
| PR guidelines | [docs/pull-request-guidelines.md](pull-request-guidelines.md) |
| Security policy | [docs/security-policy.md](security-policy.md) |

## Week 2 — Contributing

- [ ] Pick up a `good first issue` or onboarding task
- [ ] Open a PR following team conventions
- [ ] Participate in code review (review at least one PR)
- [ ] Attend sprint ceremonies

## GitHub Workflow Quick Reference

```bash
# Start work on an issue
git checkout main && git pull
git checkout -b feature/123-short-description

# Commit and push
git add .
git commit -m "feat(scope): description"
git push -u origin HEAD

# Open PR on GitHub, request review, merge after approval
```

## Getting Help

- **Technical questions:** Team Slack channel
- **Access issues:** Engineering manager or `@devops`
- **Policy questions:** [engineering-standards](https://github.com/amenses-innovation/engineering-standards)
- **Security:** [SECURITY.md](../SECURITY.md)

## Related Policies

- [engineering-standards — Onboarding Guide](https://github.com/amenses-innovation/engineering-standards/blob/main/Onboarding-Guide.md)
