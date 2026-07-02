# GitHub Teams

GitHub teams map to engineering roles and control repository access via CODEOWNERS.

## Team Structure

| Team | Slug | Responsibility |
|------|------|----------------|
| Engineering | `@amenses-innovation/engineering` | Default code owners, all engineers |
| Backend | `@amenses-innovation/backend` | APIs, services, databases |
| Frontend | `@amenses-innovation/frontend` | Web and UI applications |
| Mobile | `@amenses-innovation/mobile` | iOS and Android applications |
| DevOps | `@amenses-innovation/devops` | CI/CD, infrastructure, deployments |
| Security | `@amenses-innovation/security` | Security reviews and policies |
| Product | `@amenses-innovation/product` | Product documentation and specs |

## Access Levels

| Level | Permissions | Typical Teams |
|-------|-------------|---------------|
| Read | Clone, view issues/PRs | All engineers (org-wide) |
| Triage | Manage issues and PRs | Engineering |
| Write | Push to branches, merge PRs | Team members on their repos |
| Maintain | Manage repo settings | Tech leads |
| Admin | Full control | DevOps, org admins |

## CODEOWNERS Integration

CODEOWNERS in each repository (or inherited from `.github`) automatically request reviews:

```
* @amenses-innovation/engineering
/backend @amenses-innovation/backend
/frontend @amenses-innovation/frontend
```

See [CODEOWNERS](../CODEOWNERS) for the organization defaults.

## Requesting Access

1. Ask your engineering manager which teams you need
2. Manager submits access request to org admin
3. Access granted based on role and project assignment
4. Access reviewed quarterly and on role change

## Team Maintenance

Org admins should:

- Remove departed members promptly
- Audit team membership quarterly
- Align teams with [engineering-standards — GitHub Team Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/GitHub-Team-Policy.md)

## Related Policies

- [Repository Standards](repository-standards.md)
- [engineering-standards — Repository Permissions Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Repository-Permissions-Policy.md)
