# AI Context Kit

**Portable project context for ChatGPT, Claude, Cursor, Codex, and other AI assistants.**

AI Context Kit is a lightweight, open set of Markdown templates to keep project instructions, current status, decisions, tasks, and sources in one place. It works for software, research, business, creative, and personal projects.

## Start here

1. Read [QUICKSTART.md](QUICKSTART.md).
2. Copy the files from [template/](template/) into your own project repository.
3. Fill in PROJECT.md, INSTRUCTIONS.md, and CONTEXT.md.
4. Connect an AI client using its built-in GitHub integration, connector, or MCP tools where available. Otherwise, upload or paste the files manually. **A separate MCP server is not required.**
5. Review and commit context updates; ask the next assistant to read the latest files.

**Never put secrets or sensitive personal information in a public repository.** Your own project repository can be private.

## What is included

| File | Purpose |
| --- | --- |
| PROJECT.md | Purpose, scope, goals, constraints |
| INSTRUCTIONS.md | Rules for AI collaboration |
| CONTEXT.md | Current project state and handoff |
| DECISIONS.md | Accepted decisions and rationale |
| TASKS.md | Next steps and progress |
| SOURCES.md | References and provenance |
| agents/ | Optional AI role definitions |
| skills/ | Reusable working procedures |

See [ChatGPT + GitHub integration test instructions](platforms/chatgpt.md) and other [platform notes](platforms/).

## Design principles

- **Platform independent:** Markdown is the source of truth.
- **User owned:** Keep project data in your own repository or local files.
- **Explicit updates:** AI proposes changes; users approve important writes.
- **No backend required:** No database, custom API, or separate MCP server required; connection methods vary by AI client.
- **Honest about synchronization:** Shared GitHub files enable cross-client access only where the client has the necessary read/write tools. Context is not automatically loaded into every conversation.

## Status

Early MVP. Feedback and contributions are welcome.
