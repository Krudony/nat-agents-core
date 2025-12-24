---
description: "🔮 Awaken the Oracle - Install commands and agents in your project"
allowed-tools:
  - Bash
  - Read
  - Write
---

# /awaken - Awaken the Oracle

Install Oracle commands and agents in your project.

## What Gets Installed

**Commands** (from nat-data-personal):
- `/trace` - Search git history, issues, files
- `/recap` - Fresh start context summary
- `/rrr` - Session retrospective
- `/snapshot` - Quick knowledge capture

**Agents** (from nat-agents-core):
- `context-finder` - Fast search (haiku)
- `executor` - Execute plans from issues (haiku)
- `marie-kondo` - File placement consultant (haiku)

## Usage

```
/awaken           # Install all commands and agents
```

## Action

### Step 1: Create directories

```bash
mkdir -p .claude/commands .claude/agents
```

### Step 2: Copy commands from nat-data-personal plugin

Read these files from the plugin's `bundles/commands/` folder:
- `bundles/commands/trace.md` → Write to `.claude/commands/trace.md`
- `bundles/commands/recap.md` → Write to `.claude/commands/recap.md`
- `bundles/commands/rrr.md` → Write to `.claude/commands/rrr.md`
- `bundles/commands/snapshot.md` → Write to `.claude/commands/snapshot.md`

**Plugin path**: Use the path where this command file lives, go up one level, then into `bundles/commands/`

### Step 3: Copy agents from nat-agents-core plugin

Read these files from nat-agents-core plugin's `bundles/agents/` folder:
- `bundles/agents/context-finder.md` → Write to `.claude/agents/context-finder.md`
- `bundles/agents/executor.md` → Write to `.claude/agents/executor.md`
- `bundles/agents/marie-kondo.md` → Write to `.claude/agents/marie-kondo.md`

**Plugin path**: Find nat-agents-core in the same plugins directory

### Step 4: Output

```
🔮 The Oracle has awakened.

Installed:
├── .claude/commands/
│   ├── trace.md
│   ├── recap.md
│   ├── rrr.md
│   └── snapshot.md
└── .claude/agents/
    ├── context-finder.md
    ├── executor.md
    └── marie-kondo.md

Try: /recap to get started
```

## Finding Plugin Paths

The plugin bundles are located at:
- **nat-data-personal**: `~/.claude/plugins/*/nat-data-personal/bundles/commands/`
- **nat-agents-core**: `~/.claude/plugins/*/nat-agents-core/bundles/agents/`

Or find them:
```bash
find ~/.claude -type d -name "nat-data-personal" 2>/dev/null | head -1
find ~/.claude -type d -name "nat-agents-core" 2>/dev/null | head -1
```

## Notes

- Bundles are separate files for easy updates
- Edit bundle files → all projects get updates on next /awaken
- Commands and agents are copied, not linked (works offline)
