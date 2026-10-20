# AI working instructions

These are the shared rules for **working on this project**. The repository, directory, and active-project verification are configured separately in the AI client's Project Instructions.

1. Use `PROJECT.md` to understand goals and constraints, and `CONTEXT.md` for current status, decisions, and next steps. These files are not full chat transcripts.
2. Respect existing decisions and constraints before suggesting changes. Distinguish verified facts, assumptions, and recommendations; do not invent missing information.
3. Tailor suggestions to the project's goals. For important changes, briefly explain benefits, limitations, and alternatives. Avoid unnecessary complexity.
4. Keep `CONTEXT.md` concise and current: status, decisions and reasons, blockers, and next steps. Do not store full transcripts.
5. **Proactive context sync:** After completing a meaningful task, making an important decision, changing project status, or identifying a blocker or next step, proactively check whether `CONTEXT.md` needs updating, without waiting for the user to ask. If it does, propose a concise, specific update, show it to the user, and **wait for approval before writing**. Record only durable outcomes, decisions and reasons, current status, blockers, and actionable next steps; do not log routine messages, intermediate reasoning, or unchanged details. Combine related changes into one update. If nothing material changed, do not propose an update. Never silently remove previous decisions or important facts.
6. Never commit passwords, keys, or other secrets. Do not modify files in other projects without an explicit request.
7. **Freshness check:** Do not re-fetch files before every response. Before important decisions that depend on project status, and before proposing or saving a context update, re-read the latest `CONTEXT.md` from GitHub. Do not assume a version loaded earlier in the chat is still current.
8. **Optimistic concurrency control:** Before saving, compare the latest `CONTEXT.md` with the version used to prepare the proposed changes; reconcile intervening edits with the user. Where the write integration supports it, use the file's current SHA/version as a precondition for the update. On a version conflict, stop, re-read, and seek approval for the revised change; never overwrite silently. If version-checked writes are unavailable, disclose that protection is not guaranteed and ask the user to apply the approved change through a version-controlled workflow.
9. Follow the additional rules below.

## Project-specific rules

[Add requirements for this project here: technologies, style, constraints, quality criteria, or other agreements. Leave blank if none apply.]
