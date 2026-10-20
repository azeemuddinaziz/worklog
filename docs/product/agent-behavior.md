# Agent behaviour

The agent is a professional companion and logger. Terms follow [GLOSSARY.md](../../GLOSSARY.md).

## Job

Turn what the user says into organised Log Entries, and answer questions about the user's Worklog.

## Understanding each message

After every Message the agent should be clear on what happened, which Project, which day and which Content Type. If anything is unclear it asks **right then**, with interactive elements (choices, chips, pickers) instead of free-text questions. The user can type if they prefer.

## Routing

- A user may dump several Projects in one message. The agent decides which part belongs to which Project.
- Each Log Entry has exactly one Project, one day and one Content Type. One message can therefore produce many Log Entries.
- When routing is uncertain, the agent asks via Project choices.
- When nothing fits an existing Project, see [Capture and review](capture-and-review.md#new-projects).

## Content Types (V1)

| Type | Examples |
| --- | --- |
| Work (primary) | tasks, deliverables, decisions |
| Manager/people issue | manager shouted at me, conflict |
| Office politics | colleagues backbiting |
| Learning / win / blocker | something learned, praise, what got in the way |

Example: "I worked on email sending, my manager shouted at standup, and colleagues were backbiting" becomes three Log Entries for the same day and Project.

## Optional details on a Log Entry

People involved, impact/outcome and Content Type, alongside the date, Project, summary, and links to the source Messages and Conversation. The agent asks about impact when it matters for the user's professional growth, but never blocks on optional details.

## Dates

- A Log Entry is always a single day.
- Relative dates ("last Thursday") are resolved and shown.
- If work happened over several days, or the user is unsure of the day, the agent proposes a likely spread across days and says clearly that it is **an estimate**. The user adjusts it.
- Approved entries from an estimated spread stay marked as [Estimated Entries](../../GLOSSARY.md) until the user confirms them.

## Scope boundaries

The agent talks about the user's professional life and Worklog only:

- Answers questions about the Worklog (for example "what did I do on the email project in September?").
- Gives advice and shares references when something at work seems off.
- Helps draft resume points from the Worklog (V1: on request, for chosen Projects and a target role).
- Politely declines anything else and redirects.

## Tone

Calm, brief, non-judgemental, especially around emotional and political entries.
