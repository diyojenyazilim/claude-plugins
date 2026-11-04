# diyojenyazilim claude-plugins

Claude Code plugins and mods by diyojenyazilim.

## Install

Add the marketplace once, then install any plugin from it:

```bash
claude plugin marketplace add diyojenyazilim/claude-plugins
claude plugin install <plugin>@diyojenyazilim
```

Inside a session: `/plugin marketplace add diyojenyazilim/claude-plugins` and `/plugin install <plugin>@diyojenyazilim`. If you install while a session is open, run `/reload-plugins` or start a new session.

To pick up new plugins and new versions later:

```bash
claude plugin marketplace update diyojenyazilim
```

## Plugins

| Plugin | What it does | Repository |
| --- | --- | --- |
| `pixel-agent` | A pixel-art agent above your prompt that reacts to Claude Code, with a small companion for every running subagent. | [diyojenyazilim/pixel-agents](https://github.com/diyojenyazilim/pixel-agents) |

## Adding a plugin

Each plugin lives in its own repository, with `.claude-plugin/plugin.json` at the repository root. List it here by adding an entry to [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json):

```json
{
  "name": "my-plugin",
  "source": { "source": "github", "repo": "diyojenyazilim/my-plugin" },
  "description": "One line that says what it does."
}
```

The entry `name` must equal the `name` in the plugin's `plugin.json`. Run `claude plugin validate .` after every edit.

## License

MIT, see [LICENSE](LICENSE).
