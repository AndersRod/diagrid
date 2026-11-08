# AGENTS.md

Instructions for AI coding agents working in this repository.

## Workflow

### Branches

Never commit or push directly to `main`. It is protected, and every change lands through a pull request.

Name each branch `<type>/<short-kebab-description>`:

| Prefix        | Use for                                                   |
|---------------|-----------------------------------------------------------|
| `feature/`    | New functionality                                         |
| `fix/`        | Bug fixes going through the normal flow                   |
| `hotfix/`     | Urgent fixes that need to ship right away                 |
| `prototype/`  | Throwaway exploration; never merged as-is                 |
| `chore/`      | Tooling, dependencies, config, CI                         |
| `docs/`       | Documentation only                                        |

Example: `feature/user-onboarding`, `hotfix/login-timeout`.

### Pull requests

- Open a PR against `main` for every change.
- PRs are squash-merged, so the PR title becomes the commit message on `main`. Write it as a plain, descriptive sentence.
- The description explains what changed and why, and how it was verified.
- Resolve all review conversations before merging. The branch ruleset requires it.

### Commits

There's no commit-message convention. Write plain, descriptive messages.

### External references

Keep branch names, commit messages, PR titles and descriptions, code and docs free of links to, or IDs from, external planning tools.

## Decisions and domain language

- Domain terms are defined in `GLOSSARY.md` at the repository root.
- Architecture decisions are recorded as ADRs in `docs/adr/`, numbered sequentially (`0001-short-title.md`).
- Both are created lazily, when a term or decision is actually resolved. See `docs/agents/domain.md`.

## Agent skills

### Issue tracker

Work is tracked in an external tracker, configured per machine and not referenced from this repository. See `docs/agents/issue-tracker.md`.

### Domain docs

Single-context: one `GLOSSARY.md` and `docs/adr/` at the repository root. See `docs/agents/domain.md`.
