# Security Policy

Organization-wide security practices for Amenses Innovation.

> For vulnerability reporting, see [SECURITY.md](../SECURITY.md).

## Principles

1. **Defense in depth** — multiple layers of security controls
2. **Least privilege** — minimum access required for each role
3. **Secure by default** — safe defaults in code and infrastructure
4. **Shift left** — security integrated into development, not bolted on

## Development Practices

### Secrets Management

- Never commit secrets, API keys, or credentials
- Use environment variables and secret managers (e.g., GitHub Secrets, cloud KMS)
- Rotate secrets on compromise or team member departure
- Scan for secrets in CI (recommended: gitleaks, trufflehog)

### Dependencies

- Enable Dependabot alerts on all repositories
- Review dependency PRs promptly
- Pin dependencies with lockfiles
- Run [Dependency Review](../.github/workflows/dependency-review.yml) on PRs

### Code Security

- Enable [CodeQL](../.github/workflows/codeql.yml) analysis
- Validate and sanitize all user input
- Use parameterized queries (no SQL injection)
- Apply Content Security Policy headers on web apps
- Use HTTPS everywhere

### Authentication & Authorization

- Enforce MFA on GitHub and cloud accounts
- Use OAuth/OIDC for application auth where possible
- Implement role-based access control (RBAC)
- Session tokens must expire and be revocable

## Infrastructure Security

- Infrastructure changes require DevOps team review
- Use IaC (Terraform, etc.) — no manual console changes for production
- Network segmentation and firewall rules
- Regular backup and disaster recovery testing

## Incident Response

1. **Detect** — monitoring, alerts, or responsible disclosure
2. **Contain** — limit blast radius
3. **Eradicate** — fix root cause
4. **Recover** — restore service
5. **Learn** — postmortem and preventive measures

## Compliance

- Log access to sensitive data
- Data retention policies per legal requirements
- Client data handling per [Client Handover Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Client-Handover-Policy.md)

## Related Policies

- [SECURITY.md](../SECURITY.md) — vulnerability reporting
- [engineering-standards — Security Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Security-Policy.md)
