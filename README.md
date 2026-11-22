# AI Lawyer

An in-house legal research assistant for founders, running in Claude Code. Part of the
**[AI Team](https://github.com/HPAIF/ai-team)** — agents that work together for your company.

It researches the law from **official sources**, checks that every law is current **each time**
it uses it, reviews and drafts contracts, keeps your company's legal history, watches for legal
changes, and gets better from what it learns.

> **It is not a licensed lawyer.** For courts, authorities, large contracts and anything with real
> liability it tells you to get one — and prepares a brief so the paid hours are few.

## Install

In Claude Code:

```
/plugin marketplace add HPAIF/ai-team
/plugin install ai-lawyer@ai-team
```

Or install only this member, straight from its repository:

```
/plugin marketplace add HPAIF/ai-lawyer
/plugin install ai-lawyer@ai-lawyer
```

Then, in your project, say **"set up the AI lawyer"**. The `setup` skill creates a private
`ai-team/` workspace, asks your jurisdiction, and offers permissions, `.gitignore` and scheduled
runs. Nothing leaves your machine.

To share the setup with your team, commit this to the project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "ai-team": { "source": { "source": "github", "repo": "HPAIF/ai-team" } }
  },
  "enabledPlugins": { "ai-lawyer@ai-team": true }
}
```

## Use it

Talk normally — Claude hands legal work to the `ai-lawyer:lawyer` agent — or start a session as
the lawyer: `claude --agent ai-lawyer:lawyer`.

| You say | What happens (skill) |
|---|---|
| "Which legal form should I choose?" | verified research memo (`legal-research`) |
| "Add the Tax Code" / "research the personal data law" | law card with verification log (`add-law`) |
| "Review the contract in ai-team/lawyer/inbox/acme.pdf" | review memo + contract register entry (`contract-review`) |
| "I signed it today" / "we registered the company" | history and company facts updated (`log-job`) |
| "What changed in the law?" | digest with actions (`legal-watch`) |
| "What should I do now?" | founder briefing (`founder-briefing`) |
| "Improve yourself" | anonymised upgrade proposal for this plugin (`improve`) |

Each session in a project with a workspace starts with overdue and upcoming obligations, recent
jobs, stale law cards and pending learnings (session hook).

**Scheduled runs** (offered by `setup`): weekly `legal-watch` and monthly `founder-briefing`.

## How it is built

```
RULES.md                 hard rules: verify every time, official sources, cite, escalate, never invent…
agents/lawyer.md         the agent (reads RULES.md, the jurisdiction pack and the workspace)
skills/                  setup · legal-research · verify-law · add-law · contract-review ·
                         log-job · legal-watch · founder-briefing · improve
templates/               research memo, law card, contract review
jurisdictions/<name>/    country packs: how to verify, sources, baseline watchlist, permissions
hooks/                   session-start context
```

Your data lives in **your project**, never in the plugin:

```
ai-team/
├── team.md                  installed members, jurisdiction
├── company/                 shared with other members: profile, documents, products/<product>.md
└── lawyer/                  learnings, watchlist, history (journal, contracts, decisions,
                             obligations), laws, research, digests, inbox
```

See the [workspace contract](https://github.com/HPAIF/ai-team/blob/main/docs/workspace.md).

## Privacy
- The plugin is public; your workspace is private. Keep `ai-team/` out of public repositories
  (`setup` offers to add it to `.gitignore`) — `git init` inside it for a private history.
- The lawyer searches the web for the *legal question*, never your company's facts.
- Files the agent reads are processed by the model you use in Claude Code.

## Self-improvement
1. After corrections, mistakes, broken sources or missing steps, the lawyer writes a lesson to
   `ai-team/lawyer/learnings.md` and applies it from then on.
2. Lessons useful to everyone are marked `general`. The `improve` skill turns them into an
   anonymised pull request to this repository — only after you approve the exact text, and never
   one that weakens the hard rules.
3. Merged improvements reach every user with the next plugin update.

## Jurisdictions
Included: **Armenia**. Other countries: choose "other" in `setup` (generic mode) and contribute a
pack — see [jurisdictions/README.md](jurisdictions/README.md).

## Upgrading
`/plugin marketplace update ai-team`, then `/plugin update ai-lawyer@ai-team` (restart Claude
Code). Run "set up the AI lawyer" again to apply workspace migrations; it never overwrites your
history.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md). License: [MIT](LICENSE).
