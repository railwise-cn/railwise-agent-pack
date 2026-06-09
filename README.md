# Railwise Agent Pack

Install Railwise agents, skills, commands, tools, templates, and themes into supported coding agents — 65 assets (11 agents, 14 commands, 11 skills, 7 templates, 1 theme, 21 tools) with a zero-dependency installer.

## Install

Until the package is published to npm, install straight from GitHub:

```bash
npx github:railwise-cn/railwise-agent-pack install --target railwise --force
npx github:railwise-cn/railwise-agent-pack install --target codex
npx github:railwise-cn/railwise-agent-pack list
```

Once published to npm the same commands work via `npx @railwise/agent-pack ...`.

## Targets

| Target | Destination | Layout |
| --- | --- | --- |
| `railwise` | `~/.config/railwise` | `agent/ skill/ command/ tool/` |
| `opencode` | `~/.config/opencode` | `agent/ skill/ command/ tool/` |
| `codex` | `~/.codex` | `agents/ skills/ prompts/ tools/` |
| `claude` | `~/.claude` | `agents/ skills/ commands/ tools/` |
| `custom` | `--dest <path>` | `agent/ skill/ command/ tool/` |

## Commands

```bash
install --target <name> [--dest <path>] [--dry-run] [--force]   # copy assets
list                                                            # show all assets
where --target <name>                                           # show destination paths
```

`--dry-run` prints what would be copied; `--force` overwrites existing files.

## Regenerating

This pack is generated from [RAILWISE-CLI](https://github.com/railwise-cn/RAILWISE-CLI) via:

```bash
bun run assets:extract -- --out ../railwise-agent-pack --name @railwise/agent-pack --force
```
