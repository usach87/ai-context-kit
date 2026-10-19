# Quick start

🌐 **Language:** English · [Русский](QUICKSTART.ru.md)

[← README](README.md)

## 1. Create one shared repository

Create a GitHub repository such as `username/my-ai-context`. It can be public or private; a private repository is recommended for personal or commercial projects. To let AI assistants read and update files in a private repository, connect GitHub in each AI client you use and grant access to that repository. Private files are inaccessible without authorization. Add [PROJECTS.md](PROJECTS.md) to the repository root and the [projects/example-project/](projects/example-project/) template folder to its `projects/` directory.

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

Rename `example-project` to a recognizable, unique folder name such as `project-one`. Choose either the English or Russian templates. Keep three files: `PROJECT.md`, `CONTEXT.md`, and `INSTRUCTIONS.md`. For Russian templates, remove `.ru` from the filenames. Delete the other language's files.

Fill the files with AI assistance, review the result, and add the project name, description, and exact directory such as `projects/project-one/` to `PROJECTS.md`.

## 3. Connect GitHub

Follow the setup guide for [ChatGPT](platforms/chatgpt/chatgpt.md), [Claude](platforms/claude/claude.md), [Cursor](platforms/cursor/cursor.md), or [Codex](platforms/codex/codex.md). Use a supported integration or MCP, or provide the files manually. Verify read access; writing may require additional permissions.

## 4. Create a project in your AI client

Create a separate **Project** in ChatGPT or Claude for `project-one` (or an equivalent workspace in another client, when available). Start new chats **inside that Project** so its persistent instructions apply.

## 5. Configure Project Instructions

Open **Project Instructions** in the AI Project you created. This is the **entry point**: specify the GitHub repository, project directory, and context verification here. Keep the project's working rules in the `INSTRUCTIONS.md` file inside that directory.

Copy and customize:

```text
Project:
- GitHub repository: username/my-ai-context
- Directory: projects/project-one/
- Expected name in PROJECT.md: [project name]

At the start of a new chat:
1. Read PROJECT.md, CONTEXT.md, and INSTRUCTIONS.md only
   from the specified GitHub directory.
2. Verify that all three files were read and the name in
   PROJECT.md matches the expected name. If the path is missing,
   a file is inaccessible, or the names differ, report the issue
   and ask for clarification. Never guess the directory or
   substitute another project's context.
3. Briefly report the repository, directory, and project name
   you actually verified.
4. Follow the rules in the loaded INSTRUCTIONS.md.
   If GitHub is unavailable, ask for the files manually;
   do not claim to have read them.
```

**AI role (optional).** If you want a particular kind of help, add your preference to Project Instructions, such as “Help me design software architecture, write code, and find bugs.” Describe the tasks and outcomes you expect. For varied tasks, you can specify the role in each chat instead.

Fill in the project name in `PROJECT.md` first (step 2). It must match the expected name in these instructions but does not need to match the folder or AI Project name.

**Important:** Project Instructions do not connect GitHub automatically or provide technical isolation. Verify that the AI actually read the right files. If persistent instructions are unavailable, paste this text at the start of a new chat.

## 6. Work and save context

After meaningful work, ask the assistant to propose changes to `projects/project-one/CONTEXT.md`. Review and approve before writing. Before important decisions and context updates, the AI should check the latest `CONTEXT.md` in GitHub. For writes, it should use a version/SHA check when supported, and stop to reconcile conflicts instead of overwriting changes. If the integration cannot enforce version checks, it must say so. Do not load unrelated projects or save full transcripts.

## 7. Continue working on another AI platform

For example, you've set up your project in ChatGPT and now want to continue in Claude.

1. **Connect GitHub** to the new AI platform and grant access to the context repository (step 3).
2. **Create an AI Project** on the new platform (step 4).
3. **Configure Project Instructions** using the example in step 5. Specify the same GitHub repository and project directory.
4. **Open a chat** inside the new AI Project and ask it to load `PROJECT.md`, `CONTEXT.md`, and `INSTRUCTIONS.md`. Verify that the AI read the files from the correct directory.

You can now continue working with the context stored in GitHub.

**On subsequent switches** between already configured AI Projects, you don't need to repeat these steps. Just open a new chat in the relevant project and load the latest context.

## 8. Add more projects

Copy `projects/example-project/`, rename the folder, fill its three files, and add a row to `PROJECTS.md`. Bind each AI workspace to its corresponding directory. Put [optional files](optional/) inside that project's folder.

**Privacy:** never commit secrets. GitHub directories do not have independent access controls; use separate repositories when access requirements differ.

[← README](README.md) · [Русский](QUICKSTART.ru.md)
