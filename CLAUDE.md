## Agent skills

### Issue tracker

Issues live in GitHub Issues (via the `gh` CLI). See `docs/agents/issue-tracker.md`.

### Triage labels

Default vocabulary: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: one `GLOSSARY.md` + `docs/adr/` at the repo root. See `docs/agents/domain.md`.

## Working criteria

1. Before implementing anything, pull the latest `main` (or the repo's default branch).
2. Create a feature branch from the freshly pulled default branch; never work on it directly.
3. Immediately after implementing anything, push and open a PR using the `pr` skill.
4. Always include a "Try It" section wherever possible (PR descriptions, summaries) with steps a user can follow to verify the change.
5. After each MVP or PR, propose updates to `docs/learning.md` (topics started, learned, or coming up) and apply them only once the user approves.
