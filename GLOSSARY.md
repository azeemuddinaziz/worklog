# Worklog

A chat-based logger where working professionals talk through their day and an agent organises it into a reviewed, dated trail of their work.

## Language

**Message**:
A single piece of raw chat input from the user or reply from the agent, kept permanently as part of the Conversation.
_Avoid_: Prompt, input

**Conversation**:
The persistent chat history of Messages between a user and the agent, browsable like any chat app.
_Avoid_: Session, thread

**Log Entry**:
One organised record of a single Content Type on a single day for a single Project, extracted by the agent from Messages and approved by the user. It links back to its source Messages. One day can hold several Log Entries; work spanning several days or Projects is split into several; each is approved and keeps a revision history when edited.
_Avoid_: Log, note, record

**Estimated Entry**:
A Log Entry whose day was proposed by the agent as a likely spread rather than stated by the user. It stays visibly marked until the user confirms it.
_Avoid_: Draft entry, guess

**Archived**:
The state of a Log Entry or Project the user has set aside. It is hidden from default views but never deleted, can be restored, and an archived Log Entry may carry a reason. Log Entries are archived only by asking the agent; every archive and restore is kept in the trail.
_Avoid_: Deleted, removed

**Content Type**:
The kind of thing a Log Entry records. Actual work is primary; emotional events and office politics are secondary types, each kept as its own Log Entry.
_Avoid_: Category, tag

**Worklog**:
The collection of all a user's approved Log Entries.
_Avoid_: Journal, history

**Project**:
A separate stream of work (a job, an open-source contribution, a personal project) that Log Entries are grouped under.
_Avoid_: Workspace, folder

**Review Draft**:
The agent's proposed Log Entries for a batch of Messages, presented as a side document grouped by Project. Changes are colour-marked, unclear items need the user's input, and the user can quote any part to ask for a fix. Nothing enters the Worklog until each Log Entry is approved.
_Avoid_: Preview, pending log
