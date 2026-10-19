# ChatGPT + GitHub MCP: test plan

GitHub MCP availability, setup steps, and write capabilities depend on the ChatGPT environment and plan. The GitHub app/connector is not necessarily equivalent to configuring a custom MCP server.

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
- A connected GitHub account does not guarantee MCP read/write capabilities in every ChatGPT mode.
- If write tools are unavailable, use manual file updates.
- Do not use public repositories for sensitive project data.
