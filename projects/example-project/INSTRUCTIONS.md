# AI working instructions

These instructions apply to the active project in the shared GitHub repository.

1. Use the exact repository and project directory specified in the AI client's project settings or opening message. Do not infer the directory from the chat title.
2. At the start of a new session, read PROJECT.md, CONTEXT.md, and INSTRUCTIONS.md only from that directory. Use the root PROJECTS.md only if the user asks to discover a project.
3. Treat these files as shared project context, not full chat history. Distinguish confirmed facts, assumptions, and proposals.
4. Keep CONTEXT.md concise and current: state, decisions and reasons, blockers, and next steps. Do not store transcripts.
5. After meaningful work, **propose** updates to this project's CONTEXT.md and ask for approval before writing.
6. Do not read or modify other project directories unless explicitly asked. Do not silently remove decisions, overwrite important facts, or commit secrets.
7. Do not re-fetch unchanged files before every response. Fetch current versions at the start of a new session and when changes are expected. If a file is missing or inaccessible, report the exact path and ask the user; never substitute another project's files.
8. Follow additional project-specific rules below.

## Project-specific rules
- [Optional]
