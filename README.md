# AI Context Kit

🌐 **Language:** English · [Русский](README.ru.md)

**Share project context between AI chats — without depending on one AI platform.**

AI Context Kit is a small, open Markdown toolkit for **multiple projects**: business, research, creative, personal, or software. Keep each project's context in its own directory inside one GitHub repository, and continue from ChatGPT, Claude, or another AI assistant.

## Get started

1. Follow the [multi-project quick start](QUICKSTART.md) ([на русском](QUICKSTART.ru.md)).
2. Create a shared GitHub repository and copy [PROJECTS.md](PROJECTS.md) to its root ([Russian template](PROJECTS.ru.md)).
3. For each project, copy [projects/example-project/](projects/example-project/), rename it, and use `projects/project-folder/` and copy the **three files** from [projects/example-project/](projects/example-project/) into it. [Russian versions](projects/example-project/PROJECT.ru.md) are available; remove `.ru` from the filenames.
4. Register the project in `PROJECTS.md`, then connect your AI client to GitHub or share the files manually.
5. Set the active project's repository path in your AI workspace instructions or opening chat prompt. Read and update **only that project's files**.

```text
my-ai-context/
├── PROJECTS.md
└── projects/
    ├── project-one/
    │   ├── PROJECT.md
    │   ├── CONTEXT.md
    │   └── INSTRUCTIONS.md
    └── project-two/
        ├── PROJECT.md
        ├── CONTEXT.md
        └── INSTRUCTIONS.md
```

## The three essential files

| File | Purpose |
| --- | --- |
| [PROJECT.md](projects/example-project/PROJECT.md) | Project goals, audience, scope, constraints |
| [CONTEXT.md](projects/example-project/CONTEXT.md) | Current state, key decisions, recent progress, next step |
| [INSTRUCTIONS.md](projects/example-project/INSTRUCTIONS.md) | How an AI assistant should use and update the shared context |

Each project has its own three files. The root-level `PROJECTS.md` is a lightweight index, not a shared context dump. Need more structure later? See [optional/](optional/) for separate decision, task, and source logs. These are **not required** for the MVP.

Platform setup guides: [ChatGPT](platforms/chatgpt/chatgpt.md), [Claude](platforms/claude/claude.md), [Cursor](platforms/cursor/cursor.md), [Codex](platforms/codex/codex.md). ([Русские версии](README.ru.md))

## Principles

- **Universal:** No coding knowledge required; usable for business and personal projects.
- **Portable:** Plain Markdown, not tied to one model or chat.
- **User-owned:** Your own repository and revision history.
- **MCP optional:** A suitable built-in GitHub integration is enough; manual sharing is a fallback.
- **Explicit approval:** Review significant context changes before writing.
- **Project isolation:** The AI should resolve the active directory and not read other projects by default. GitHub folders do not provide separate access permissions.
- **No automatic chat sync:** Assistants must fetch fresh context and save approved changes; capabilities vary by client.
- **Privacy:** Keep sensitive information out of public repositories; use a private repository when needed.

## Status

Minimal MVP. No backend or custom MCP server required.

## License

Distributed under the [MIT License](LICENSE). Copyright © 2026 Sergey Usachev.
