# claude-goat 🐐

A curated marketplace + foldered library of “GOAT” agent configurations (Markdown rule/agent prompts) for agentic coding tools.

## What this repo is
- **A Claude Code plugin marketplace** that lets you install individual GOAT agents (one per plugin) from the Claude Code UI/terminal.
- **A human-friendly folder structure** so you can also copy/paste agents into other tools (Cursor, Antigravity, Gemini CLI).

## Install

### Claude Code (via marketplace)
1. Add this marketplace (GitHub-hosted):
   - In Claude Code:  
     `/plugin marketplace add x86txt/claude-goat`
2. Browse + install a GOAT:
   - `/plugin browse`
   - `/plugin install goat-go-programmer@claude-goat` (example)

Validate locally (recommended):  
`claude plugin validate .`

### Claude Code (manual / local)
- Add as a local marketplace:
  - `/plugin marketplace add /path/to/claude-goat`
- Or load a single plugin dir directly (for dev/testing):
  - `claude --plugin-dir ./plugins/goat-go-programmer`

### Cursor (manual)
Cursor “rules” live under `.cursor/rules/` (often with `.mdc` extension).
- Copy the GOAT you want into: `.cursor/rules/claude-goat/`
- If Cursor expects `.mdc`, rename accordingly (content stays Markdown).

### Antigravity (manual)
Antigravity workspace rules commonly live under: `.agent/rules/` in your repo/workspace.
- Copy the GOAT you want into `.agent/rules/claude-goat/` and reference it in your workflow as needed.

### Gemini CLI (manual)
Gemini CLI reads user settings from `~/.gemini/settings.json` (and can be extended via MCP servers).
- Keep GOAT prompts in your repo (e.g., `agents/...`) and paste them into your agent instructions, or store them in your own prompt library.

## Compatibility note
These GOAT configs have been tested to **not** conflict with other Claude Code marketplaces/plugins (including `everything-claude-code` and `superpowers-marketplace`). Still, any AI toolchain can get… weird 🌀.

Use this prompt to self-audit conflicts:
> “Please review all of the skills, rules, and agents available to you and determine if any of them conflict. If they do, please provide me a structured table of the conflicting items and your recommended solution.”

## Repo layout (high level)
- `.claude-plugin/marketplace.json` — marketplace catalog
- `plugins/*` — one plugin per GOAT (installable in Claude Code)
- `agents/*` — the same GOAT configs organized by topic for manual use

## License
See `LICENSE`.
