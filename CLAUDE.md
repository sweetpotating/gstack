# gstack

## Web browsing

Use the `/browse` skill from gstack for all web browsing. Never use `mcp__claude-in-chrome__*` tools.

## Available skills

| Skill | Category |
|-------|----------|
| `/office-hours` | Plan-mode review |
| `/plan-ceo-review` | Plan-mode review |
| `/plan-eng-review` | Plan-mode review |
| `/plan-design-review` | Plan-mode review |
| `/plan-devex-review` | Plan-mode review |
| `/design-consultation` | Design |
| `/design-shotgun` | Design |
| `/design-html` | Design |
| `/design-review` | Design |
| `/autoplan` | Plan-mode review |
| `/review` | Implementation + review |
| `/investigate` | Implementation + review |
| `/codex` | Implementation + review |
| `/qa` | QA |
| `/qa-only` | QA |
| `/browse` | Browser |
| `/connect-chrome` | Browser |
| `/setup-browser-cookies` | Browser |
| `/ship` | Release + deploy |
| `/land-and-deploy` | Release + deploy |
| `/canary` | Release + deploy |
| `/setup-deploy` | Release + deploy |
| `/document-release` | Documentation |
| `/document-generate` | Documentation |
| `/benchmark` | Operational |
| `/retro` | Operational |
| `/learn` | Operational |
| `/setup-gbrain` | Operational |
| `/cso` | Security |
| `/careful` | Safety + scoping |
| `/freeze` | Safety + scoping |
| `/guard` | Safety + scoping |
| `/unfreeze` | Safety + scoping |
| `/gstack-upgrade` | Maintenance |
| `/devex-review` | DX review |

## Skill routing

When the user's request matches an available skill, invoke it via the Skill tool. When in doubt, invoke the skill.

Key routing rules:
- Product ideas/brainstorming → invoke /office-hours
- Strategy/scope → invoke /plan-ceo-review
- Architecture → invoke /plan-eng-review
- Design system/plan review → invoke /design-consultation or /plan-design-review
- Full review pipeline → invoke /autoplan
- Bugs/errors → invoke /investigate
- QA/testing site behavior → invoke /qa or /qa-only
- Code review/diff check → invoke /review
- Visual polish → invoke /design-review
- Ship/deploy/PR → invoke /ship or /land-and-deploy
- Save progress → invoke /context-save
- Resume context → invoke /context-restore
- Author a backlog-ready spec/issue → invoke /spec
