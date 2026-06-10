# Claude Code Access & Permissions

This documents the standing permissions granted to Claude Code in this project, so it can work without prompting on every action. Set up at Chidi's explicit request ("give yourself all the access you need… don't ask again").

## Where it's configured

`./.claude/settings.local.json` — this is **personal & gitignored**, so the grant applies to your machine only and is not pushed to the repo. (This `ACCESS.md` is the committed, human-readable record of what was granted.)

## What's allowed (no prompt)

| Permission | Covers |
|------------|--------|
| `Read` | Read any file |
| `Edit` | Edit any file |
| `Write` | Create/overwrite any file |
| `Bash` | Any shell command (except the denied ones below) |
| `WebFetch` | Fetch any URL |
| `WebSearch` | Web searches |
| `Skill` | Run any skill (`/website`, `/deep-research`, etc.) |
| `mcp__…get_posts`, `mcp__…get_profile_history` | The connected MCP tools |

Plus **`defaultMode: "acceptEdits"`** — file edits apply automatically without a confirmation step.

## What's still denied (safety net)

Even with broad access, these stay blocked to prevent irreversible damage:

- `rm -rf /`, `rm -rf /*`, `rm -rf ~`, `rm -rf ~/*`, `sudo rm *` — catastrophic deletes
- `git push --force`, `git push -f` — force-push over remote history
- `git reset --hard origin/*` — destroy local work against remote
- Reading secrets: `.env` files, `~/.ssh/**`, `~/.aws/credentials`

If a genuinely-needed action hits the denylist, I'll flag it rather than work around it.

## Related config (machine-global, not in this repo)

- `~/.claude/settings.json` — global settings + the hook that opens new files in VS Code
- `~/.claude/CLAUDE.md` — global instructions

See [`CLAUDE-SETUP.md`](./CLAUDE-SETUP.md) for the full path map.

## Standing workflow

Per the saved workflow preference: after completing changes I **commit and push** automatically (branch `main`, which auto-deploys to GitHub Pages) without being asked each time.
