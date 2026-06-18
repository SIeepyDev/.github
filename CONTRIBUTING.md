# Contributing

Thanks for your interest. These projects are maintained by Sleepy Productions. This guide covers the standard workflow across all repos.

## Branch & commit

- Work on a short-lived branch off the trunk; keep the trunk green.
- Trunk branches are protected: **no force-pushes, no deletions.** Direct pushes are allowed for maintainers.
- Write clear commit messages: a concise subject line, then a body explaining the *why* when it isn't obvious.
- Never commit secrets, API keys, tokens, or personal data. Use environment variables.

## Code review

Every non-trivial change gets a review before it lands on the trunk:

1. **Open a pull request** using the template. Link the issue it closes.
2. **Automated review** runs on the PR (e.g. Copilot review where enabled) — address what it flags.
3. **Self / maintainer review** of the diff: correctness, security (no leaked secrets, safe input handling), and that the change does what the PR says.
4. Merge once it builds clean and the checklist is satisfied.

For trivial fixes (typos, docs), a direct push to a working branch is fine — just keep the trunk protected and clean.

## Quality bar

- It builds clean and existing tests pass.
- No secrets or personal data in the diff.
- Behavior matches what the PR/commit claims.
- Local-first and privacy-respecting: no new telemetry or off-device calls without a clear, stated reason.

## Reporting bugs & requesting features

Use the issue templates. For security issues, follow [SECURITY.md](SECURITY.md) — report privately, not in a public issue.
