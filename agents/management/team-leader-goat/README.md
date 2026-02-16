# Team Leader Goat (Manual Install)

This folder contains the "Team Leader Goat" agent configuration for manual installation.

## Files

- `team-leader-goat.md`: The agent prompt/configuration.

## Installation

### Claude Code (Local Reference)

You can reference this file directly in your `claude` command:

```bash
claude --agent-file ./agents/management/team-leader-goat/team-leader-goat.md "Your complex request here"
```

### Copy/Paste (Other Tools)

1.  Open `team-leader-goat.md`.
2.  Copy the entire content.
3.  Paste it into your tool's custom instruction or "persona" setting.
    - **Cursor**: Save as `.cursor/rules/team-leader.mdc`.
    - **Gemini CLI**: Add to your system prompt or a specific agent configuration.
