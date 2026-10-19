# ChatGPT + GitHub integration: test plan

🌐 **Language:** English · [Русский](chatgpt.ru.md)

[← README](../README.md) · [Quick start](../QUICKSTART.md)

Use an available GitHub integration or connector in ChatGPT; a separate official GitHub MCP server is **not required** for this workflow. Read and write capabilities depend on the environment, plan, and permissions. A built-in GitHub integration is not necessarily equivalent to a separately configured MCP server.

## Preconditions
1. Your own GitHub repository exists and contains the context files.
2. GitHub access is connected in ChatGPT with permissions appropriate for the test.
3. Confirm that the current ChatGPT environment exposes GitHub file-reading tools. For writing, confirm file-write tools separately.

## Test A — Read
Ask: "Read template/PROJECT.md and template/CONTEXT.md from OWNER/REPO. Summarize the project, citing which files you read."

Check that the assistant actually retrieves the files, rather than inferring their contents.

## Test B — Write
Ask: "Propose one harmless change to template/CONTEXT.md. Show me the exact diff and wait for my approval before writing."

After approval, request the commit, then verify the change on GitHub.

## Test C — Cross-assistant handoff
Read the updated file from another supported AI client. Confirm that it sees the latest committed content.

## Troubleshooting
- A connected GitHub account does not guarantee file read/write tools in every ChatGPT mode. Check actual tool access, not whether the connection is called MCP.
- If write tools are unavailable, use manual file updates.
- Do not use public repositories for sensitive project data.
