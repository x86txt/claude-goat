# Contributing to ClaudeGoat

This repo is intentionally opinionated: GOAT agents should be **useful, safe, low-conflict, and testable**.

## Ground rules
- Keep GOAT agents **Markdown-only**.
- Prefer **clear constraints** and **explicit output contracts** over vibes.
- Don’t add “magic frameworks” or tool-specific commands unless they’re widely supported.

## Changes to an existing GOAT
Your PR must include:

1. **Claim** — what you improved (one sentence)
2. **Proof** — documented evidence the change is better:
   - before/after example prompts + outputs, OR
   - a small benchmark, OR
   - reproducible scenario + why the new behavior is safer/more correct
3. **Non-regression** — confirm you didn’t break compatibility:
   - Claude Code plugin validation passes (`claude plugin validate .`)
   - No new collisions in namespaces, plugin names, or skill names
   - Confirm no conflicts with common marketplaces (e.g., `everything-claude-code`, `superpowers-marketplace`) *or* document any known overlaps and mitigation

## Adding a brand new GOAT agent
Please include:
- A new agent file in the appropriate `agents/<category>/<topic>/` folder
- A matching Claude Code plugin in `plugins/<plugin-name>/` with:
  - `.claude-plugin/plugin.json`
  - `agents/<same-agent-file>.md`
- A short README in the agent folder describing what it **does** and **does not** do
- Add it to `.claude-plugin/marketplace.json`

## Naming conventions
- Plugins: `goat-<thing>` (kebab-case)
- Agent files: `goat-<thing>.md`
- Keep plugin name and agent file name aligned.

## PR checklist
- [ ] `claude plugin validate .` passes
- [ ] New/updated agent has proof of improvement (see above)
- [ ] Category + agent README files are present/updated
