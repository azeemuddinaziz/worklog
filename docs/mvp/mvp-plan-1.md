# MVP plan 1

A simple chat with an agent that logs your work. Not refined; user-facing first. Terms follow [GLOSSARY.md](../../GLOSSARY.md). Scope source: [Scope and roadmap](../product/scope-and-roadmap.md). Concepts to learn first: [MVP 1 concepts](mvp-1-concepts.md).

There is no fixed deadline. The original target was about five days of building, but learning comes first, so the order below matters more than the duration.

## What the MVP does

You talk to the agent about your work. It proposes Log Entries as cards in the chat. You approve, edit or reject each card. Approved entries appear in a read-only Worklog view, grouped by Project and day.

## Decisions

| Area | Decision |
| --- | --- |
| Capture | Inline path only: one approval card per proposed Log Entry. No Review Draft panel. |
| Saving | Nothing is saved until approved. A proposed entry is a row in the log entries table with a status (`pending`, `approved`, `rejected`). Approval is an HTTP endpoint, not a model action. |
| Agent | Vercel AI SDK so the provider is swappable. Starts on Claude Sonnet, chosen by env config. |
| Tools | `propose_log_entries`, `create_project`, `list_projects`, `query_worklog`, `ask_choice` |
| Clarifying questions | `ask_choice` renders clickable chips; a click sends a normal Message and typing still works. |
| Dates | One confirmed day per entry, resolved from the client's date and timezone. If work spans several days the agent asks. Estimated Entries are deferred. |
| New Projects | Agent asks with a chip; on yes, the server creates the Project. No slash form. |
| Entry fields | All four Content Types. Optional people involved and impact (nullable, never asked). |
| Card editing | Summary, day, Project, Content Type. |
| Context | The model sees the system prompt, the Project list with descriptions, today's date and the last 30 Messages. The 30 is one config value. |
| Scope guard | System prompt only. |
| Failures | Error bubble with Retry. The user's Message is stored first. |
| Auth | None. One hard-coded user, with `user_id` on every table. |
| Backend | Express, Prisma, Postgres (local system install, no Docker). All backend logic lives here. |
| Frontend | Next.js, Tailwind, shadcn. Frontend only. |

## Backend API

| Endpoint | Purpose |
| --- | --- |
| `POST /chat` | Send a Message, stream the reply |
| `GET /messages` | Conversation history |
| `POST /entries/:id/approve`, `/reject` | Decide a pending Log Entry |
| `PATCH /entries/:id` | Edit a pending Log Entry |
| `GET /entries` | Worklog, filterable by Project |
| `GET/POST/PATCH /projects` | List, create, edit and archive Projects |

## Build order

Backend first, with automated tests on the backend rules (for example, nothing is saved before approval).

1. Project skeleton and database schema
2. Agent loop and tools, exercised from the terminal
3. Chat screen with approval cards and chips
4. Worklog and Projects screens
5. Prompt tuning with real messages (the buffer)

## Deferred

Review Draft panel, Pending section and summaries, onboarding tour, `/project` form, revision history and trail, archiving and restoring Log Entries, estimated spreads, resume points, login, multiple Conversations.

## Known risk

Approved entries are read-only, so a wrong approved entry cannot be fixed until revision history and agent edits arrive. The card edit step is the only correction path.
