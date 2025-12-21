# nat-agents-core

Claude Code plugin: Core agents and commands for multi-project use.

## Installation

```bash
/install nat-agents-core
```

Or add to `.claude/settings.json`:
```json
{
  "enabledPlugins": {
    "nat-agents-core@nat-agents-core": true
  }
}
```

## Agents

| Agent | Purpose |
|-------|---------|
| `context-finder` | Fast search through git history, files, codebase |
| `coder` | Write code from specs |
| `executor` | Execute bash commands from specs |
| `planner` | Create implementation plans |

## Commands

| Command | Purpose |
|---------|---------|
| `/context-finder` | Search git/issues/retrospectives |

## Usage

These agents are available via the Task tool:

```
subagent_type: nat-agents-core:context-finder
subagent_type: nat-agents-core:executor
subagent_type: nat-agents-core:coder
subagent_type: nat-agents-core:planner
```

## Development

```bash
# Clone via ghq
ghq get laris-co/nat-agents-core

# Edit commands/agents
cd ~/Code/github.com/laris-co/nat-agents-core

# After changes, clear cache + restart Claude Code
rm -rf ~/.claude/plugins/cache/nat-plugins/
```

## License

MIT
