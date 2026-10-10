# FFC-IN-Claude-Plugins

Free For Charity's Claude plugin marketplace. `FFC-IN-` because this is an FFC-owned project;
`FFC-EX-` is reserved for one repo per external charity site (see `.claude/rules/00-ffc-mission.md`
in `FFC-IN-ffcadmin.org`).

## Layout

- `.claude-plugin/marketplace.json` — the marketplace (`free-for-charity`)
- `plugins/ffc-site-owner/` — public plugin for charity applicants and site owners (skills only)

The site-owner plugin must stay **skills-only**: no `bin/`, hooks, agents, or local MCP servers.
Claude Desktop and claude.ai chat ignore or reject those, and site owners use those apps.
FFC admin tooling belongs in a separate **private** repo, never here, because everything in this repo is public.

## Sources of truth

The skills restate FFC policy; they don't define it. When they disagree, the source wins. Fix the skill.

| Skill content | Source of truth |
|---|---|
| Prerequisites, eligibility, application, gates | `FFC-IN-ffcadmin.org/docs/application-prerequisites-inventory.md` |
| Guide links (`ffcadmin.org/guides/<slug>/`) | `FFC-IN-ffcadmin.org/src/data/setup-guides.ts` |
| Site-owner edit flow | `FFC-IN-ffcadmin.org/src/app/site-owner/` and `docs/site-owner-repo-config.md` |
| Charity site conventions | The template's `AGENTS.md` (`FFC-IN-Footer_Only_Template`, `FFC-IN-FFC_Single_Page_Template`) |

## Rules

- Never rename a plugin's `name` after publishing; change `displayName` instead.
- Bump `version` in the plugin's `plugin.json` on every release, or users won't get the update.
- Before committing, run `claude plugin validate . --strict`.
- Conventional Commits; branch + PR to `main`.
