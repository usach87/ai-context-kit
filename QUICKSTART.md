# Quick start

AI Context Kit is a portable set of Markdown files for keeping project knowledge independent of any single AI assistant.

## 1. Create your own copy
Use **Use this template** on GitHub (once enabled), or download this repository and create a private repository for your project. Do not put private data in a public repository.

## 2. Fill in the context
Start with `template/PROJECT.md`, `template/INSTRUCTIONS.md`, and `template/CONTEXT.md`. Add decisions to `template/DECISIONS.md` and tasks to `template/TASKS.md`. Rename or copy the `template/` directory to your project root if you prefer.

## 3. Connect an AI assistant
Use the AI client's built-in GitHub integration or connector when available. An official or custom GitHub MCP server is **optional**, not a prerequisite. Authorize access to **your** repository with the minimum necessary permissions and check read and write capabilities separately. Follow `platforms/chatgpt.md` for a ChatGPT test. If direct access is unavailable, upload or paste the Markdown files manually.

## 4. Work and save
Ask the assistant to read `PROJECT.md`, `INSTRUCTIONS.md`, and `CONTEXT.md` before starting. After work, ask it to propose updates to decisions, tasks, and current context. Review changes before committing.

## 5. Switch assistants
In the next assistant, request a fresh read from GitHub. Neither a GitHub connector nor an MCP server automatically injects repository contents into every conversation. Ask for a fresh read, and verify that the assistant retrieved the current files.

## Security
Never commit passwords, tokens, personal records, or other secrets. GitHub visibility and MCP permissions are separate controls. Use a private repository for personal or confidential context.
