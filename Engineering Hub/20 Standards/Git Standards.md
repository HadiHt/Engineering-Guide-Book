# Git Standards

Use these rules for branch, commit, and merge hygiene.

## Branches

- Create branches for intentional units of work.
- Use clear names that communicate purpose.
- Prefer a team convention such as `<type>/<task-id>/<short-description>`.
- Do not push directly to protected branches unless explicitly allowed.

## Commits

- Keep commits small and reviewable.
- Use one logical change per commit when practical.
- Prefer a consistent commit convention, for example: `<type>(scope): short description`.
- Keep history readable before merge.

## Pull Requests

- Make the PR description clear about behavior changes, risks, and follow-ups.
- Rebase, squash, or fix up history when needed for readability.
- Do not merge with unresolved blocking review findings.

## Safety

- Never commit secrets.
- Do not commit local machine artifacts.
- Avoid large binary files unless they are intentionally part of the work.
