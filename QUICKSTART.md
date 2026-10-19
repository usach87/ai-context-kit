# Quick start

🌐 **Language:** English · [Русский](QUICKSTART.ru.md)

[← README](README.md)

## 1. Create one shared repository

Create a GitHub repository such as `username/my-ai-context`. Copy [PROJECTS.md](PROJECTS.md) to its root, then copy the entire [projects/example-project/](projects/example-project/) template folder into its `projects/` directory.

```text
my-ai-context/
├── PROJECTS.md
└── projects/
    ├── Sophia/
    │   ├── PROJECT.md
    │   ├── CONTEXT.md
    │   └── INSTRUCTIONS.md
    └── I-Design-Award/
        ├── PROJECT.md
        ├── CONTEXT.md
        └── INSTRUCTIONS.md
```

## 2. Rename and fill the example project folder

Rename `example-project` to a recognizable, unique folder name such as `Sophia`. **No separate project ID is required.** Keep only one language's three files: English `PROJECT.md`, `CONTEXT.md`, `INSTRUCTIONS.md`, or Russian `PROJECT.ru.md`, `CONTEXT.ru.md`, `INSTRUCTIONS.ru.md` (remove `.ru` from the filenames in your repository). Remove unused language versions.

Fill the files with AI assistance, review the result, and add the project name, description, and exact directory such as `projects/Sophia/` to `PROJECTS.md`.

## 3. Connect GitHub

Follow the setup guide for [ChatGPT](platforms/chatgpt/chatgpt.md), [Claude](platforms/claude/claude.md), [Cursor](platforms/cursor/cursor.md), or [Codex](platforms/codex/codex.md). Use a supported integration or MCP, or provide the files manually. Verify read access; writing may require additional permissions.

## 4. Bind the AI workspace to the exact path

If your AI client supports persistent project instructions, create a separate AI workspace for this project and paste:

> GitHub repository: `username/my-ai-context`. Branch: `main`. Active project directory: `projects/Sophia/`. At the start of a new session, read `projects/Sophia/PROJECT.md`, `projects/Sophia/CONTEXT.md`, and `projects/Sophia/INSTRUCTIONS.md` from that repository and branch. Do not read other projects. If any file is unavailable, report the exact path and error; never substitute another project's context. Propose updates only inside this directory and write only after my approval.

Replace the repository, branch, and directory. **A Git branch and a project directory are different concepts.** Project instructions provide an exact target, but do not grant GitHub access or guarantee that every client will obey them. If persistent instructions are unavailable, paste this at the start of a chat.

## 5. Work and save context

After meaningful work, ask the assistant to propose changes to `projects/Sophia/CONTEXT.md`. Review and approve before writing. Do not load unrelated projects or save full transcripts.

## 6. Continue in another AI chat

Open an AI workspace with the same configured repository and path. Ask it to fetch the latest files and confirm their exact paths. If settings do not transfer between platforms, repeat step 4. `PROJECTS.md` is for browsing projects, **not a required lookup on every session**.

## 7. Add more projects

Copy `projects/example-project/`, rename the folder, fill its three files, and add a row to `PROJECTS.md`. Bind each AI workspace to its corresponding directory. Put [optional files](optional/) inside that project's folder.

**Privacy:** never commit secrets. GitHub directories do not have independent access controls; use separate repositories when access requirements differ.

[← README](README.md) · [Русский](QUICKSTART.ru.md)
