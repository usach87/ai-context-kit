# Quick start: multiple projects in one repository

🌐 **Language:** English · [Русский](QUICKSTART.ru.md)

[← AI Context Kit README](README.md)

Use one GitHub repository for multiple projects. Each AI chat selects **one active project** and reads only its directory.

## 1. Create a shared repository

Create a GitHub repository such as `username/my-ai-context`. Use a private repository for confidential projects. Copy [PROJECTS.md](template/PROJECTS.md) to the repository root.

```text
my-ai-context/
├── PROJECTS.md
└── projects/
    ├── family-app/
    │   ├── PROJECT.md
    │   ├── CONTEXT.md
    │   └── INSTRUCTIONS.md
    └── tea-business/
        ├── PROJECT.md
        ├── CONTEXT.md
        └── INSTRUCTIONS.md
```

`PROJECTS.md` is a small index of project names, IDs, and directories, not a collection of full project contexts.

## 2. Set up your first project

Choose a stable ID such as `family-app` and create `projects/family-app/`. Copy these three templates into that folder:

- [PROJECT.md](template/PROJECT.md) — goals and scope.
- [CONTEXT.md](template/CONTEXT.md) — current state and next steps.
- [INSTRUCTIONS.md](template/INSTRUCTIONS.md) — AI working rules.

[Russian templates](template/PROJECT.ru.md) are also available: copy them and remove `.ru` from the filenames. Add a row to `PROJECTS.md` with the project ID, name, description, and directory. Ask an AI assistant to help fill the templates, and review the proposed content before saving.

## 3. Connect your AI client to GitHub

Follow the platform guide: [ChatGPT](platforms/chatgpt/chatgpt.md), [Claude](platforms/claude/claude.md), [Cursor](platforms/cursor/cursor.md), [Codex](platforms/codex/codex.md).

Use an available GitHub integration, connector, or MCP. A custom MCP server is **not required**. Verify that the assistant can actually read the chosen directory. Write access varies by client and permissions. If GitHub access is unavailable, share the active project's three files manually.

## 4. Bind an AI workspace or chat to one directory

If your AI client supports persistent project instructions, create a workspace for “Family App” and add:

> Shared GitHub repository: `username/my-ai-context`. Active project: `family-app`. Directory: `projects/family-app/`. At the beginning of a new session, read `PROJECT.md`, `CONTEXT.md`, and `INSTRUCTIONS.md` **only from this directory**. Work only on this project's context and propose updates for approval. If files are inaccessible, say so; do not invent their contents.

Replace the example repository and ID. Use a different directory for each AI workspace. **Persistent instructions do not grant GitHub access by themselves**; configure access separately. If your client has no persistent project instructions, paste this text at the start of a new chat.

## 5. Work and save approved changes

After meaningful work, ask the assistant to propose updates to **`projects/family-app/CONTEXT.md`**. Review and approve before committing. Do not save full chat transcripts or load unrelated projects by default.

## 6. Continue in another AI chat

If the active project is already configured in the client's workspace instructions, ask it to load the latest project context.

Otherwise use this prompt:

> Open `username/my-ai-context`. Active project: `family-app`; directory: `projects/family-app/`. Read the three files there and summarize current status and the next step. Do not load other projects. If access fails, tell me.

If you only know a project name, the assistant can use `PROJECTS.md` to find the directory. If the name is ambiguous, it should ask you to choose. **A chat title alone does not reliably select a GitHub directory.** Full chat histories are not synchronized across platforms.

## 7. Add more projects

Create a separate directory with the same three files for each project, then register it in `PROJECTS.md`. Avoid root-level `CONTEXT.md` and `INSTRUCTIONS.md` that could mix different projects.

Optional [DECISIONS.md, TASKS.md, and SOURCES.md](optional/) files belong inside the corresponding project directory.

## Privacy

Do not commit passwords, tokens, or secrets. Use a private repository for sensitive projects. GitHub folder paths are **not** separate access-control boundaries; use separate repositories if projects require different permissions.

[← README](README.md) · [Быстрый старт на русском](QUICKSTART.ru.md)
