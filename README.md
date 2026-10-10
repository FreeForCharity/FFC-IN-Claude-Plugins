# Free For Charity — Claude Plugins

The Claude plugin marketplace for [Free For Charity](https://freeforcharity.org).

| Plugin | For |
|---|---|
| [`ffc-site-owner`](plugins/ffc-site-owner) | Charity applicants and site owners |

## Install (Claude Code)

```
/plugin marketplace add FreeForCharity/FFC-IN-Claude-Plugins
/plugin install ffc-site-owner@free-for-charity
```

## Develop

```
claude --plugin-dir ./plugins/ffc-site-owner   # try it for one session
claude plugin validate . --strict              # validate the marketplace and plugins
```
