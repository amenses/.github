# Repository Standards

This document defines the minimum standards every Amenses Innovation repository must meet.

## Required Files

Every application and library repository should include:

| File | Purpose |
|------|---------|
| `README.md` | Project overview, setup, and usage |
| `LICENSE` | License terms |
| `CONTRIBUTING.md` | Contribution guidelines (or link to org defaults) |
| `.gitignore` | Ignore build artifacts, secrets, and IDE files |
| `.github/CODEOWNERS` | Code review ownership (or inherit from org) |

## Recommended Files

| File | Purpose |
|------|---------|
| `CHANGELOG.md` | Version history |
| `SECURITY.md` | Security reporting (or inherit from org) |
| `docs/` | Extended documentation |
| `.github/workflows/ci.yml` | Continuous integration |

## Repository Settings

Configure the following in GitHub repository settings:

- **Default branch:** `main`
- **Branch protection:** Require PR reviews, status checks, and linear history (for production repos)
- **Merge options:** Squash merge preferred; rebase merge allowed
- **Delete head branches:** Enabled
- **Vulnerability alerts:** Enabled
- **Dependabot alerts:** Enabled

## Labels

Use consistent labels across repositories:

| Label | Color | Use |
|-------|-------|-----|
| `bug` | Red | Defects |
| `enhancement` | Green | Features |
| `documentation` | Blue | Docs work |
| `task` | Gray | Engineering chores |
| `dependencies` | Purple | Dependency updates |
| `security` | Dark red | Security-related |
| `triage` | Yellow | Needs prioritization |

## README Structure

A good README includes:

1. Project name and one-line description
2. Prerequisites and installation
3. Quick start / usage examples
4. Development setup
5. Testing instructions
6. Deployment notes (if applicable)
7. Links to related docs and policies

## Inheriting Organization Defaults

Repositories in the `amenses-innovation` organization automatically inherit:

- Issue templates from `.github`
- Default workflows (when enabled)
- Organization profile README
- Security policies

See [engineering-standards](https://github.com/amenses-innovation/engineering-standards) for governance policies.
