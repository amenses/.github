# Pull Request Guidelines

Guidelines for creating and reviewing pull requests at Amenses Innovation.

## Before Opening a PR

1. **Link an issue** — every PR should reference an issue unless it's a trivial fix (typo, dependency bump).
2. **Keep it small** — aim for < 400 lines changed; split large work into stacked PRs.
3. **Self-review** — read your own diff before requesting review.
4. **Run tests locally** — don't rely solely on CI.
5. **Choose the right template** — see [.github/PULL_REQUEST_TEMPLATE/](../.github/PULL_REQUEST_TEMPLATE/).

## PR Title

Follow [Conventional Commits](commit-guidelines.md):

```
feat(auth): add password reset flow
fix(api): validate email format on registration
```

## PR Description

Include:

- **What** changed and **why**
- **How** to test (step-by-step)
- **Screenshots** for UI changes
- **Breaking changes** clearly marked
- **Deployment notes** if applicable

## Review Process

### For Authors

- Respond to feedback within 2 business days
- Resolve conversations after addressing feedback
- Don't merge your own PR (except emergencies with lead approval)
- Ensure all CI checks pass before merge

### For Reviewers

- Review within 2 business days
- Be specific and constructive
- Distinguish blocking vs. non-blocking feedback
- Approve when satisfied; don't nitpick style if linter handles it

### Approval Requirements

| Repository Type | Required Approvals |
|---------------|-------------------|
| Application | 1 |
| Shared library | 2 |
| Infrastructure | 2 (+ DevOps team) |
| Security-sensitive | 2 (+ Security team) |

CODEOWNERS automatically request the right reviewers.

## Merge Strategy

- **Squash merge** — default for feature branches
- **Merge commit** — for release branches only
- **Rebase merge** — allowed when maintaining clean linear history

## After Merge

- Delete the feature branch
- Verify deployment (if auto-deployed)
- Close linked issues
- Monitor for regressions

## Related Documents

- [Branching Strategy](branching-strategy.md)
- [Commit Guidelines](commit-guidelines.md)
- [Release Process](release-process.md)
