# Quick start

🌐 **Language:** English · [Русский](QUICKSTART.ru.md)

[← AI Context Kit README](README.md) · [README на русском](README.ru.md)

AI Context Kit lets you continue **any project** in another AI chat without starting from scratch.

## 1. Create your project repository

Copy the three files from [template/](template/) into your own GitHub repository (private if needed). You can also download the files and share them manually.

## 2. Describe your project

Ask your AI assistant: "Help me fill in PROJECT.md, CONTEXT.md, and INSTRUCTIONS.md for my project. Ask me only the questions you need."

- **PROJECT.md** — what the project is and what success looks like.
- **CONTEXT.md** — what's happening now, key decisions, progress, and next steps.
- **INSTRUCTIONS.md** — how assistants should work with this context.

## 3. Connect your AI chat

Use a built-in GitHub integration/connector if supported. GitHub MCP is **optional**, not required. Confirm that the integration can read your repository; writing may require different permissions or may be unavailable.

If direct GitHub access is unavailable, provide the Markdown files manually.

Platform guides: [ChatGPT](platforms/chatgpt/chatgpt.md), [Claude](platforms/claude/claude.md), [Cursor](platforms/cursor/cursor.md), [Codex](platforms/codex/codex.md). You do not need to copy or fill in `platforms/`; these are reference guides.

## 4. Work, then save

Ask the assistant to read the latest three files. When you finish a meaningful session, ask it to **propose** changes to CONTEXT.md, including key decisions and next steps. Approve the changes before saving or committing them.

## 5. Continue in another AI chat

Ask the new assistant to fetch the current files from your repository, or upload them manually. Verify it used the latest content. No integration automatically synchronizes entire chat histories.

## Optional files

If CONTEXT.md becomes too large, add separate logs from [optional/](optional/): DECISIONS.md, TASKS.md, and SOURCES.md.

## Privacy

Do not commit passwords, access tokens, or sensitive personal data. Use a private repository for confidential projects.
