# Changelog

All notable changes to the AI lawyer. Versions follow semver: patch = fixes and wording,
minor = new skill / jurisdiction / workspace files, major = breaking workspace change.
Entries that need a workspace change list a **Migration** step; `setup` (upgrade mode) applies it.

## 0.2.5 — 2026-11-28
- Shorter replies: chat answers are about 5 lines by default (answer first, no headings, at most
  3 bullets, no report of housekeeping). The full answer format is for memos and full analyses;
  long content goes into a workspace file with the path in the chat.

## 0.2.4 — 2026-11-23
- Talk to colleagues only where the founder sees it: no hidden Agent-tool calls; @mention in group
  chats (one answer, no discussion without the founder); "For @member:" elsewhere.

## 0.2.3 — 2026-11-23
- Missed questions: an unanswered question that still matters is repeated briefly under
  "Still open:" at the end of the next answer.

## 0.2.2 — 2026-11-23
- Ask colleagues directly, never through the founder: @mention in group chats, the Agent tool
  as main agent, "Question for @member" when called by the lead.

## 0.2.1 — 2026-11-23
- Rule "Be concise": shortest answer that keeps all important information (warnings, numbers,
  dates, sources, decisions); long only when the content needs it.

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
