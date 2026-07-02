# Release Process

How Amenses ships software to production.

## Versioning

We follow [Semantic Versioning](https://semver.org/):

- **MAJOR** — incompatible API changes
- **MINOR** — backward-compatible features
- **PATCH** — backward-compatible bug fixes

Pre-release versions use suffixes: `v1.2.0-beta.1`, `v1.2.0-rc.1`

## Release Cadence

| Type | Cadence | Branch |
|------|---------|--------|
| Regular release | Bi-weekly or per sprint | `release/X.Y.Z` |
| Hotfix | As needed | `hotfix/*` |
| Major release | Quarterly (planned) | `release/X.0.0` |

Teams may adjust cadence; document deviations in the repository README.

## Release Steps

### 1. Prepare

- [ ] All targeted issues/PRs merged to `main`
- [ ] Create `release/X.Y.Z` branch from `main`
- [ ] Bump version in manifests (`package.json`, `pyproject.toml`, etc.)
- [ ] Update `CHANGELOG.md`

### 2. Validate

- [ ] Full test suite passes on release branch
- [ ] Staging deployment and QA sign-off
- [ ] Security scan clean
- [ ] Migration scripts tested (if applicable)

### 3. Release

- [ ] Open a [Release PR](../.github/PULL_REQUEST_TEMPLATE/release.md)
- [ ] Merge release branch to `main`
- [ ] Tag `vX.Y.Z` on `main`
- [ ] GitHub Release created (automated via [release workflow](../.github/workflows/release.yml))

### 4. Deploy

- [ ] Deploy tagged version to production
- [ ] Verify health checks and monitoring
- [ ] Notify stakeholders

### 5. Post-Release

- [ ] Monitor error rates for 24 hours
- [ ] Close release milestone
- [ ] Cherry-pick hotfixes as needed

## Changelog Format

```markdown
## [1.2.0] - 2026-07-02

### Added
- User profile export feature (#123)

### Fixed
- Login redirect loop on Safari (#456)

### Changed
- Upgraded Node.js to 20 LTS
```

## Rollback

If a release causes issues:

1. Revert to the previous tagged version
2. Deploy the previous tag
3. Open a hotfix if forward-fix is faster than revert
4. Conduct postmortem for P0/P1 incidents

## Related Policies

- [Branching Strategy](branching-strategy.md)
- [engineering-standards — Release Management Policy](https://github.com/amenses-innovation/engineering-standards/blob/main/Release-Management-Policy.md)
