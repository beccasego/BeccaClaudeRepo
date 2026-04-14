# Workshop Recap — April 14, 2026

## What We Set Up

### VS Code
- Opened BeccaClaude folder as the VS Code workspace
- Claude Code extension running inside VS Code terminal

### Git + GitHub
- Initialized git repo in BeccaClaude folder
- Connected to GitHub: `https://github.com/beccasego/BeccaClaudeRepo.git`
- First commit and push done; PR workflow working via `/commit-commands:commit-push-pr`

### Claude Code
- Running as the AI assistant inside VS Code
- Reads `CLAUDE.md` at the start of every session for project context
- Knows this folder is both the Obsidian vault and the knowledge base

### Starter Kit (Elnora AI)
- Cloned `claude-code-starter-kit` and merged into BeccaClaude
- Key files added: `TOOLS.md`, `docs/getting-started.md`, `marketplace-plugins.md`
- `CLAUDE.md` updated with Core Rules, KB config, and lazy-load references

### Obsidian
- Vault root = BeccaClaude folder (same as git repo)
- All work folders (BD, CI, Fundraising, Research) are live Obsidian notes
- `.gitignore` excludes Obsidian system files (workspace, cache)

### Plugins Installed
- **commit-commands** — `/commit`, `/commit-push-pr`, `/clean-gone`
- **document-skills** — `/docx`, `/pptx`, `/xlsx`, `/pdf`, and more

## Key Files to Know
| File | Purpose |
|------|---------|
| `CLAUDE.md` | Claude's instructions, loaded every session |
| `TOOLS.md` | Plugin and slash command reference |
| `.claude/knowledge-base.local.md` | Vault path config (local only) |
| `.gitignore` | Excludes Obsidian system files and secrets |
