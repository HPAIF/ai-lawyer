# Jurisdiction packs

The AI lawyer's rules and skills are jurisdiction-neutral. Everything country-specific lives in a
pack: `jurisdictions/<name>/` (lowercase, e.g. `armenia`, `georgia`, `germany`).

| File | What it holds |
|---|---|
| `README.md` | language rules; how law is published and **how to verify a provision** there; local mandatory contract checks; monitoring guide (parliament, draft portal, regulators, search keywords); known access issues |
| `sources.md` | official source registry: Tier 1 (authoritative texts), Tier 2 (regulators), Tier 3 (leads only), rules of use |
| `watchlist.md` | baseline topics for a typical company there (copied into the workspace by `setup`) |
| `permissions.json` | `{"permissions":{"allow":[…]}}` WebFetch allow-list for the official sources |

## No pack for your country?
Choose "other" during `setup`. The lawyer works in generic mode, builds
`ai-team/lawyer/sources.md` from official government sources on first research, and records
learnings. Run the `improve` skill later to contribute a new pack — without any company data.

## Available
- `armenia/` — Republic of Armenia (plus EAEU, and EU only when relevant).
