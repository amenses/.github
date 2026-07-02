# Branching Strategy

Amenses uses a **trunk-based development** model with short-lived feature branches and protected `main`.

## Branch Types

| Branch | Pattern | Purpose | Lifetime |
|--------|---------|---------|----------|
| Main | `main` | Production-ready code | Permanent |
| Develop | `develop` | Integration branch (optional) | Permanent |
| Feature | `feature/<issue-id>-<short-description>` | New features | Days |
| Bugfix | `bugfix/<issue-id>-<short-description>` | Non-urgent fixes | Days |
| Hotfix | `hotfix/<issue-id>-<short-description>` | Production fixes | Hours |
| Release | `release/<version>` | Release preparation | Days |

## Workflow

### Features and Bugfixes

```
main ─────────────────────────────────────────────►
       \                           /
        feature/123-add-auth ─────/
```

1. Branch from `main` (or `develop` if your team uses it).
2. Open a PR early; keep changes small and focused.
3. Merge via squash after approval and CI pass.

### Hotfixes

```
main ────────●──────────────────────────────────►
              \
release/1.2 ───●── hotfix/456-fix-crash ──► cherry-pick to main
```

1. Branch from the affected release branch or `main`.
2. Fix, test, and merge with expedited review.
3. Cherry-pick to `main` and any active release branches.

### Releases

1. Create `release/<version>` from `main`.
2. Bump version, update changelog, final QA.
3. Merge to `main` and tag `vX.Y.Z`.
4. Deploy from the tag.

## Branch Protection Rules

`main` (and `develop` if used) must have:

- Required pull request reviews (minimum 1; 2 for infrastructure)
- Required status checks (CI, CodeQL where applicable)
- No force pushes
- No direct commits (admins excepted for emergencies)

## Naming Conventions

- Use lowercase and hyphens: `feature/42-user-authentication`
- Include issue ID when available
- Keep descriptions short (3–5 words)

## Related Policies

- [Commit Guidelines](commit-guidelines.md)
- [Pull Request Guidelines](pull-request-guidelines.md)
- [Release Process](release-process.md)
- [engineering-standards — Git Branching Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Git-Branching-Policy.md)
