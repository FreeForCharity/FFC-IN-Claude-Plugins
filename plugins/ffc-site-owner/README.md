# Free For Charity – Site Owner Toolkit

A Claude plugin for nonprofits working with [Free For Charity](https://freeforcharity.org).
It works in Claude Desktop, claude.ai, and Claude Code. It contains skills only.

| Skill | Use it when you want to… |
|---|---|
| `ffc-getting-started` | Work through FFC's application prerequisites, apply, or set up your website-editing environment (GitHub + Claude) |
| `edit-my-site` | Change anything on your charity website: contact info, photos, text, team, donate button |
| `post-an-update` | Publish news, newsletters, board minutes, or events |
| `check-my-site` | Get a plain-language health check of your website |
| `ask-ffc-for-help` | Work out whether something is FFC's to do, and draft a message to the FFC team |

## Install

```
/plugin install ffc-site-owner --marketplace FreeForCharity/FFC-IN-Claude-Plugins
```

You don't need to name a skill. Describe what you want, for example
"I want to apply to Free For Charity — where do I start?" or
"Update our phone number to (555) 123-4567."

Human guides: https://ffcadmin.org/site-owner/ · https://ffcadmin.org/guides/

## Source of truth

The content follows FFC's founder-approved *Application & Prerequisites* inventory
(`FFC-IN-ffcadmin.org/docs/application-prerequisites-inventory.md`) and the
`/site-owner` pages on ffcadmin.org. When those change, update
`skills/ffc-getting-started/references/` and bump `version` in `.claude-plugin/plugin.json`.
