---
name: legal-research
description: Answer a legal question for the founder's company — compliance, company law, data protection, contracts, employment, IP, licensing, sector regulation, and the legal side of tax. Use for any "can we / must we / what does the law say / what are the risks" question.
---

# legal-research

1. **Load memory.** `ai-team/company/profile.md`, the relevant `ai-team/company/products/*.md`,
   active lessons in `ai-team/lawyer/learnings.md`, the last ~20 entries of
   `ai-team/lawyer/history/journal.md`, and anything related in `history/decisions.md`,
   `history/contracts.md`, `history/obligations.md`, `research/` (earlier memos on the topic)
   and `laws/` (cards for the relevant acts).
2. **Pin down the facts.** List the facts you rely on and the assumptions you make. If one
   missing fact would change the answer, ask the founder that one question first (or answer
   under each alternative, clearly labelled).
3. **Map the question to areas** in `ai-team/lawyer/watchlist.md` and the product modules that
   trigger them. Name every area that applies — founders often miss tax and data-protection angles.
4. **Find the law** on Tier 1 sources (jurisdiction `sources.md`). Use secondary sources only as
   leads to find the right act and article.
5. **Run `ai-lawyer:verify-law`** for every act/provision you will rely on.
6. **Check practice** where interpretation matters: higher-court practice, constitutional court,
   regulator clarifications (Tier 2).
7. **Answer** in the format in `RULES.md` (short answer → law → interpretation with confidence →
   risks → what to do → verification → heads-up). Tax consequences → hand the exact question to
   the accountant member (see "Team work").
8. **Save** a memo `ai-team/lawyer/research/R-XXXX-slug.md` (next free number) from
   `${CLAUDE_PLUGIN_ROOT}/templates/research-memo.md` when the question is substantive (anything
   the founder may act on). Skip only for trivial lookups.
9. **Update memory** with `ai-lawyer:log-job`: journal entry; new obligations/actions; decisions
   the founder makes; watchlist additions; company facts learned; learnings.
10. **Escalate** if rule 7 applies — say so in the first line of the answer.
