# Capture and review

How a user's words become approved Log Entries. Terms follow [GLOSSARY.md](../../GLOSSARY.md).

## Layout

The chat is the main surface; a document panel (the Review Draft) opens beside it, on the right half of a large screen. A left panel lists Conversations, with a highlighted **Pending** section.

## Two paths

The agent chooses by the size of the input. The user can always ask for a Review Draft.

### Short message (inline path)

A short message about a single Project: the agent clarifies and shows the proposed Log Entry in the chat, with interactive choices for anything unclear. The user approves it there.

### Large dump (Review Draft path)

A full-day or multi-Project/multi-day dump: the agent gathers everything, asking clarifying questions at each message, then produces a Review Draft in the side panel.

## Review Draft

- One document, divided by Project, containing one block per proposed Log Entry.
- Colour-coded blocks, not a line-by-line diff (suitable for non-developers):
  - **Green**: new entry
  - **Red**: changed or removed since the last version, after the user asks for a change
  - **Amber**: needs the user's input (unclear date, unclear Project, estimated spread)
- Interactive elements sit inside the document wherever there is confusion.
- The user can quote any part and ask the agent to fix it.
- Approval is **per Log Entry**. Nothing enters the Worklog until approved.
- At the end the agent asks for a final confirmation before saving.

## New Projects

When a message fits no existing Project:

- **Review Draft path**: the draft itself asks, in the document, whether to create a new Project for the entries.
- **Inline path**: the agent asks in chat whether to create a Project; if yes, it shows a short form (name, description/your role).

## Pending work

If the user leaves a Conversation unfinished or doesn't answer something:

- The Conversation is listed in the highlighted **Pending** section of the left panel, with its drafts.
- After a while (about one to two weeks) the agent summarises what happened and where it was interrupted, and offers to continue so the user is never left without context.
- Nothing is saved without approval, however long it stays pending.
