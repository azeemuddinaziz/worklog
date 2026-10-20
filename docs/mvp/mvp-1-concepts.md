# MVP 1 concepts

Everything to understand to build [MVP plan 1](mvp-plan-1.md) yourself, without an agent. Concepts only, no references.

## Web fundamentals
- Client and server; request and response
- HTTP methods, status codes, headers, JSON
- Endpoints and REST-style API design
- CORS
- Environment variables and secrets
- Streaming responses (Server-Sent Events)

## Backend with Node and Express
- Node runtime, modules (ESM), the event loop
- Promises and async/await; error handling
- Express routing, middleware, request validation
- Project structure: routes, services, data access
- Config management

## TypeScript
- Types, interfaces, unions, generics
- Narrowing and type safety at API boundaries
- Schema validation of runtime data

## Databases and Postgres
- Tables, rows, columns, primary and foreign keys
- Relations: one-to-many, many-to-many
- Indexes, constraints, enums, nullable columns
- Transactions
- Status columns and state transitions
- Migrations

## Prisma
- Schema file, models and relations
- Client queries, filtering, ordering
- Migrations and seeding

## Data modelling for this app
- Users, Projects, Conversations, Messages, Log Entries
- Linking a Log Entry to its source Messages
- Pending, approved and rejected as a state machine
- Soft state (archived) versus deletion
- Dates, timezones and storing a day

## LLMs and agents
- What an LLM is; tokens
- Context window and context building
- System prompt versus user messages
- Temperature and determinism
- Structured output and schema-constrained responses
- Tool use (function calling) and the agent loop
- Tool design: names, descriptions, input schemas, results
- Human-in-the-loop approval; keeping the model away from direct writes
- Prompt design, prompt tuning, and handling off-topic input
- Provider-agnostic abstraction and swapping models
- Cost, latency and rate limits
- Failure modes: timeouts, hallucination, malformed tool calls

## Agent behaviour for this app
- Routing text to the right Project
- Splitting one message into several Log Entries
- Resolving relative dates
- When to ask a clarifying question versus proceed

## Frontend with Next.js
- React components, props, state, effects
- Next.js App Router, server versus client components
- Fetching data; consuming a streamed response
- Forms and controlled inputs
- Optimistic and error states, retry

## UI
- Tailwind utility-first styling
- shadcn components and composition
- Chat layout and message rendering
- Rendering structured content (cards, chips) from tool results
- Accessibility basics

## Testing and quality
- Unit versus integration tests
- Test-driven development
- Testing against a real database
- Faking the model in tests
- Evaluating prompts with sample messages

## Tooling and workflow
- pnpm workspaces
- Git branches, pull requests
- Local Postgres setup
- Linting and formatting
