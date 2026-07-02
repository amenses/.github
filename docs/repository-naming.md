# Repository Naming

Consistent repository names improve discoverability and automation.

## Naming Convention

```
<category>-<name>
```

Use lowercase, hyphens as separators, no underscores or spaces.

## Categories

| Prefix | Examples | Description |
|--------|----------|-------------|
| `app-` | `app-platform`, `app-careers` | Applications and services |
| `lib-` | `lib-auth-sdk`, `lib-utils` | Shared libraries |
| `sdk-` | `sdk-python`, `sdk-typescript` | Client SDKs |
| `infra-` | `infra-terraform`, `infra-k8s` | Infrastructure as code |
| `design-` | `design-system`, `design-assets` | Design resources |
| `docs-` | `docs-api`, `docs-internal` | Documentation sites |
| `template-` | `template-service`, `template-frontend` | Repository templates |
| `tool-` | `tool-cli`, `tool-migrator` | Developer tools |

## Special Repositories

| Name | Purpose |
|------|---------|
| `.github` | Organization defaults, templates, and workflows |
| `engineering-standards` | Governance and policy documents |

## Rules

1. **Be descriptive** — `app-user-dashboard` not `app-ud`
2. **Avoid redundancy** — don't repeat the org name: `app-amenses-platform` ❌
3. **Match deployment names** — repo name should align with service name where possible
4. **No secrets in names** — repository names are public

## Renaming

Renaming a repository:

1. Update CI/CD references and deployment configs
2. Update documentation links
3. Set up redirects (GitHub handles automatic redirects for a period)
4. Notify dependent teams

## Related Policies

- [Repository Standards](repository-standards.md)
- [engineering-standards — Repository Naming Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Repository-Naming-Policy.md)
