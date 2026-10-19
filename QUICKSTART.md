# Quick start

🌐 **Language:** English · [Русский](QUICKSTART.ru.md)

[← README](README.md)

## 1. Create one shared repository

Create a GitHub repository such as `username/my-ai-context`. Copy [PROJECTS.md](PROJECTS.md) to its root, then copy the entire [projects/example-project/](projects/example-project/) template folder into its `projects/` directory.

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

## 2. Rename and fill the example project folder

Rename `example-project` to a recognizable, unique folder name such as `project-one`. Keep only one language's three files: English `PROJECT.md`, `CONTEXT.md`, `INSTRUCTIONS.md`, or Russian `PROJECT.ru.md`, `CONTEXT.ru.md`, `INSTRUCTIONS.ru.md` (remove `.ru` from the filenames in your repository). Remove unused language versions.

Fill the files with AI assistance, review the result, and add the project name, description, and exact directory such as `projects/project-one/` to `PROJECTS.md`.

## 3. Connect GitHub

Follow the setup guide for [ChatGPT](platforms/chatgpt/chatgpt.md), [Claude](platforms/claude/claude.md), [Cursor](platforms/cursor/cursor.md), or [Codex](platforms/codex/codex.md). Use a supported integration or MCP, or provide the files manually. Verify read access; writing may require additional permissions.

## 4. Create a project in your AI client

Create a separate **Project** in ChatGPT or Claude for `project-one` (or an equivalent workspace in another client, when available). Start new chats **inside that Project** so its persistent instructions apply.

## 5. Configure Project Instructions: context and AI role

Open **Project Instructions** in the AI Project you created. Specify both the GitHub location and **what kind of help** you want. Copy the example and replace the bracketed values:

```text
Project:
- GitHub repository: username/my-ai-context
- Branch: main
- Directory: projects/project-one/
- Expected name in PROJECT.md: [project name]

AI role:
- Primary: [developer / analyst / designer / general assistant]
- Additional roles: [optional]
- Preferences: [e.g. concise answers, detailed plans, code examples]

Rules:
1. At the start of a new session, read PROJECT.md, CONTEXT.md,
   and INSTRUCTIONS.md only from the specified directory and branch.
2. Verify that all three files are accessible and compare the name
   in PROJECT.md with the expected name. If the path is missing,
   a read fails, or the names differ, report the issue and ask.
   Never guess a directory or substitute another project's files.
3. After verification, briefly report the actual repository,
   branch, directory, and project name you read.
4. Work in the selected role while adapting to the user's task.
   Distinguish verified facts, assumptions, and proposals.
5. After meaningful work, propose updates only to this project's
   CONTEXT.md. Show changes and await approval before writing.
   Do not modify other projects.
6. If GitHub access is unavailable, do not claim to have read
   the files; ask the user to provide them manually.
```

**Roles shape the help you receive:** a developer focuses on architecture and code, an analyst on requirements and validation, and a designer on UX and visual solutions. You can select a general assistant or multiple roles and switch roles for a specific task.

Fill in the project name in `PROJECT.md` during step 2 before enabling the name check. The expected name should match the file content; it does not have to match the folder or AI Project name.

**Important:** a Git branch (`main`) is different from a directory (`projects/project-one/`). Project Instructions do not grant GitHub access or technically guarantee isolation; verify actual file reads. If persistent instructions are unavailable, paste this at the beginning of a new chat.

## 6. Work and save context

After meaningful work, ask the assistant to propose changes to `projects/project-one/CONTEXT.md`. Review and approve before writing. Do not load unrelated projects or save full transcripts.

## 7. Continue in another AI chat

Open an AI workspace with the same configured repository and path. Ask it to fetch the latest files and confirm their exact paths. If settings do not transfer between platforms, repeat step 5. `PROJECTS.md` is for browsing projects, **not a required lookup on every session**.

## 8. Add more projects

Copy `projects/example-project/`, rename the folder, fill its three files, and add a row to `PROJECTS.md`. Bind each AI workspace to its corresponding directory. Put [optional files](optional/) inside that project's folder.

**Privacy:** never commit secrets. GitHub directories do not have independent access controls; use separate repositories when access requirements differ.

[← README](README.md) · [Русский](QUICKSTART.ru.md)
