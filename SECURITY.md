# Security Policy

## Supported Versions

Security updates are provided for actively maintained repositories. Check each repository's README or release notes for supported versions.

| Version | Supported |
|---------|-----------|
| Latest release | Yes |
| Previous major | Best effort |
| Older versions | No |

## Reporting a Vulnerability

**Do not** open a public GitHub issue for security vulnerabilities.

Report security issues to:

- **Email:** [security@amenses.com](mailto:security@amenses.com)
- **Subject line:** `[SECURITY] <repository-name> — brief description`

Include:

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

## Response Timeline

| Stage | Target |
|-------|--------|
| Acknowledgment | Within 48 hours |
| Initial assessment | Within 5 business days |
| Fix or mitigation plan | Within 30 days (severity-dependent) |
| Disclosure coordination | After fix is deployed |

## Disclosure Policy

We follow coordinated disclosure. We ask that you:

- Give us reasonable time to investigate and remediate before public disclosure.
- Avoid accessing, modifying, or deleting data that is not yours.
- Avoid actions that degrade service availability.

We will credit reporters who wish to be acknowledged, unless they prefer to remain anonymous.

## Security Practices

Organization-wide security practices are documented in:

- [docs/security-policy.md](docs/security-policy.md)
- [engineering-standards — Security Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Security-Policy.md)

## Automated Scanning

Repositories inherit workflows for:

- **CodeQL** — static application security testing
- **Dependency Review** — vulnerable dependency detection on pull requests
- **Dependabot** — automated dependency update alerts
