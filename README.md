<div align="center">

# diyojenyazilim · Claude Code plugins

**A small, hand-picked marketplace of plugins and mods for [Claude Code](https://github.com/anthropics/claude-code).**

[![License: MIT](https://img.shields.io/github/license/diyojenyazilim/claude-plugins?color=2F3A4A&labelColor=161B26)](LICENSE)

[Installation](#installation) · [Plugins](#plugins) · [Contributing](#contributing)

</div>

> [!WARNING]
> Make sure you trust a plugin before installing, updating or using it. Each plugin lives in its own repository and can change over time. Read its source and its README first.

## Installation

Add the marketplace once, then install any plugin from it:

```bash
claude plugin marketplace add diyojenyazilim/claude-plugins
claude plugin install <plugin>@diyojenyazilim
```

Inside a session, use `/plugin marketplace add diyojenyazilim/claude-plugins` and `/plugin install <plugin>@diyojenyazilim`, or browse the catalog with `/plugin > Discover`. If you install while a session is open, run `/reload-plugins` or start a new one.

To pick up new plugins and new versions later:

```bash
claude plugin marketplace update diyojenyazilim
```

## Plugins

| Plugin | What it does | Install |
| --- | --- | --- |
| [`pixel-agents`](https://github.com/diyojenyazilim/pixel-agents) | A pixel-art companion above your prompt that reacts to Claude Code, with a small friend for every running subagent. | `/plugin install pixel-agents@diyojenyazilim` |
| [`terminal-gui`](https://github.com/diyojenyazilim/terminal-gui) | Restyles tool and agent rows as running/done cards and assistant replies as chat bubbles. | `/plugin install terminal-gui@diyojenyazilim` |

### pixel-agents

<div align="center">
  <img src="assets/pixel-agents.svg" alt="The five pixel-agents characters: Bit, Ghost, Astronaut, Code Wizard and Cloud" width="560" />
</div>

A Claude Code mod that puts a small pixel-art agent above your prompt. It reacts to what Claude is doing, picks up a prop for the tool at hand, shows how full your context is, and gives every subagent a companion of its own. Five characters, six color themes.

[Read more](https://github.com/diyojenyazilim/pixel-agents#readme)

### terminal-gui

A Claude Code mod that restyles tool and agent rows as GUI-like cards, with running and finished states told apart, and shows assistant replies as chat bubbles. Requires Claude Code v2.1.287 or later.

```bash
claude plugin install terminal-gui@diyojenyazilim
```

[Read more](https://github.com/diyojenyazilim/terminal-gui#readme)

## How this repository is organized

```text
.
├── .claude-plugin/
│   └── marketplace.json   the catalog Claude Code reads
├── assets/                images used by this README
├── LICENSE
└── README.md
```

This repository holds only the catalog. Every plugin lives in its own repository.

## Contributing

Every plugin is its own public repository with `.claude-plugin/plugin.json` at the root and a license. To list one here, open a pull request that adds an entry to [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json):

```json
{
  "name": "my-plugin",
  "source": { "source": "github", "repo": "diyojenyazilim/my-plugin" },
  "description": "One line that says what it does.",
  "category": "interface",
  "keywords": ["mod", "ui"]
}
```

The entry `name` must equal the `name` in the plugin's `plugin.json`. Run `claude plugin validate .` after every edit.

## License

MIT, see [LICENSE](LICENSE). Each plugin carries its own license in its repository.
