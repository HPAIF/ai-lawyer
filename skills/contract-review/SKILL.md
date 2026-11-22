---
name: contract-review
description: Review, draft or redline a contract or legal document for the company (subscription/SaaS terms, SLA, DPA, NDA, employment, contractor, partner, lease, terms of service, privacy policy) under the company's jurisdiction, and enter it in the contract register.
---

# contract-review

1. **Load memory**: `ai-team/company/` files; `ai-team/lawyer/history/contracts.md` (earlier
   deals with this party, our standard positions); `history/decisions.md`; earlier
   `research/CR-*` memos; active lessons in `learnings.md`.
2. **Identify**: parties, our side, type, value, term, governing law, language, signing method.
   Register it now in `history/contracts.md` with status `draft`/`negotiating` (next free C-id).
3. **Check against the law** (run `ai-lawyer:verify-law` on every provision you cite):
   - civil/contract law: formation, form requirements, penalties/liquidated damages, limits on
     limitation of liability, unilateral termination, limitation periods;
   - language and form requirements for contracts with local parties;
   - personal data (who processes what, transfers abroad, security, breach notice);
   - fiscal duties (cash register / e-receipts) if the product issues receipts;
   - cybersecurity / critical-infrastructure duties if the customer is in a regulated sector;
   - tax: VAT, withholding for foreign counterparties (→ ask the accountant member);
   - IP: ownership of code, licences, open source;
   - competition: exclusivity, price-related clauses, information exchange between competitors;
   - anything the jurisdiction pack README lists as a local mandatory check.
4. **Commercial checks**: liability cap vs. value, SLA credits, uptime definitions, data export
   at termination, payment terms and late penalties, auto-renewal, change of control, dispute
   resolution (courts vs. arbitration, venue).
5. **Write the review** from `${CLAUDE_PLUGIN_ROOT}/templates/contract-review.md` →
   `ai-team/lawyer/research/CR-XXXX-slug.md`, with a clear verdict and suggested wording for
   each issue. When drafting, produce bilingual text only if the founder asks; otherwise English
   plus a note on any language requirement.
6. **Track**: every date/obligation in the contract (renewal notice, payment, reporting, SLA
   reports, data deletion) → `history/obligations.md`. On signing/termination, update the
   register row and its event log. If an accountant member exists, note the contract's money
   terms for them (`accountant` registers it on their side).
7. `ai-lawyer:log-job`. Escalate per rule 7 (value above threshold, unusual liability, foreign
   law, exclusivity with a large customer).
