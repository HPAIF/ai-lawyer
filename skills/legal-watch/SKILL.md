---
name: legal-watch
description: Proactive scan of the jurisdiction's official sources for new laws, amendments, drafts, court positions and regulator news that affect the company; writes a digest with recommended actions and updates obligations. Runs weekly on a schedule; also use when the founder asks "what changed / anything new".
---

# legal-watch

Runs without the founder: never ask questions — record them as obligations. Be concrete and
short, and report only what matters to *this* company.

1. **Load context**: `ai-team/company/profile.md`, `ai-team/company/products/*.md`,
   `ai-team/lawyer/watchlist.md`, the jurisdiction pack (`README.md`, `sources.md`),
   `history/obligations.md`, `laws/` cards, active lessons, and the previous digest in
   `ai-team/lawyer/digests/` (last scan date; avoid repeating items). If an accountant member
   exists, skim its latest tax-watch digest to avoid duplicates and pick up legal angles.
2. **Scan since the last digest** (or the last 14 days if none), using the pack's monitoring
   guide:
   - parliament — bills introduced/adopted on watchlist topics;
   - government draft-consultation portal — drafts open for comment (note the deadline — the
     founder may want to comment);
   - consolidated-law source — newly published acts and amendments to acts with law cards; any
     card whose `pending_changes` entry-into-force date has now passed;
   - regulators relevant to the company's products (tax, data protection, sector, competition,
     central bank only if money flows through the product);
   - web search for news **as leads only**, with the pack's keywords. Confirm every item on a
     Tier 1/2 source before reporting it as fact; otherwise label it "unconfirmed lead".
3. **Assess each item**: what changes, from when, who it affects, does it affect the company
   (now / when incorporated / when a module launches), confidence.
4. **Write** `ai-team/lawyer/digests/YYYY-MM-DD-legal-watch.md`:
   ```
   # Legal watch — YYYY-MM-DD (period scanned: … → …)
   ## Deadline radar (open obligations overdue or due in 14 days)
   ## Action needed (most urgent first)
   ## Coming changes to prepare for
   ## Drafts open for comment
   ## No action — for awareness
   ## Sources checked (and any that failed)
   ```
   If nothing relevant changed, say so in one line and still list the sources checked.
5. **Update memory**: new deadlines/actions → `history/obligations.md`; new topics →
   `watchlist.md`; law cards with new pending changes → front-matter + log row; failed or moved
   sources → learning; `ai-lawyer:log-job` with request "scheduled: legal-watch".
6. Never submit comments, email or contact anyone. Research and write files only.
