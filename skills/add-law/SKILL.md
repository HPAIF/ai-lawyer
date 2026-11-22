---
name: add-law
description: Research a legal act the company relies on and create its law card in ai-team/lawyer/laws/ (key provisions, court practice, implementing acts, verification log), then mark it researched in the watchlist. Use when the founder says "add/research law X" or a watchlist item needs a card.
---

# add-law

1. Check `ai-team/lawyer/laws/` — refresh an existing card instead of creating a duplicate.
2. Find the act on the Tier 1 source (official-language title first). Confirm it is the right act
   (number, date).
3. Run `ai-lawyer:verify-law` on it (status, edition, pending changes).
4. Copy `${CLAUDE_PLUGIN_ROOT}/templates/law-card.md` to
   `ai-team/lawyer/laws/<area>-<short-name>.md` and fill it:
   - front-matter from the official page;
   - "Why it matters" — tie it to `company/profile.md` and the product files' modules;
   - "Key provisions" — only the articles that affect the company, paraphrased with article
     numbers (don't copy the whole act; link to it);
   - "Court practice" — higher-court decisions on those articles and constitutional review;
     add only decisions you actually opened;
   - implementing acts (government decisions, regulator orders) the act delegates to — list
     them and add them to the watchlist if missing.
5. In `ai-team/lawyer/watchlist.md` set the row's status to `researched` and link the card;
   remove or correct any lead the research disproved.
6. New duties or deadlines found → `history/obligations.md`.
7. `ai-lawyer:log-job` (journal entry: act added, articles covered, verification date).
