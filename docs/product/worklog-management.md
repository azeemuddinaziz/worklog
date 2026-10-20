# Worklog management

Terms follow [GLOSSARY.md](../../GLOSSARY.md).

## Browsing

Everything lives in the same UI as the agent: Conversation history, Projects, and the Worklog by Project and day.

## Projects

- Created from a form (name, description/your role) or proposed by the agent. See [Capture and review](capture-and-review.md#new-projects).
- The description helps the agent route future messages.
- Users can **edit** and **archive** Projects directly.
- Users cannot delete Projects or move entries between Projects directly; they ask the agent.

## Editing Log Entries

- Edited via the agent or the entry view.
- Every edit keeps a revision history so past versions stay viewable.
- When the agent makes a change to a saved entry (edit, move to another Project, archive, restore), it shows the change for the user's approval first.

## Archiving and restoring

- There is **no deletion**. A Log Entry is archived instead, optionally with a reason.
- Archiving a Log Entry is done only by asking the agent.
- Archived entries and Projects remain viewable and can be restored through the agent.

## Trail

Every state change is recorded. An entry that was saved, archived, then restored shows all three events in its trail, with when and (for archiving) why.

## Open questions

- Exact UI for viewing the trail and revisions.
