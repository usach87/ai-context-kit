# Codex

## Connect a repository

Official OpenAI guides: [Codex quickstart](https://developers.openai.com/codex/quickstart), [MCP in Codex](https://developers.openai.com/codex/mcp).

**In Codex CLI or IDE**, open a locally cloned GitHub repository; no extra GitHub connector is required to read its local files. Configure MCP if GitHub API access is needed. **Codex cloud** uses a separate repository connection and permissions. Verify available read and write tools.

🌐 **Language:** English · [Русский](codex.ru.md)

[← README](../../README.md) · [Quick start](../../QUICKSTART.md)

Use `PROJECT.md`, `CONTEXT.md`, and `INSTRUCTIONS.md` directly from the project repository. AI Context Kit does **not require AGENTS.md**; `INSTRUCTIONS.md` is the single source of collaboration rules.

Ask Codex explicitly to read all three files before working. Do not assume `INSTRUCTIONS.md` is automatically discovered as an agent instruction file. Review proposed changes to context before writing or committing. Verify which GitHub and MCP tools your Codex environment exposes before relying on automatic writes.
