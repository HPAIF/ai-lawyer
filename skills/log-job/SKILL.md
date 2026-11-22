---
name: log-job
description: Record a job in the company's legal memory — journal entry plus updates to the contract register, decisions, obligations, shared company facts, watchlist and learnings. Use at the end of every task that produced advice, a document, a decision, a contract event, a deadline or a change of company facts (including scheduled runs).
---

# log-job

All history files are **append-only**: add rows/entries; to correct, add a new entry that
references the old one. Never delete history. Get today's date with `date +%F`.
Paths below are under `ai-team/lawyer/` unless they start with `ai-team/`.

1. **Journal** — append to `history/journal.md` (next J-number, format at the top of the file):
   request, what was done, output files, laws relied on with verification dates, follow-ups.
2. **Contracts** — any contract drafted/reviewed/signed/renewed/terminated → add or update its
   row in `history/contracts.md` (status, dates, value, key risks, memo link) and append an
   event line `C-xxxx · date · event`.
3. **Decisions** — the founder chose something (legal form, a contract position, accepting a
   risk) → append to `history/decisions.md` with the reasoning and sources.
4. **Obligations** — every deadline, recurring duty or recommended action → append a row to
   `history/obligations.md` (keep the exact table format; due date `YYYY-MM-DD` or `—`). Mark
   finished ones `done` (don't delete the row).
5. **Company facts** — new or changed facts → update `ai-team/company/profile.md`, the product
   file in `ai-team/company/products/` or `ai-team/company/documents.md`, and say in the journal
   entry what changed (these files are shared with other members).
6. **Watchlist** — new legal area surfaced → add to `watchlist.md`.
7. **Learnings** — anything this task taught you (correction, mistake, source change, missing
   step) → append to `learnings.md` with the right scope (see RULES.md).
8. Confirm to the founder in one line what was recorded (e.g. "Logged J-0007, C-0002, O-0012, L-0003").
