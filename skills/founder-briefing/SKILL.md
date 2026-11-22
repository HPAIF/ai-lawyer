---
name: founder-briefing
description: Monthly (or on request) proactive briefing for the founder — where the company stands legally, what to do next for its stage, deadlines, gaps in documents and facts, recent legal changes, and pending self-improvements. Use for "what should I do now", "status", "am I compliant", or the monthly scheduled run.
---

# founder-briefing

Think like a careful in-house counsel at a start-up: practical, prioritised, cheap first.

1. **Load everything**: `ai-team/company/`, `ai-team/lawyer/history/`, digests since the last
   briefing, `watchlist.md`, `laws/`, `learnings.md`; `ai-team/team.md` for other members.
2. **Stage check** — for the company's stage (pre-incorporation → incorporated → first customer
   → hiring → scaling / foreign markets), list what a company at this stage in this jurisdiction
   should have done, and compare with `ai-team/company/documents.md` and `history/decisions.md`.
   Typical items: legal form decision; registration; bank account; accountant; trademark;
   standard customer contract + DPA + SLA; privacy policy; data protection setup;
   employment/contractor templates with IP assignment; fiscal/receipt design of the product;
   security policy; insurance.
3. **Calendar** — overdue and next-60-days items from `history/obligations.md`.
4. **Contracts** — renewals, notice periods, expiring contracts from `history/contracts.md`.
5. **Law changes** — summarise legal-watch digests since the last briefing; anything needing a
   decision.
6. **Verify** every law-based recommendation with `ai-lawyer:verify-law` (UNVERIFIED if not).
7. **Self-improvement** — count `general` learnings that are `pending`; if any, propose running
   `ai-lawyer:improve`.
8. **Write** `ai-team/lawyer/digests/YYYY-MM-DD-founder-briefing.md`:
   ```
   # Founder briefing — YYYY-MM-DD
   ## Top 3 things to do this month
   ## Deadlines (overdue / next 60 days)
   ## Gaps (missing documents, missing facts, undecided questions)
   ## Law changes affecting you
   ## When to pay for a real lawyer this month (if at all)
   ## Questions for other team members
   ## Agent self-improvement (pending learnings)
   ```
9. `ai-lawyer:log-job` (journal entry; new rows in obligations; open questions recorded).
