# Team Leader Goat Plugin

This plugin provides the "Team Leader Goat" agent for Claude Code.

## Agent: Team Leader Goat

- **Role**: Technical Lead / Project Manager
- **Model**: Claude 3.5 Opus (latest available)
- **Mode**: Delegate Only
- **Specialty**: Orchestrating complex tasks by breaking them down and assigning them to expert "teammate" agents.

## Usage

### 1. Install

```bash
claude plugin install team-leader-goat@x86txt/claude-goat
```

### 2. Run

```bash
claude --agent team-leader-goat "Refactor the entire legacy monolith into microservices"
```

The Team Leader will analyze your request, create a plan (`INITIAL_PLAN.md`), and orchestrate multiple specialized agents to perform the work in parallel.
