# SimplePark Project Conventions

These conventions apply to all repositories within the SimplePark GitHub organization.

## Repository Naming

- Use **lowercase** with **dashes** to separate words (e.g., `parking-api`, `payment-service`).
- Keep names short and descriptive. Avoid abbreviations that are not widely understood.
- For multi-repo projects, prefix repositories with a shared project name followed by a dash (e.g., `platform-api`, `platform-web`, `platform-docs`).
- Do not use camelCase or snake_case in repository names.

## Branch Naming

Use the following prefixes for branch names:

| Prefix    | Purpose                                                     |
|-----------|-------------------------------------------------------------|
| `feat/`   | New features (e.g., `feat/parking-zones`)                   |
| `fix/`    | Bug fixes (e.g., `fix/payment-timeout`)                     |
| `chore/`  | Maintenance, dependencies, CI (e.g., `chore/update-deps`)   |
| `docs/`   | Documentation changes (e.g., `docs/api-reference`)          |
| `hotfix/` | Urgent production fixes (e.g., `hotfix/null-pointer-crash`) |

- Use lowercase with dashes within the description portion.
- Keep branch names concise but meaningful.

## Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```text
<type>(<optional scope>): <description>

[optional body]

[optional footer(s)]
```

Common types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `ci`, `perf`, `build`.

Examples:

- `feat(zones): add geofence validation for parking zones`
- `fix(payments): handle timeout on iDEAL callback`
- `docs: update API authentication guide`

## Pull Request Naming

Follow the same [Conventional Commits](https://www.conventionalcommits.org/) format used for commit messages:

```text
<type>(<optional scope>): <description>
```

Common types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `ci`, `perf`, `build`.

Examples:

- `feat(zones): add geofence validation for parking zones`
- `fix(payments): handle timeout on iDEAL callback`
- `docs: update API authentication guide`

## Pull Requests

- Reference related issues (e.g., `Closes #42`).
- Keep pull requests focused -- one logical change per PR.

## Templates

GitHub templates are provided in the `.github/` directory to ensure consistency across repositories.

Issue templates use [GitHub's YAML issue forms](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-githubs-form-schema), which render as structured web forms with validated fields. Blank issues are disabled via `config.yml`.

| Template        | Path                                                                                       | Purpose                                |
|-----------------|--------------------------------------------------------------------------------------------|----------------------------------------|
| Bug Report      | [`.github/ISSUE_TEMPLATE/bug_report.yml`](.github/ISSUE_TEMPLATE/bug_report.yml)           | Reporting bugs with reproduction steps |
| Feature Request | [`.github/ISSUE_TEMPLATE/feature_request.yml`](.github/ISSUE_TEMPLATE/feature_request.yml) | Proposing new features or enhancements |
| Task            | [`.github/ISSUE_TEMPLATE/task.yml`](.github/ISSUE_TEMPLATE/task.yml)                       | General work or technical debt         |
| Template Config | [`.github/ISSUE_TEMPLATE/config.yml`](.github/ISSUE_TEMPLATE/config.yml)                   | Template chooser configuration         |
| Pull Request    | [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md)                     | Standard PR description structure      |

Use these templates when creating issues and pull requests. Repositories that need additional templates can extend this set while keeping the defaults.

## Code Style

Individual repositories should include their own language-specific linting and formatting configuration. At a minimum:

- Use an automated formatter (e.g., Prettier, dart format, Black) and enforce it in CI.
- Use a linter appropriate for the language.
- Prefer explicit over implicit. Favor readability over cleverness.
