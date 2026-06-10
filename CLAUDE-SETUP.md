# Claude Code Setup — Where Everything Lives

A reference for where your global Claude file and your skills/commands are stored.

## 🌐 Global CLAUDE.md

**Location:** `~/.claude/CLAUDE.md`
(full path: `/Users/drmatrix99/.claude/CLAUDE.md`)

- This is the **global / user-level** instruction file. It loads in **every** project you open with Claude Code, on this machine, for your user account.
- It holds cross-project preferences: British English, concise tone, git defaults, latest-Claude defaults.
- A **project-level** `CLAUDE.md` (this repo has one at `./CLAUDE.md`) is layered *on top* and can override or extend the global one.

**Load order (later wins):** global `~/.claude/CLAUDE.md` → project `./CLAUDE.md` → any subfolder `CLAUDE.md`.

## ⚙️ Global settings (incl. the VS Code auto-open hook)

**Location:** `~/.claude/settings.json`

- Personal settings for all projects: theme, workflows, and the `PostToolUse` hook that opens newly created files in Visual Studio Code.
- Not part of any git repo — it's machine-local config, so it isn't committed/pushed.

## 🧩 Skills & Commands — two different kinds

There are **two** kinds of "skills" in your setup, stored in different places:

### 1. Your custom skill/command — `website`
**Location:** `./.claude/commands/website.md`
(full path: `/Users/drmatrix99/Desktop/Claude Code/.claude/commands/website.md`)

- This is a **project slash command**. It lives inside this repo, so it's committed and only available when working in this project.
- Invoked by typing `/website`.
- Project commands go in `.claude/commands/`; you could also add user-wide ones in `~/.claude/commands/` (currently empty).

### 2. Built-in / bundled skills — everything else
**Location:** shipped *inside the Claude Code application itself* (not in your folders).

These are the skills that come with Claude Code and are available everywhere:
`deep-research`, `code-review`, `simplify`, `verify`, `run`, `update-config`, `keybindings-help`, `fewer-permission-prompts`, `loop`, `claude-api`, `init`, `review`, `security-review`.

You don't manage these as files — they're maintained by Anthropic and updated with the CLI.

## 📍 Quick map

| Thing | Path | Scope | In git? |
|-------|------|-------|---------|
| Global instructions | `~/.claude/CLAUDE.md` | All projects | No |
| Global settings + hook | `~/.claude/settings.json` | All projects | No |
| Project instructions | `./CLAUDE.md` | This repo | Yes |
| Project local settings | `./.claude/settings.local.json` | This repo (you only) | Gitignored |
| `/website` command | `./.claude/commands/website.md` | This repo | Yes |
| Built-in skills | (inside the Claude Code app) | All projects | N/A |
| Auto-memory | `~/.claude/projects/.../memory/` | This project's memory | No |
