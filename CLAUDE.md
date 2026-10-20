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
6. In grilling and other Q&A sessions, ask questions with `AskUserQuestion` (selectable options, max 4 per call) instead of plain-text question lists.
7. The owner is learning the engineering side while building. The first time a technical term appears in a reply, plan or PR, define it in one plain line. Prefer explaining over assuming.
8. MVP documents live in `docs/mvp/`. Plans are named `mvp-plan-N.md` (`mvp-plan-1.md`, `mvp-plan-2.md`, ...), and each plan's concepts-to-learn list is named `mvp-N-concepts.md`.
