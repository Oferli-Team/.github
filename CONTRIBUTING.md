# Oferli Engineering Contribution Guidelines

These guidelines define the default development workflow for Oferli repositories. Individual projects may override them where there is a clear technical, product, security, or client-driven reason.

## Branches

Create short-lived branches from the default branch. Recommended naming:

- `feature/<description>`
- `fix/<description>`
- `hotfix/<description>`
- `refactor/<description>`
- `chore/<description>`
- `docs/<description>`

Direct pushes to protected branches are not allowed except for a documented emergency bypass.

## Commits

Use Conventional Commit-style messages where practical:

```text
type(scope): description
```

Common types are `feat`, `fix`, `refactor`, `test`, `docs`, `ci`, `build`, `chore`, `perf`, and `revert`. Scopes such as `auth`, `payments`, `api`, `web`, `mobile`, and `infra` are optional but encouraged when useful.

Work-in-progress commits inside feature branches do not need to be perfect when the repository uses squash merging. The final PR title should follow the commit convention because it may become the final commit message.

## Pull requests

Meaningful changes should normally be merged through pull requests. Keep each PR as small as practical while still representing one complete logical change.

Each PR should explain what changed, why it changed, how it can be tested, and any migrations, environment variables, API changes, deployment implications, feature flags, or breaking changes. UI changes should include sanitized screenshots or recordings where useful.

Do not merge while required CI checks are failing. Resolve review discussions before merge.

## Code review

Review for correctness, security, maintainability, architecture, tests, error handling, backward compatibility, and deployment implications. Consider performance where it is relevant to the change.

Avoid blocking PRs solely because of personal style preferences when automated formatting or project conventions already cover the issue. Discuss large architecture decisions before significant implementation begins.

`CODEOWNERS` belongs in each working repository because review ownership depends on that repository's domains.

## Security and client confidentiality

Never commit passwords, access tokens, API keys, private keys, production credentials, customer data, or secrets from `.env` files. Use environment variables and approved secret-management systems.

Client repositories are private by default. Do not publish or submit client code, business information, screenshots, architecture details, customer information, or project materials to public repositories or unapproved external services, including AI tools.

## Documentation

Projects should document local setup, required environment variables, test commands, important architecture, API contracts, and deployment where applicable.

Organization members can access detailed engineering standards in the private [Oferli engineering handbook](https://github.com/Oferli-Team/oferli-docs). External contributors should follow this file and the repository-local documentation available to them.
