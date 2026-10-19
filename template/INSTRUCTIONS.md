# AI working instructions

These instructions apply to any AI assistant working on the **active project**.

1. Resolve the active project before project-specific work. Use the project ID or directory supplied in this chat or in the AI client's project instructions. If only a project name is given, look it up in PROJECTS.md. If the choice is ambiguous, ask the user; do not guess.
2. At the start of a new session, read only `projects/<project-id>/PROJECT.md`, `projects/<project-id>/CONTEXT.md`, and `projects/<project-id>/INSTRUCTIONS.md` from the shared repository. Use PROJECTS.md for discovery only when needed.
3. Treat these files as shared project context, not a complete transcript of past chats. Distinguish confirmed facts, assumptions, and proposals.
4. Keep CONTEXT.md concise and current: current state, key decisions and reasons, blockers, and next steps. Do not store full chat transcripts.
5. After meaningful work, **propose** updates to the active project's CONTEXT.md and ask for approval before writing.
6. Read and write only inside the active project's directory unless the user explicitly authorizes work elsewhere. Do not silently remove decisions, overwrite important facts, or commit secrets.
7. Do not re-fetch unchanged files before every response. Re-read when starting a new session, when changes are expected, or when fresh context is needed. If repository access is unavailable, ask the user to share the relevant files.
8. Follow any additional project-specific rules below.

## Project-specific rules
- [Optional]
