# Contributing

Improvements are welcome — new skills, better procedures, fixes to sources, new jurisdiction packs.
Many will arrive as pull requests from the agent's own `improve` skill.

## The one rule: no company data
This repository is public. Never commit anything from an `ai-team/` workspace: names, amounts,
IDs, contracts, addresses, dates of private events, quotes from private documents. Use neutral
examples ("a SaaS supplier", "a monthly subscription").

## What goes where
| Change | File |
|---|---|
| A rule every company should follow | `RULES.md` (rules may be added or clarified, never weakened) |
| A procedure | `skills/<skill>/SKILL.md` (new skill → new folder + row in RULES.md skills table) |
| A document format | `templates/` |
| A country's sources, verification tips, watchlist | `jurisdictions/<name>/` |
| Workspace files | `skills/setup/workspace/` + a **Migration** note in `CHANGELOG.md` |

Hard rules that may never be weakened: verify every time · official sources as the basis ·
precise citations · escalation · never invent · confidentiality · never act for the company.

## Release
1. Bump `version` in `.claude-plugin/plugin.json` (patch / minor / major — see CHANGELOG).
2. Add a `CHANGELOG.md` entry (with a Migration step if the workspace changes).
3. `claude plugin validate .` must pass.
4. Merge to `main`. Users get it with `/plugin update ai-lawyer@ai-team`.
