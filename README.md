# AI Context Kit

**Share project context between AI chats — without depending on one AI platform.**

AI Context Kit is a small, open Markdown template for **any project**: business, research, creative, personal, or software. Keep a common source of truth in your own GitHub repository, and use it from ChatGPT, Claude, or another AI assistant.

## Get started

1. Read [QUICKSTART.md](QUICKSTART.md).
2. Copy the **three files** in [template/](template/) into your own repository.
3. Ask your AI assistant to help fill them in.
4. Connect GitHub through an available integration, connector, or MCP (optional), or share the files manually.
5. Ask each new AI chat to read the latest files. Review and approve updates before saving.

## The three essential files

| File | Purpose |
| --- | --- |
| [PROJECT.md](template/PROJECT.md) | Project goals, audience, scope, constraints |
| [CONTEXT.md](template/CONTEXT.md) | Current state, key decisions, recent progress, next step |
| [INSTRUCTIONS.md](template/INSTRUCTIONS.md) | How an AI assistant should use and update the shared context |

Need more structure later? See [optional/](optional/) for separate decision, task, and source logs. These are **not required** for the MVP.

Platform-specific tips: [ChatGPT](platforms/chatgpt.md), [Claude](platforms/claude.md), [Cursor](platforms/cursor.md), [Codex](platforms/codex.md).

## Principles

- **Universal:** No coding knowledge required; usable for business and personal projects.
- **Portable:** Plain Markdown, not tied to one model or chat.
- **User-owned:** Your own repository and revision history.
- **MCP optional:** A suitable built-in GitHub integration is enough; manual sharing is a fallback.
- **Explicit approval:** Review significant context changes before writing.
- **No automatic chat sync:** Assistants must fetch fresh context and save approved changes; capabilities vary by client.
- **Privacy:** Keep sensitive information out of public repositories; use a private repository when needed.

## Status

Minimal MVP. No backend or custom MCP server required.
