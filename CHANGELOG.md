# Changelog

All notable changes to the AI lawyer. Versions follow semver: patch = fixes and wording,
minor = new skill / jurisdiction / workspace files, major = breaking workspace change.
Entries that need a workspace change list a **Migration** step; `setup` (upgrade mode) applies it.

## 0.2.0 — 2026-11-22
- The workspace is found in the project folder **or any parent folder**, so one company-level
  `ai-team/` serves several product repositories (`<company>/projects/<product>/`). The session
  hook prints the resolved workspace path.
- `setup` joins an existing workspace in a parent folder and offers the company-level layout.
- Repository moved to the HPAIF organization.
- **Migration:** none.

## 0.1.0 — 2026-11-22
- First public release, generalised from a private single-company setup.
- Agent `lawyer`, rules (`RULES.md`), skills: setup, legal-research, verify-law, add-law,
  contract-review, log-job, legal-watch, founder-briefing, improve.
- Shared AI Team workspace (`ai-team/`, contract v1) with one company profile and one file per
  product.
- Self-improvement: `learnings.md` + `improve` (anonymised, founder-approved pull requests).
- Jurisdiction pack: Armenia.
