---
name: setup
description: Set up (or repair/upgrade) the AI lawyer in the current project — creates the private ai-team/ workspace (shared company files + ai-team/lawyer/), seeds the watchlist from a jurisdiction pack, registers the lawyer in team.md, and offers permissions, privacy and scheduled runs. Use on first use in a project, when the workspace is missing, or after a plugin update that changes the workspace.
---

# setup

Template files are in `${CLAUDE_PLUGIN_ROOT}/skills/setup/workspace/`. Never overwrite an
existing file in `ai-team/` — the workspace may already hold real history.

1. **Explain** in two lines what will be created (`ai-team/` private workspace) and that nothing
   leaves the machine.
2. **Ask** (one question at a time, skip what is already in `ai-team/team.md`):
   - jurisdiction — list the folders in `${CLAUDE_PLUGIN_ROOT}/jurisdictions/` as options, plus
     "other" (generic mode);
   - answer language (default English).
3. **Create shared files if missing** (another member may have created them already):
   `ai-team/README.md`, `ai-team/team.md`, `ai-team/company/profile.md`,
   `ai-team/company/documents.md`, `ai-team/company/products/_template.md`. Fill `team.md`
   (jurisdiction, date, `workspace_contract: 1`) and the profile's stage date and jurisdiction.
4. **Create the member folder** `ai-team/lawyer/` from the template's `lawyer/` folder:
   `learnings.md`, `history/{journal,contracts,decisions,obligations}.md`, `laws/README.md`,
   `research/README.md`, `digests/README.md`, `inbox/README.md`.
5. **Seed the watchlist:** copy `${CLAUDE_PLUGIN_ROOT}/jurisdictions/<name>/watchlist.md` to
   `ai-team/lawyer/watchlist.md`. Generic mode → create a watchlist with the standard areas
   (formation, tax, personal data, contracts, IP, employment, sector rules) and an empty
   `ai-team/lawyer/sources.md` to fill with official sources on first research.
6. **Register** a row in `team.md`: `lawyer | ai-lawyer | ai-lawyer:lawyer | ai-team/lawyer/ |
   <plugin version> | <today> | legal research, contracts, compliance, legal watch`.
7. **First journal entry** `J-0001 · <today> · setup` and obligations
   `O-0001` "Fill in company/profile.md and a product file in company/products/" (due in 14 days).
   If products are described in the project (README, docs), offer to draft the product file
   from them — the founder confirms before you write.
8. **Offer, don't force** (ask each; do only what is approved):
   - **Privacy:** if the project is a git repo, add `ai-team/` to `.gitignore`; suggest
     `git init` inside `ai-team/` for private history.
   - **Permissions:** merge the `allow` list from `jurisdictions/<name>/permissions.json` into
     the project's `.claude/settings.json` so official sources can be fetched without prompts.
   - **Scheduled runs:** weekly `legal-watch` (e.g. Mondays 09:00) and monthly
     `founder-briefing` (1st of month). Create them if a scheduling tool is available in this
     session; otherwise explain how to schedule them in the Claude app.
9. **Upgrade mode** (workspace exists): compare with the template, create only missing files or
   folders, apply migrations listed in `CHANGELOG.md` for versions newer than the one in
   `team.md`, update the version in `team.md`, and log what changed.
10. Finish with a short summary: what exists now, the three most useful first questions to ask
    the lawyer, and `log-job`.
